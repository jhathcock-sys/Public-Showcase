---
title: Zero-Clobber Real-Time Synchronization
description: Preventing cold-start overwrites and offline partition collisions across multi-device PWAs and mobile guard consoles using atomic transactions, per-entity timestamp merging, and idempotent FIFO outboxes.
tags:
  - architecture
  - distributed-sync
  - firestore
  - offline-first
updated: 2026-11-17
---

# Zero-Clobber Real-Time Synchronization

Shared operational apps rarely fail on a single laptop sitting on fiber. They fail at 06:00 AM shift change when three supervisors pull phones out of their pockets simultaneously, an offline tablet reconnects from a concrete basement, or a cold-start browser tab opened via a quick NFC tag tap writes state before its local store finished hydrating.

With naive "last-writer-wins" document saves, the cold-start device overwrites ten minutes of live peer checkouts with stale defaults. Across both [Arclight Security](../01_Products/Arclight-Security-ERP.md) and our [Retail Operations PWAs](../01_Products/Retail-Operations-PWAs.md), we eliminate silent data loss using four concrete defenses.

---

## Concurrent Merge Flow

```mermaid
sequenceDiagram
    autonumber
    participant Phone as Cold-Start Phone (NFC Tap)
    participant Tablet as Roaming Supervisor Tablet
    participant Cloud as Firestore Transaction Engine

    Note over Phone: Scans Asset #04 locally before full hydration
    Phone->>Cloud: runTransaction(read remote -> mergeStoreState -> set)
    Tablet->>Cloud: Concurrent update on Asset #09
    Cloud-->>Phone: Reads authoritative remote snapshot inside txn
    Note over Phone: Unions rosters & devices; compares per-asset timestamps
    Phone->>Cloud: Commits merged state (Asset #04 updated, Asset #09 preserved)
    Cloud-->>Tablet: Real-time onSnapshot delivers converged view
```

---

## 1. Atomic Read-Merge-Write with Per-Entity Timestamps

Instead of blind `setDoc(ref, localState)` writes, shared operational documents commit inside an atomic **`runTransaction`** (with a resilient `getDoc` + `setDoc` fallback only when the device is explicitly partitioned offline).

Inside the transaction, **`mergeStoreState`** and **`mergeCollectionById`** resolve conflicts at the **item level** rather than the document level:
- **Device & Roster Unions:** Active device registrations (`registeredDevices`) and employee rosters union deterministically by normalized ID/name, preserving the higher `lastActiveAt` heartbeat.
- **Per-Asset Timestamp Arbitration:** For each tracked asset or key ring, the merger calculates `Math.max(checkedOutAt, lastCheckedInAt)` on both local and remote records. Whichever record holds the newer event wins for that individual asset—so Device A checking out a scanner never reverts Device B's return of a key ring two seconds earlier.
- **Custom Metadata Preservation:** Asset renames (`renamedAt`) and slot reassignments follow independent timestamp comparisons so factory-default placeholders on a freshly booted phone never clobber custom floor labels saved earlier in the week.

---

## 2. Sanitization & Firestore `1 MiB` Ceiling Defense

Cloud Firestore rejects any write containing `undefined` object properties and enforces a hard `1,048,576`-byte (`1 MiB`) limit per document. Real-world field tools routinely collect hundreds of scan logs and audit records over time.

1. **Zero `undefined` Crashes:** Every Firestore client initializes with `initializeFirestore(app, { ignoreUndefinedProperties: true })`, backed by an explicit recursive sanitization pass (`stripUndefined`) before transaction submission.
2. **Proactive `750 KB` Pruning Watermark:** Before writing shared state documents, a UTF-8 byte-size estimator (`TextEncoder`) checks payload footprint. Whenever serialized size crosses **`750 KB`** (leaving over `250 KB` of headroom), ephemeral rolling event buffers (`logs`, `checkEvents`, `audits`) trim deterministically from oldest timestamps downward—guaranteeing high-frequency checkout logs never brick the live state document mid-shift.

---

## 3. Idempotent FIFO Offline Outboxes

Transactions protect connected peers, while **idempotent FIFO outboxes** protect mobile workers walking into RF dead zones.

In Arclight's Mobile Guard store (`FieldStore`), field mutations—`CLOCK_IN`, `CHECKPOINT_SCAN`, `DAR_SUBMIT`, `INCIDENT_SUBMIT`, `POLICY_SIGN`, `ARMORY_CHECKOUT`, `BOLO_ACK`, and `RADIO_CLIP_UPLOAD`—never get lost when cellular bars drop:
- **Deterministic `idempotencyKey`:** Every queued action hashes its payload plus original creation timestamp (`{TYPE}-{hash}-{epochMs}`), preventing duplicate server records if an HTTP callback succeeds remotely just before the mobile socket drops.
- **Timestamp Preservation:** Actions keep their original offline event timestamp (`recordedAt` / `timestamp`) alongside retry counters (`PENDING -> SYNCING -> SYNCED | FAILED`) rather than inheriting the reconnect wall-clock time—preserving legal accuracy for geofence clock-ins, guard tours, and dead-zone radio logs.

---

## 4. Boundary-Safe Tenant Isolation

Real-time state convergence never crosses security boundaries. Where external portals (`CLIENT_VIEWER`) subscribe to live streams, read queries and `onSnapshot` listeners target strictly filtered sub-collections scoped by `orgId`, `clientId`, and `clientVisible == true`—ensuring high-frequency multi-device operational state never mixes confidential internal records into client-readable documents.
