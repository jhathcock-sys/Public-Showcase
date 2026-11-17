---
title: Engineering & Product Documentation — Hathcock Labs
description: Vault homepage detailing Hathcock Labs' verification-first software philosophy, heterogeneous compute architecture, and chapter map across products, AI systems, and engineering deep dives.
tags:
  - index
  - engineering
  - ai-systems
  - architecture
  - hathcock-labs
updated: 2026-11-17
---

# Engineering & Product Documentation — Hathcock Labs

Most software failures in regulated operations, clinical education, and physical floor tooling do not happen because a UI framework lacked animations. They happen because someone left statutory licensing rules in a PDF binder instead of TypeScript evaluators, let cold-start mobile devices overwrite live database records, trusted an unconstrained LLM to verify its own clinical claims, or shipped a mobile web layout without testing how iOS Safari handles `<dialog>` and `AudioContext`.

At **Hathcock Labs**, every codebase and AI engineering workflow follows one core standard: **human-directed, verification-first craftsmanship**.

```mermaid
flowchart LR
    Human["Human Architect\nScope · Risk Tolerances · Sign-Off"] --> AI["AI Cognitive Stack\n18 Specialists · <=2,000-Token Contexts · Hybrid RRF Memory"]
    AI --> Verify["Verification Stack\nAdversarial Auditor · Secret/Lint Hooks · Typecheck · Playwright DOM/WCAG"]
    Verify --> Products["Production Systems\nTri-State Security ERP · iOS Board Prep · Floor PWAs · Parametric CAD"]
```

---

## Core Engineering Axioms

### 1. Deterministic Code Over Prose Rules
Whether checking if a Pennsylvania security officer holds an active Act 235 card before releasing an expandable baton (`18 Pa. C.S. § 908`), calculating FLSA `29 C.F.R. § 778.115` weighted-average overtime in integer cents, or enforcing a `<= 2,000`-token ceiling on subagent dispatches, critical invariants belong in deterministic, tested code—not wishful prompts or manual checklists.

### 2. Heterogeneous Compute & Zero-Waste Token Economics
Rather than burning cloud frontier quotas on every mechanical task, workloads distribute intentionally across hardware tiers:
- **Sub-Millisecond Scratch NVMe:** SQLite WAL FTS5 retrieval (`<1.5 ms`), compiler caches, and atomic `fcntl.flock` handoff locks.
- **Always-On Apple Silicon M1 Max Inference (`squad-local`):** 5-model zero-cloud-token CLI serving `nomic-embed-text` (`768d` vectors), `hermes3:8b` (automatic `01_Dispatch/` JSON triage & 5-bullet digests), `qwen2.5-coder:14b` (code/regex/SQL reviews), `deepseek-r1:14b` (step-by-step sanity checks), and `qwen3:14b` (general local Q&A), plus automated round-trip DR verification.
- **Cloud Frontier Tiers:** Reserved deliberately for safety-critical reasoning (`Echo` clinical accuracy, `Vault` security rules, `Apex` auth/webhooks, `Nexus` sync races, `Sentinel` IAM boundaries) and deep architecture.

### 3. Physical Reality First (Gloves, Dead Zones & WebKit Quirks)
Software runs in bright daylight offices, concrete basements with zero LTE, hurried stockrooms, and handheld devices operated one-handed. Our modules filter `<35ms` laser scanner bursts away from Spacebar PTT hotkeys, recover iOS WebKit `'interrupted'` audio states on lock-screen wake, bridge dead zones with `idempotencyKey`-deduplicated FIFO queues, and print solid plastic NFC enclosures mid-layer in OpenSCAD.

### 4. Adversarial Truth & Zero-Slop Design Discipline
Every unverified legal claim or browser quirk passes an independent, context-isolated external audit (`Scout` ↔ `Muse`), production AI runs locked behind `temperature: 0.0` Zod contracts preserving raw officer testimony verbatim, and automated headless Playwright DOM/WCAG verification prevents dark-slate UI clones or clipped controls from ever reaching builds.

---

## How the AI Stack Connects Directly to Shipped Systems

| Cognitive Layer / Mechanism | Production Guarantee Delivered Across Products | Primary Reference |
| :--- | :--- | :--- |
| **Mandatory `pro` Clinical & Rules Locks** | Zero unverified medical ratios (`Echo`) & airtight 13-collection `CLIENT_VIEWER` isolation (`Vault` / `Apex`) | [01 · The 18-Specialist Squadron](02_AI-Systems-Architecture/01-The-18-Specialist-Squadron.md) |
| **Optane FTS5 + Hybrid RRF (`k = 60`)** | Surfaces solved WebKit, FLSA `29 C.F.R. § 778.115`, and `pnpm` build fixes in `<1.5 ms` | [02 · Five-Tier Memory & Hybrid RRF](02_AI-Systems-Architecture/02-Five-Tier-Memory-and-Hybrid-RRF.md) |
| **`<=2,000`-Token Differential Compiler** | Eliminates context rot during 5-package refactors while gating dual quota caps live | [03 · Differential Context & Quota](02_AI-Systems-Architecture/03-Differential-Context-and-Quota-Governance.md) |
| **Two-Node Dropzone + Schema-Locked AI** | Catches PA/DE/MD statutory & Safari `<dialog>` traps pre-code; preserves immutable raw testimony | [04 · Adversarial & Fact-Locked AI](02_AI-Systems-Architecture/04-Adversarial-Verification-and-Fact-Locked-AI.md) |
| **Chained Git/Playwright Gates & DR** | Enforces clean TypeScript, passing tests, DOM contrast, `0600` keys & tested off-box restores | [05 · Autonomous DevOps & Gates](02_AI-Systems-Architecture/05-Autonomous-DevOps-and-Zero-Trust-Gates.md) |
| **Kernel `inotify` + Apple Silicon Inference** | Turns on-foot field voice notes into routed tasks at `0 MB` idle RAM & `0` local vector tokens | [06 · Mobile Dispatch & Local LLM](02_AI-Systems-Architecture/06-Ambient-Mobile-Dispatch-and-Local-Inference.md) |

---

## Verified Quantitative Snapshot

- **Arclight Security (`v0.3`):** `5/5` workspace packages typecheck clean; `25/25` test suites (`205/205` unit & integration tests passing); `0` visual/WCAG defects across `1440×900` and `375×812`.
- **SonoPrep Pro (`iOS`):** `421` audited RVT/SPI questions, `132` SVGs, `18` interactive hotspots, `34/34` unit/App Store compliance tests, `15/15` E2E stages, `0` `oxlint` warnings, `<500 KB` bundles.
- **Cognitive Tooling:** `<1.5 ms` Optane FTS5 search, `93%` blackboard initialization token drop (`8` active slots), `100%` `768d` embedding cache parity, `<3.5s` parallel 22-invariant cross-node verification.

---

## Three-Node Compute Allocation Summary

| Node Role | Hardware Profile | Dedicated Workloads | Endurance & Protection Model |
| :--- | :--- | :--- | :--- |
| **Workstation Node** | 4C/8T Laptop · `12 GB` RAM + `11.4 GB` zram · **Optane NVMe Scratch** | Interactive development, `memory.db` WAL FTS5 (`<1.5 ms`), `ccache`/Rust/Node caches, `inotify` dispatch triggers | `vm.vfs_cache_pressure=50`, `[none]` I/O scheduler, `earlyoom` `--avoid` protection |
| **Inference & Backup Node** | Always-On Unified-Memory **Apple Silicon M1 Max (`32 GB`)** | `squad-local` 5-model lineup (`nomic-embed-text`, `hermes3:8b` `01_Dispatch/` triage, `qwen2.5-coder:14b`, `deepseek-r1:14b`, `qwen3:14b`), container stack, 4-step DR verification | `launchd` container & `300s` vector watchdogs; `0` cloud tokens burned locally |
| **Edge Network Node** | `8 GB` **ARM SBC** | Primary network DNS filter + unified plain-English control telemetry HUD | Volatile RAM `journald`, `noatime,commit=60` mount, `300s` SQLite flush batching |

---

## Complete Documentation Map

### 01 · Shipped Products & Hardware Systems
- [Arclight Security ERP & CAD](01_Products/Arclight-Security-ERP.md) — Replacing the 4-vendor contract security stack across Maryland, Delaware, and Pennsylvania.
- [SonoPrep Pro (iOS)](01_Products/SonoPrep-iOS.md) — Commercial ARDMS RVT/SPI vascular board prep with a 100% On-Device Study Vault and live Doppler physics simulation.
- [High-Velocity Retail Floor & Asset PWAs](01_Products/Retail-Operations-PWAs.md) — Single-handed mobile custody and coaching planners built for `<35ms` barcode wedges and instant NFC cold starts.
- [Parametric Additive CAD & Hardware Fixtures](01_Products/Additive-CAD-and-Hardware-Fixtures.md) — OpenSCAD CSG mounts, cantilever snap-fits, and pause-at-layer embedded RFID/NFC enclosures.

### 02 · AI Systems Architecture (7-Chapter Flagship Series)
- [00 · Cognitive Architecture Overview](02_AI-Systems-Architecture/00-Cognitive-Architecture-Overview.md) — Solving single-context decay across our 3-node heterogeneous compute topology.
- [01 · The 18-Specialist Squadron](02_AI-Systems-Architecture/01-The-18-Specialist-Squadron.md) — Individual profiles of all 18 engineering roles, inter-agent seams, zero-mention routing, and tiered audits.
- [02 · Five-Tier Memory & Hybrid RRF Retrieval](02_AI-Systems-Architecture/02-Five-Tier-Memory-and-Hybrid-RRF.md) — Structural repo maps, `fcntl.flock` rolling blackboards, FTS5 BM25 + 14-day recency, and `k = 60` Reciprocal Rank Fusion.
- [03 · Differential Context & Quota Governance](02_AI-Systems-Architecture/03-Differential-Context-and-Quota-Governance.md) — `<= 2,000`-token compiler, 8-step trim ladder, anti-dump detectors, mandatory frontier locks, and live HUD math.
- [04 · Adversarial Verification & Fact-Locked AI](02_AI-Systems-Architecture/04-Adversarial-Verification-and-Fact-Locked-AI.md) — Two-node adversarial research (`Scout` ↔ `Muse`) and schema-locked, raw-transcript-preserving production AI.
- [05 · Autonomous DevOps & Zero-Trust Gates](02_AI-Systems-Architecture/05-Autonomous-DevOps-and-Zero-Trust-Gates.md) — Pre-commit secret/lint gates, workspace pre-push `tsc` + `vitest`, Playwright WCAG visual gates, 22-check drift doctor, and DR restores.
- [06 · Ambient Mobile Dispatch & Local Inference](02_AI-Systems-Architecture/06-Ambient-Mobile-Dispatch-and-Local-Inference.md) — Zero-RAM `inotify` inbox triggers, automatic `hermes3:8b` JSON dispatch triage, and 5-model `squad-local` offloading.

### 03 · Systems & UI Deep Dives
- [Half-Duplex Push-to-Talk Over LTE](03_Architecture-Deep-Dives/Half-Duplex-PTT-Over-LTE.md) — Lease-backed floor locks, `10-33 SOS` preemption, synthesized radio chirps, and LiveKit + dead-zone replay.
- [Statutory Compliance as Deterministic Code](03_Architecture-Deep-Dives/Statutory-Compliance-As-Code.md) — MD/DE/PA evaluators, integer-cents FLSA `29 C.F.R. § 778.115` overtime, and Dark-Hours SLA liquidation math.
- [Zero-Clobber Real-Time Synchronization](03_Architecture-Deep-Dives/Zero-Clobber-Realtime-Sync.md) — Atomic `runTransaction` per-entity timestamp merging, `750 KB` log pruning ahead of `1 MiB` caps, and FIFO outboxes.
- [Anti-Slop UI Engineering & WebKit Resilience](03_Architecture-Deep-Dives/Anti-Slop-UI-Engineering.md) — Domain archetypes, `OKLCH` + `color-mix()` tokens, native `<dialog>` coordinate guards, and Safari platform fixes.

### 04 · Engineering Build Log
- [November 2026 Engineering Milestones](04_Build-Log/2026-11-Milestones.md) — Verified production benchmarks, test counts, and platform releases.
