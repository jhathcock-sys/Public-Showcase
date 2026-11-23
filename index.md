---
title: Engineering & Product Documentation — Hathcock Labs
description: Vault homepage detailing Hathcock Labs' verification-first software philosophy, heterogeneous compute architecture, and chapter map across products, AI systems, and engineering deep dives.
tags:
  - index
  - engineering
  - ai-systems
  - architecture
  - hathcock-labs
updated: 2026-11-23
---

# Engineering & Product Documentation — Hathcock Labs

Most software failures in regulated operations, clinical education, programmatic media rendering, and physical floor tooling do not happen because a UI framework lacked animations. They happen because someone left statutory licensing rules in a PDF binder instead of TypeScript evaluators, let cold-start mobile devices overwrite live database records, trusted an unconstrained LLM to verify its own clinical claims, or shipped a mobile web layout without testing how iOS Safari handles `<dialog>` and `AudioContext`.

At **Hathcock Labs**, every codebase and AI engineering workflow follows one core standard: **human-directed, verification-first craftsmanship** orchestrated across **12 repositories** under **`Halcyon` (XO & Flight Director)**, **18 specialized roles**, and external adversarial auditor **`Muse`**.

```mermaid
flowchart LR
    Human["Human Architect\nScope · Risk Tolerances · Sign-Off"] --> AI["AI Cognitive Stack\nHalcyon XO + 18 Specialists · <=2,000-Token Contexts · Hybrid RRF"]
    AI --> Verify["Verification Stack\nAdversarial Auditor · <5ms Hooks · 24/24 Pro Rulesets · Playwright WCAG"]
    Verify --> Products["Production Systems (12 Repos)\nSecurity ERP + PTT · iOS Board Prep · Video Engine · PWAs · CAD"]
```

---

## Core Engineering Axioms

### 1. Deterministic Code Over Prose Rules
Whether checking if a Pennsylvania security officer holds an active Act 235 card before releasing an expandable baton (`18 Pa. C.S. § 908`), calculating FLSA `29 C.F.R. § 778.115` weighted-average overtime in integer cents, or enforcing a `<= 2,000`-token ceiling on subagent dispatches, critical invariants belong in deterministic, tested code—not wishful prompts or manual checklists.

### 2. Heterogeneous Compute & Zero-Waste Token Economics
Rather than burning cloud frontier quotas on every mechanical task, workloads distribute intentionally across hardware tiers:
- **Sub-Millisecond Scratch NVMe:** SQLite WAL FTS5 retrieval (`<1.5 ms`), compiler caches, and atomic `fcntl.flock` handoff locks.
- **Always-On Apple Silicon M1 Max Inference (`squad-local`):** Flash-Attention + `q8_0` KV cache + `8K` context-cap local inference eliminating `64K` Modelfile eviction thrash (**`qwen3:8b` at `4.8 GB` VRAM / `37 tok/s`** co-resident with pinned **`nomic-embed-text`** at **`0` evictions & `0 MB` swap**), plus `14B` local review tiers (`qwen2.5-coder:14b`, `deepseek-r1:14b`, `qwen3:14b`) and automated round-trip DR verification at **`0` cloud tokens**.
- **27-Model Cloud Frontier Tiers (Pool 1 + Pool 2):** Routes `>95%` of work across `20` Pool 1 Gemini models—combining runtime subagent delegation (`inherit` → **Gemini 4 Neon High**, `pro`/`flash` → **Gemini 4 Hydrogen** tiered coding) with explicit `/swarm` pinning (`gemini-4-neon-xhigh`) for safety-critical reasoning (`Echo` clinical accuracy, `Vault` security rules, `Apex` auth/webhooks, `Nexus` sync races, `Sentinel` IAM boundaries)—while reserving `7` Pool 2 cross-vendor models (Claude 5.5; excluding sunsetting GPT-OSS 120B) selectively for release-gate cross-checks.

### 3. Physical Reality First (Gloves, Dead Zones & WebKit Quirks)
Software runs in bright daylight offices, concrete basements with zero LTE, hurried stockrooms, and handheld devices operated one-handed. Our modules filter `<35ms` laser scanner bursts away from Spacebar PTT hotkeys, recover iOS WebKit `'interrupted'` audio states on lock-screen wake, bridge dead zones with `idempotencyKey`-deduplicated FIFO queues, and print solid plastic NFC enclosures mid-layer in OpenSCAD.

### 4. Adversarial Truth & Zero-Slop Design Discipline
Every unverified legal claim or browser quirk passes an independent, context-isolated external audit (`Scout` ↔ `Muse`), production AI runs locked behind `temperature: 0.0` Zod contracts preserving raw officer testimony verbatim, and automated headless Playwright DOM/WCAG verification prevents dark-slate UI clones or clipped controls from ever reaching builds.

---

## How the AI Stack Connects Directly to Shipped Systems

| Cognitive Layer / Mechanism | Production Guarantee Delivered Across Products | Primary Reference |
| :--- | :--- | :--- |
| **SSOT Native Agents & Lifecycle Hooks** | `squadron.json` → `18` `agents/*.md` (`-82.6%` roster, `commandExecutionPolicy: off`, `skills: []`) + **`204` hook tests** (`>400→350L` read clamp, `--reporter=dot`, OOM `flock` & Air-Gap) | [01 · The 18-Specialist Squadron](02_AI-Systems-Architecture/01-The-18-Specialist-Squadron.md) |
| **Optane FTS5 + Hybrid RRF (`k = 60`)** | `<100 ms` `<= 4 KB` sharded symbol maps, `<= 3.5 KB` blackboard & `<1.5 ms` recall of WebKit, FLSA `29 C.F.R. § 778.115` & `pnpm` fixes | [02 · Five-Tier Memory & Hybrid RRF](02_AI-Systems-Architecture/02-Five-Tier-Memory-and-Hybrid-RRF.md) |
| **18-Upgrade Context & Quota Governance** | `11.5 KB` rules (`-45.6%`), `4 → 1` MCP prune & `<=2,000`-token dispatches delivering **~20× token reduction (`80.5m` / `~1.38M` tok / `0` quota walls)** | [03 · Differential Context & Quota](02_AI-Systems-Architecture/03-Differential-Context-and-Quota-Governance.md) |
| **Two-Node Dropzone + Schema-Locked AI** | Catches PA/DE/MD statutory & Safari `<dialog>` traps pre-code; preserves immutable raw testimony & mandatory Wave 3 Break-It Audits (`0 CRIT/HIGH`) | [04 · Adversarial & Fact-Locked AI](02_AI-Systems-Architecture/04-Adversarial-Verification-and-Fact-Locked-AI.md) |
| **Chained Git, Tree Stamps & `30/30` Doctor** | Scoped Anti-Slop pre-commit, consume-once `HEAD^{tree}` (`0700`, `60s` TTL) stamps, `24/24` Pro rulesets, `30/30` doctor (w/ stale-model hygiene) & off-box DR | [05 · Autonomous DevOps & Gates](02_AI-Systems-Architecture/05-Autonomous-DevOps-and-Zero-Trust-Gates.md) |
| **Kernel `inotify` + Tuned Local Inference** | Turns mobile captures into routed tasks at `0 MB` idle RAM & runs `qwen3:8b` (`4.8 GB` / `37 tok/s`) co-resident w/ pinned `nomic-embed-text` (`0` evictions, `0 MB` swap) | [06 · Mobile Dispatch & Local LLM](02_AI-Systems-Architecture/06-Ambient-Mobile-Dispatch-and-Local-Inference.md) |

---

## Verified Quantitative Snapshot

- **Arclight Security (`v0.7.1` Sprint 2 + Wave 0 + Sprint 2.5):** **`1,098/1,098` automated tests** (`670` unit, `394` Vitest E2E, `34` Playwright browser E2E across `1440px` desktop & `375px` mobile), **`42` Gen-2 Cloud Functions (`enforceAppCheck: true`)**, **`0` `oxlint` warnings/errors across `360` files**, **`474.9 KB` max JS chunk (`<500 KB`)**, Wave 0 state decomposition (`10,895 → 421` LOC web + `12` slices; `5,583 → 384` LOC mobile + `7` slices), clean production provisioning + `orgMode` immutability lock, and **`0 CRITICAL / 0 HIGH`** across **`3` independent adversarial break-it rounds**.
- **SonoPrep Pro (`iOS`):** `421` audited RVT/SPI questions, `132` SVGs, `18` interactive hotspots, `34/34` unit/App Store compliance tests, `15/15` E2E stages, `0` `oxlint` warnings, `<500 KB` bundles.
- **Deterministic Video Engine (`v0.1.0`):** `4/4` packages typecheck clean; **`33/33` pipeline unit tests**; `17/17` seeded episodes clearing the 9-rule Grade `6.6–9.0` anti-slop voice gate; `1080×1920` `60fps` H.264 + `-14 LUFS` AAC stereo; `<35 KB` companion bio hubs.
- **18-Upgrade Engineering ROI & Fleet Governance:** **`11.5 KB` global rules** (`-45.6%` from `21.0 KB`), **`-82.6%` compact roster**, progressive-disclosure skills, **`<= 3.5 KB` active blackboard**, **`4 → 1` global MCP prune**, **`204` lifecycle hook tests** (`>400→350L` read clamp, `--reporter=dot`, scoped Anti-Slop, consume-once `HEAD^{tree}` `0700` `60s` tree stamps), `<100 ms` `<= 4 KB` sharded symbol maps, Flash-Attention + `q8_0` KV + `8K`-cap Apple Silicon co-residency (`qwen3:8b` `4.8 GB` / `37 tok/s` + pinned `nomic-embed-text`, `0` evictions, `0 MB` swap), **`24/24` zero-bypass GitHub Pro Rulesets** across `12` repos, **`30/30 PASS`** diagnostic doctor (w/ stale-model hygiene), and verified **~20× production token reduction** (**`80.5m`**, **`~1.38M` est tokens** across `20` runs, **`0` quota walls** vs `~29.6M` raw read tokens across `2` resets).

---

## Three-Node Compute Allocation Summary

| Node Role | Hardware Profile | Dedicated Workloads | Endurance & Protection Model |
| :--- | :--- | :--- | :--- |
| **Workstation Node** | 4C/8T Laptop · `12 GB` RAM + `11.4 GB` zram · **Optane NVMe Scratch** | Auto-hydrated Optane `fleet wt` worktrees, `hooks.json` (`204` tests), `<100 ms` `<= 4 KB` symbol maps, `memory.db` WAL FTS5 (`1.29 ms`), `ccache`/Rust/Node caches, `inotify` dispatch triggers | `vm.vfs_cache_pressure=50`, `[none]` I/O scheduler, `earlyoom`, `fcntl.flock` heavy-build serialization (`15m` TTL), 24/7 no-sleep & Wi-Fi `power_save=0` |
| **Inference & Backup Node** | Always-On Unified-Memory **Apple Silicon M1 Max (`32 GB`)** | Tuned Ollama (`OLLAMA_FLASH_ATTENTION=1`, `q8_0` KV, `8K` cap): **`qwen3:8b` (`4.8 GB` / `37 tok/s`) + pinned `nomic-embed-text`** + `14B` tiers, containers, iOS builds, 4-step DR verification | **`0` evictions · `0 MB` swap**; `launchd` container & `300s` vector watchdogs; `0` cloud tokens burned locally |
| **Edge Network Node** | `8 GB` **ARM SBC** | Primary network DNS filter + unified plain-English control telemetry HUD | Volatile RAM `journald`, `noatime,commit=60` mount, `300s` SQLite flush batching |

---

## Complete Documentation Map (`19` Chapters)

### 01 · Shipped Products & Hardware Systems (`5`)
- [Arclight Security ERP & CAD](01_Products/Arclight-Security-ERP.md) — Replacing the 4-vendor contract security stack across MD/DE/PA (`v0.7.1`: Sprint 2 watchdogs/anti-spoof/QBR, Wave 0 modular state slices, Sprint 2.5 clean production onboarding & `orgMode` lock, `1,098/1,098` tests, `42` Gen-2 App-Check functions).
- [SonoPrep Pro (iOS)](01_Products/SonoPrep-iOS.md) — Commercial ARDMS RVT/SPI vascular board prep with a 100% On-Device Study Vault and live Doppler physics simulation.
- [Deterministic Programmatic Video Production Engine](01_Products/Deterministic-Video-Production-Engine.md) — Multi-channel `1080×1920` `60fps` Remotion composition, `-14 LUFS` FFmpeg mastering, Grade `6.6–9.0` anti-slop voice gate, and idempotent publishing.
- [High-Velocity Retail Floor & Asset PWAs](01_Products/Retail-Operations-PWAs.md) — Single-handed mobile custody and execution tooling built for `<35ms` barcode wedges and instant NFC cold starts.
- [Parametric Additive CAD & Hardware Fixtures](01_Products/Additive-CAD-and-Hardware-Fixtures.md) — OpenSCAD CSG mounts, cantilever snap-fits, and pause-at-layer embedded RFID/NFC enclosures.

### 02 · AI Systems Architecture (7-Chapter Flagship Series)
- [00 · Cognitive Architecture Overview](02_AI-Systems-Architecture/00-Cognitive-Architecture-Overview.md) — Why single-context coding collapses and how `Halcyon` (XO) orchestrates 18 specialists across 3 compute nodes.
- [01 · The 18-Specialist Squadron](02_AI-Systems-Architecture/01-The-18-Specialist-Squadron.md) — Single-source `squadron.json` (`-82.6%` compact roster → `18` native `agents/*.md`), `4-Wave` OOM-safe doctrine with Wave 3 Adversarial Break-It Passes (`Sentinel` + `Aegis` → `0 CRIT/HIGH`), and `Tier A1/A2/B/C/D` audits.
- [02 · Five-Tier Memory & Hybrid RRF Retrieval](02_AI-Systems-Architecture/02-Five-Tier-Memory-and-Hybrid-RRF.md) — `<100 ms` `<= 4 KB` sharded symbol maps, `<= 3.5 KB` `fcntl.flock` rolling blackboards, progressive-disclosure skills, FTS5 BM25 + 14-day recency, and `k = 60` Reciprocal Rank Fusion.
- [03 · Differential Context & Quota Governance](02_AI-Systems-Architecture/03-Differential-Context-and-Quota-Governance.md) — `<= 2,000`-token compiler, 18-upgrade static prompt tax cuts (`11.5 KB` rules, `4 → 1` MCP prune), **`204` lifecycle hook tests**, 27-model routing, and the **~20× production token benchmark** (`80.5m`, `~1.38M` est tok, `0` quota walls).
- [04 · Adversarial Verification & Fact-Locked AI](02_AI-Systems-Architecture/04-Adversarial-Verification-and-Fact-Locked-AI.md) — Two-node adversarial research (`Scout` ↔ `Muse`) and schema-locked, raw-transcript-preserving production AI.
- [05 · Autonomous DevOps & Zero-Trust Gates](02_AI-Systems-Architecture/05-Autonomous-DevOps-and-Zero-Trust-Gates.md) — Auto-hydrated Optane `fleet wt` worktrees, `<5ms` blob/secret & scoped Anti-Slop hooks, consume-once `HEAD^{tree}` (`0700`, `60s` TTL) tree stamps, **`24/24` zero-bypass Pro Rulesets**, **`30/30` diagnostic doctor**, and DR restores.
- [06 · Ambient Mobile Dispatch & Local Inference](02_AI-Systems-Architecture/06-Ambient-Mobile-Dispatch-and-Local-Inference.md) — Zero-RAM `inotify` inbox triggers and Flash-Attention + `q8_0` KV + `8K`-cap Apple Silicon co-residency (`qwen3:8b` `4.8 GB` / `37 tok/s` + pinned `nomic-embed-text`, `0` evictions, `0 MB` swap).

### 03 · Systems & UI Deep Dives
- [Half-Duplex Push-to-Talk Over LTE](03_Architecture-Deep-Dives/Half-Duplex-PTT-Over-LTE.md) — Lease-backed floor locks, `10-33 SOS` preemption, synthesized radio chirps, and LiveKit + dead-zone replay.
- [Statutory Compliance as Deterministic Code](03_Architecture-Deep-Dives/Statutory-Compliance-As-Code.md) — MD/DE/PA evaluators, integer-cents FLSA `29 C.F.R. § 778.115` overtime, and Dark-Hours SLA liquidation math.
- [Zero-Clobber Real-Time Synchronization](03_Architecture-Deep-Dives/Zero-Clobber-Realtime-Sync.md) — Atomic `runTransaction` per-entity timestamp merging, `750 KB` log pruning ahead of `1 MiB` caps, and FIFO outboxes.
- [Anti-Slop UI Engineering & WebKit Resilience](03_Architecture-Deep-Dives/Anti-Slop-UI-Engineering.md) — Domain archetypes, `OKLCH` + `color-mix()` tokens, native `<dialog>` coordinate guards, and Safari platform fixes.

### 04 · Engineering Build Log
- [November 2026 Engineering Milestones](04_Build-Log/2026-11-Milestones.md) — Verified production benchmarks, test counts, and platform releases.
