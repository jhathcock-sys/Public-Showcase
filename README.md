---
title: Hathcock Labs — Public Engineering & Product Documentation
description: Authoritative public documentation book covering Hathcock Labs' AI multi-agent engineering architecture, regulated security ERP, iOS clinical exam preparation, retail hardware PWAs, and parametric CAD systems.
tags:
  - documentation
  - architecture
  - ai-systems
  - portfolio
  - hathcock-labs
updated: 2026-11-17
---

# Hathcock Labs — Engineering & Product Documentation Showcase

Welcome to the public engineering knowledgebase for **Hathcock Labs**. This repository serves as a deep, readable architectural manual covering how we design, verify, and ship production software for high-consequence environments—alongside our flagship **7-part AI Systems Architecture series** detailing how 18 domain-specialized engineering agents, sub-millisecond hybrid memory, differential context compilation, and zero-trust DevOps gates work in concert under human architectural control.

> [!NOTE]
> **Universal Format:** Browse directly on **GitHub**, open the folder as a standalone **Obsidian** vault, or publish as a static documentation site with **Quartz v4**. Every cross-reference uses standard relative Markdown links.

---

## Engineering Highlights at a Glance

- **18 Partitioned Domain Specialists (`02_AI-Systems-Architecture/`):** Explicit inter-agent boundary seams (e.g., `Prism` visual aesthetics vs. `Forge` `100dvh` & `<500 KB` bundle budgets; read-only `Echo` clinical verification vs. `Aegis` code refactoring), lazy `SKILL.md` runbook injection, and programmatic **`pro [MANDATORY]`** frontier locks on security, clinical, auth, and sync code.
- **Sub-`1.5 ms` Optane Memory & Hybrid RRF (`k = 60`):** Replaces `50k+`-token file dumps with `<1.5 KB` `REPO_MAP.md` structural navigation, `fcntl.flock` rolling `8`-entry blackboards (`93%` init reduction), Optane SQLite WAL FTS5 BM25 + 14-day recency, and asynchronous `768d` vectors computed at **`0` cloud tokens** on Apple Silicon.
- **Deterministic Context & Quota Governance:** Enforces `<= 2,000`-token subagent dispatches via an `8`-step trim ladder and unfenced code-dump detection (`>80` lines -> `exit 1`), paired with real-time `5-hour` (`100M`, 25%-load rolloff countdown) and `7-day` (`500M`, `0.025x` cache, `0.55x` medium) rolling quota gauges inside an ANSI-safe terminal HUD.
- **Zero-Trust Verification & Drift Readiness:** Sub-`50ms` secret/lint pre-commit hooks, monorepo pre-push type/test chains, Playwright DOM/WCAG visual verification, 22-invariant 3-node drift inspection (`<3.5s`), and 4-step sandbox-verified SQLite DR restores.
- **Production Software Across Three Physical Domains:** Tri-State security ERP (`205/205` tests passing across `5` workspace packages), App Store-ready iOS vascular exam prep (`421` clinical items, `34/34` unit + `15/15` E2E), hardware-wedge `<35ms` stockroom PWAs, and parametric OpenSCAD pause-at-layer RFID/NFC enclosures.

---

## Recommended Reading Tracks

### Track A · AI & Systems Engineers (Start Here for Multi-Agent Architecture)
If you came for how we avoid LLM context rot, hallucinations, and runaway token burn across real multi-package production repositories:
1. [00 · Cognitive Architecture Overview](02_AI-Systems-Architecture/00-Cognitive-Architecture-Overview.md) — Why single-context chat coding collapses and how our 3-node heterogeneous topology separates compute cleanly.
2. [01 · The 18-Specialist Squadron](02_AI-Systems-Architecture/01-The-18-Specialist-Squadron.md) — Profiles of all 18 domain roles, inter-agent seams, zero-mention intent routing, lazy `SKILL.md` loading, and tiered release audits.
3. [02 · Five-Tier Memory & Hybrid RRF Retrieval](02_AI-Systems-Architecture/02-Five-Tier-Memory-and-Hybrid-RRF.md) — `<1.5 ms` Optane SQLite FTS5 BM25 + 14-day recency fused via Reciprocal Rank Fusion (`k = 60`) with `768d` local vectors.
4. [03 · Differential Context & Quota Governance](02_AI-Systems-Architecture/03-Differential-Context-and-Quota-Governance.md) — Deterministic `<= 2,000`-token context compiler, 8-step trim ladder, anti-dump detectors, mandatory frontier locks, and live HUD math.
5. [04 · Adversarial Verification & Fact-Locked AI](02_AI-Systems-Architecture/04-Adversarial-Verification-and-Fact-Locked-AI.md) — Two-node adversarial research (`Scout` ↔ `Muse`) and temperature-zero schema-locked production AI.
6. [05 · Autonomous DevOps & Zero-Trust Gates](02_AI-Systems-Architecture/05-Autonomous-DevOps-and-Zero-Trust-Gates.md) — Sub-50ms secret/lint hooks, pre-push `tsc` + `vitest`, Playwright DOM/WCAG gating, 22-check 3-node drift doctor, and verified DR restores.
7. [06 · Ambient Mobile Dispatch & Local Inference](02_AI-Systems-Architecture/06-Ambient-Mobile-Dispatch-and-Local-Inference.md) — Zero-RAM kernel `inotify` triggers, automatic `hermes3:8b` JSON dispatch triage, and the 5-model `squad-local` M1 Max zero-token CLI.

### Track B · Product & Enterprise Architecture Reviewers
Explore the real-world systems built with this toolchain:
- [Arclight Security ERP & CAD](01_Products/Arclight-Security-ERP.md) — Multi-tenant Tri-State (`MD`, `DE`, `PA`) security guard ERP replacing the 4-vendor Frankenstack.
- [SonoPrep Pro (iOS)](01_Products/SonoPrep-iOS.md) — Commercial ARDMS RVT/SPI vascular board prep with a 100% On-Device Study Vault and real-time Doppler simulation.
- [High-Velocity Retail Floor & Asset PWAs](01_Products/Retail-Operations-PWAs.md) — Phone-first hardware custody & execution tooling engineered for `<35ms` laser scanner wedges and flaky stockrooms.
- [Parametric Additive CAD & Hardware Fixtures](01_Products/Additive-CAD-and-Hardware-Fixtures.md) — OpenSCAD CSG mounts, compliant cantilever snap-fits, and pause-at-layer embedded RFID/NFC enclosures.

### Track C · Systems Deep Dives & Release History
- [Half-Duplex Push-to-Talk Over LTE](03_Architecture-Deep-Dives/Half-Duplex-PTT-Over-LTE.md)
- [Statutory Compliance as Deterministic Code](03_Architecture-Deep-Dives/Statutory-Compliance-As-Code.md)
- [Zero-Clobber Real-Time Synchronization](03_Architecture-Deep-Dives/Zero-Clobber-Realtime-Sync.md)
- [Anti-Slop UI Engineering & WebKit Resilience](03_Architecture-Deep-Dives/Anti-Slop-UI-Engineering.md)
- [November 2026 Engineering Milestones](04_Build-Log/2026-11-Milestones.md)

---

## Complete Vault Index

| Section | Chapters | Focus |
| :--- | :---: | :--- |
| **Root** | `2` | [README](README.md) · [Vault Home (`index.md`)](index.md) |
| **01 · Products** | `4` | [Arclight Security ERP](01_Products/Arclight-Security-ERP.md) · [SonoPrep iOS](01_Products/SonoPrep-iOS.md) · [Retail Operations PWAs](01_Products/Retail-Operations-PWAs.md) · [Additive CAD & Fixtures](01_Products/Additive-CAD-and-Hardware-Fixtures.md) |
| **02 · AI Systems Architecture** | `7` | [Overview](02_AI-Systems-Architecture/00-Cognitive-Architecture-Overview.md) · [18 Specialists](02_AI-Systems-Architecture/01-The-18-Specialist-Squadron.md) · [5-Tier Memory & RRF](02_AI-Systems-Architecture/02-Five-Tier-Memory-and-Hybrid-RRF.md) · [Context & Quota](02_AI-Systems-Architecture/03-Differential-Context-and-Quota-Governance.md) · [Adversarial & Fact-Locked AI](02_AI-Systems-Architecture/04-Adversarial-Verification-and-Fact-Locked-AI.md) · [DevOps & Zero-Trust Gates](02_AI-Systems-Architecture/05-Autonomous-DevOps-and-Zero-Trust-Gates.md) · [Mobile Dispatch & Local LLM](02_AI-Systems-Architecture/06-Ambient-Mobile-Dispatch-and-Local-Inference.md) |
| **03 · Architecture Deep Dives** | `4` | [Half-Duplex PTT](03_Architecture-Deep-Dives/Half-Duplex-PTT-Over-LTE.md) · [Statutory Compliance](03_Architecture-Deep-Dives/Statutory-Compliance-As-Code.md) · [Zero-Clobber Sync](03_Architecture-Deep-Dives/Zero-Clobber-Realtime-Sync.md) · [Anti-Slop UI & WebKit](03_Architecture-Deep-Dives/Anti-Slop-UI-Engineering.md) |
| **04 · Build Log** | `1` | [November 2026 Milestones](04_Build-Log/2026-11-Milestones.md) |

---

## Target Audience Guide

| Reader Focus | Suggested Path | What You Will Find |
| :--- | :--- | :--- |
| **AI Systems Architects & Tool Builders** | `02_AI-Systems-Architecture/00` through `06` | Token-governed multi-agent execution, Optane FTS5/RRF retrieval, POSIX locking, adversarial verification, and zero-cost Apple Silicon vector offloading. |
| **Enterprise & Regulated Product Engineers** | `01_Products/Arclight-Security-ERP.md` + `03_Architecture-Deep-Dives/*` | Multi-tenant Firestore boundaries, FLSA `29 C.F.R. § 778.115` integer-cents payroll math, Tri-State compliance evaluators, and half-duplex WebRTC PTT. |
| **Mobile, Clinical & Hardware Developers** | `SonoPrep-iOS.md`, `Retail-Operations-PWAs.md`, `Additive-CAD-and-Hardware-Fixtures.md` | App Store StoreKit 2 + Privacy manifests, `<35ms` HID scanner isolation, iOS WebKit audio lock recovery, and parametric pause-print CAD tolerances. |

---

## Public Release & Sanitization Guarantees

- **Viewing Options:** Open directly inside GitHub's native Markdown & Mermaid viewer, mount this directory locally as a standalone Obsidian vault, or deploy via Quartz v4 (`index.md` landing page).
- **Strict Air-Gap Sanitization:** This showcase contains zero proprietary credentials, API keys, RFC-1918 LAN IP ranges, local mDNS suffixes, workstation filesystem paths, personal/employee names, or private store identifiers. A standalone `.git/hooks/pre-commit` air-gap firewall validates every added diff line prior to staging and release.

---

## Core Engineering Benchmarks Summary

| System Pillar | Benchmark / Constraint | Mechanism Behind Guarantee |
| :--- | :--- | :--- |
| **Specialist Dispatch** | `<= 2,000` tokens / `<= 35` lines/slice | Deterministic `squad-context` compiler + `8`-step trim ladder |
| **Optane Knowledge Search** | `< 1.5 ms` lexical / `< 300` tokens | SQLite WAL FTS5 BM25 (`5:2:1`) + `14d` recency + `k=60` RRF |
| **Blackboard Concurrency** | `8` active entries (`~93%` init reduction) | Re-entrant POSIX `fcntl.flock` + lossless cold archival |
| **Local Open-Weight Offload** | `0` cloud tokens (`5`-model M1 Max CLI) | `squad-local`: `nomic-embed-text`, `hermes3:8b`, `qwen2.5-coder:14b`, `deepseek-r1:14b`, `qwen3:14b` |
| **Pre-Commit & Pre-Push** | `< 50 ms` commit / `< 15s` push | Staged diff secret regex, `oxlint`, `tsc --noEmit` & `vitest` |
| **Infrastructure Health** | `22/22` checks in `< 3.5 seconds` | Parallel 3-node drift probe + 4-step sandboxed DR restore proof |
