---
title: Hathcock Labs — Public Engineering & Product Documentation
description: Authoritative public documentation book covering Hathcock Labs' AI multi-agent engineering architecture, regulated security ERP, iOS clinical exam preparation, retail hardware PWAs, and parametric CAD systems.
tags:
  - documentation
  - architecture
  - ai-systems
  - portfolio
  - hathcock-labs
updated: 2026-11-18
---

# Hathcock Labs — Engineering & Product Documentation Showcase

Welcome to the public engineering knowledgebase for **Hathcock Labs** (**19 chapters** across products, AI cognitive infrastructure, systems deep dives, and milestone logs). This repository serves as a deep architectural manual covering how we design, verify, and ship production software for high-consequence environments—anchored by our flagship **7-part AI Systems Architecture series** detailing how **`Halcyon` (XO & Flight Director)**, **18 domain-specialized engineering agents**, external auditor **`Muse`**, sub-millisecond hybrid memory, differential context compilation, and **`24/24` zero-bypass rulesets** work in concert under human architectural control.

> [!NOTE]
> **Universal Format:** Browse directly on **GitHub**, open the folder as a standalone **Obsidian** vault, or publish as a static documentation site with **Quartz v4**. Every cross-reference uses standard relative Markdown links.

---

## Engineering Highlights at a Glance

- **`Halcyon` XO + 18 Partitioned Domain Specialists (`02_AI-Systems-Architecture/`):** Explicit boundary seams (`Prism` OKLCH aesthetics vs. `Forge` PWA/Capacitor/Expo native packaging; read-only `Echo` clinical & `Scout` statutory veto power; `Hermes` private-vault-only isolation vs. `Scribe` air-gap skill firewall), **`Tier A1/A2/B/C/D` audit matrices**, and a **`4-Wave` OOM-safe execution doctrine** preventing concurrent bundler/Chromium swaps on `12 GB` RAM.
- **Sub-`1.5 ms` Optane Memory & Hybrid RRF (`k = 60`):** Replaces `50k+`-token file dumps with `<1.5 KB` `REPO_MAP.md` structural navigation, `fcntl.flock` rolling `8`-entry blackboards (`93%` init reduction), Optane SQLite WAL FTS5 BM25 + 14-day recency (`996/996` vector parity), and `768d` vectors + 5-model `squad-local` inference at **`0` cloud tokens** on Apple Silicon.
- **Dual-Model Routing & Fixed-Bucket Quota Governance:** Enforces `<= 2,000`-token subagent dispatches (`8`-step trim ladder + unfenced code-dump rejection), pairs `Orchestrator (Argon/Carbon)` with `Gemini 4 Hydrogen` (`57%` Terminal-Bench 4.1, `-24%` quota, `-19%` latency), and monitors calibrated **`32.5M` fixed 5-hour buckets** / **`195M` 7-day rolling caps** anchored to live `/usage` headers (`XX% LIVE`, isolated `Cld:XX%`).
- **Optane Worktrees, `24/24` Zero-Bypass Rulesets & `23/23` Drift Readiness:** Isolates active development inside `fleet wt` worktrees, gates every commit under `<5 ms` (`>2 MB` blob / media / SQLite / secret + 5-Category Air-Gap Firewall), locks **12 repositories** under **`24/24` zero-bypass GitHub Pro `trunk-immutable` & `tags-immutable` Rulesets**, ships `<5s` linear-forward `fleet release` / `fleet rollback`, and audits **`23/23`** 3-node invariants in **`0.55s`**.
- **Production Systems Across Regulated & Media Domains:** Tri-State security ERP + live PTT (`v0.4.0`: `433/433` unit, `164/164` E2E, `19` Blaze functions, `457.24 kB` max chunk), App Store-ready iOS vascular board prep (`421` items, `34/34` unit + `15/15` E2E), programmatic `1080×1920` `60fps` `-14 LUFS` short-form video engine (`33/33` unit, Grade `6.6–9.0`), `<35ms` floor hardware PWAs, and parametric OpenSCAD NFC enclosures.

---

## Recommended Reading Tracks

### Track A · AI & Systems Engineers (Start Here for Multi-Agent Architecture)
If you came for how we avoid LLM context rot, hallucinations, and runaway token burn across real multi-package production repositories:
1. [00 · Cognitive Architecture Overview](02_AI-Systems-Architecture/00-Cognitive-Architecture-Overview.md) — Why single-context chat coding collapses and how our 3-node heterogeneous topology separates compute cleanly.
2. [01 · The 18-Specialist Squadron](02_AI-Systems-Architecture/01-The-18-Specialist-Squadron.md) — Profiles of all 18 domain roles, inter-agent seams, zero-mention intent routing, lazy `SKILL.md` loading, and tiered release audits.
3. [02 · Five-Tier Memory & Hybrid RRF Retrieval](02_AI-Systems-Architecture/02-Five-Tier-Memory-and-Hybrid-RRF.md) — `<1.5 ms` Optane SQLite FTS5 BM25 + 14-day recency fused via Reciprocal Rank Fusion (`k = 60`) with `768d` local vectors.
4. [03 · Differential Context & Quota Governance](02_AI-Systems-Architecture/03-Differential-Context-and-Quota-Governance.md) — `<= 2,000`-token compiler, `Gemini 4 Hydrogen` + `Orchestrator` routing, and calibrated `32.5M`/`195M` fixed `/usage` gauges.
5. [04 · Adversarial Verification & Fact-Locked AI](02_AI-Systems-Architecture/04-Adversarial-Verification-and-Fact-Locked-AI.md) — Two-node adversarial research (`Scout` ↔ `Muse`) and temperature-zero schema-locked production AI.
6. [05 · Autonomous DevOps & Zero-Trust Gates](02_AI-Systems-Architecture/05-Autonomous-DevOps-and-Zero-Trust-Gates.md) — Optane worktrees (`fleet wt`), `<5ms` blob/secret hooks, **`24/24` zero-bypass Pro Rulesets** across `12` repos, **`23/23` `squad-doctor` (`0.55s`)**, and verified DR restores.
7. [06 · Ambient Mobile Dispatch & Local Inference](02_AI-Systems-Architecture/06-Ambient-Mobile-Dispatch-and-Local-Inference.md) — Zero-RAM kernel `inotify` triggers, automatic `hermes3:8b` JSON dispatch triage, and the 5-model `squad-local` M1 Max zero-token CLI.

### Track B · Product & Enterprise Architecture Reviewers
Explore the real-world systems built with this toolchain:
- [Arclight Security ERP & CAD](01_Products/Arclight-Security-ERP.md) — Multi-tenant Tri-State (`MD`, `DE`, `PA`) security guard ERP + live PTT (`v0.4.0`: `433` unit + `164` E2E + `19` Blaze functions).
- [SonoPrep Pro (iOS)](01_Products/SonoPrep-iOS.md) — Commercial ARDMS RVT/SPI vascular board prep with a 100% On-Device Study Vault and real-time Doppler simulation.
- [Deterministic Programmatic Video Production Engine](01_Products/Deterministic-Video-Production-Engine.md) — Multi-channel `1080×1920` `60fps` Remotion + `-14 LUFS` FFmpeg pipeline with Grade `6.6–9.0` anti-slop voiceover verification.
- [High-Velocity Retail Floor & Asset PWAs](01_Products/Retail-Operations-PWAs.md) — Phone-first hardware custody & execution tooling engineered for `<35ms` laser scanner wedges and flaky stockrooms.
- [Parametric Additive CAD & Hardware Fixtures](01_Products/Additive-CAD-and-Hardware-Fixtures.md) — OpenSCAD CSG mounts, compliant cantilever snap-fits, and pause-at-layer embedded RFID/NFC enclosures.

### Track C · Systems Deep Dives & Release History
- [Half-Duplex Push-to-Talk Over LTE](03_Architecture-Deep-Dives/Half-Duplex-PTT-Over-LTE.md)
- [Statutory Compliance as Deterministic Code](03_Architecture-Deep-Dives/Statutory-Compliance-As-Code.md)
- [Zero-Clobber Real-Time Synchronization](03_Architecture-Deep-Dives/Zero-Clobber-Realtime-Sync.md)
- [Anti-Slop UI Engineering & WebKit Resilience](03_Architecture-Deep-Dives/Anti-Slop-UI-Engineering.md)
- [November 2026 Engineering Milestones](04_Build-Log/2026-11-Milestones.md)

---

## Complete Vault Index (`19` Chapters)

| Section | Chapters | Focus |
| :--- | :---: | :--- |
| **Root** | `2` | [README](README.md) · [Vault Home (`index.md`)](index.md) |
| **01 · Products** | `5` | [Arclight Security ERP](01_Products/Arclight-Security-ERP.md) · [SonoPrep iOS](01_Products/SonoPrep-iOS.md) · [Video Production Engine](01_Products/Deterministic-Video-Production-Engine.md) · [Retail Operations PWAs](01_Products/Retail-Operations-PWAs.md) · [Additive CAD & Fixtures](01_Products/Additive-CAD-and-Hardware-Fixtures.md) |
| **02 · AI Systems Architecture** | `7` | [Overview](02_AI-Systems-Architecture/00-Cognitive-Architecture-Overview.md) · [Halcyon & 18 Specialists](02_AI-Systems-Architecture/01-The-18-Specialist-Squadron.md) · [5-Tier Memory & RRF](02_AI-Systems-Architecture/02-Five-Tier-Memory-and-Hybrid-RRF.md) · [Context & Quota](02_AI-Systems-Architecture/03-Differential-Context-and-Quota-Governance.md) · [Adversarial & Fact-Locked AI](02_AI-Systems-Architecture/04-Adversarial-Verification-and-Fact-Locked-AI.md) · [DevOps & Pro Rulesets](02_AI-Systems-Architecture/05-Autonomous-DevOps-and-Zero-Trust-Gates.md) · [Mobile Dispatch & Local LLM](02_AI-Systems-Architecture/06-Ambient-Mobile-Dispatch-and-Local-Inference.md) |
| **03 · Architecture Deep Dives** | `4` | [Half-Duplex PTT](03_Architecture-Deep-Dives/Half-Duplex-PTT-Over-LTE.md) · [Statutory Compliance](03_Architecture-Deep-Dives/Statutory-Compliance-As-Code.md) · [Zero-Clobber Sync](03_Architecture-Deep-Dives/Zero-Clobber-Realtime-Sync.md) · [Anti-Slop UI & WebKit](03_Architecture-Deep-Dives/Anti-Slop-UI-Engineering.md) |
| **04 · Build Log** | `1` | [November 2026 Milestones](04_Build-Log/2026-11-Milestones.md) |

---

## Target Audience Guide

| Reader Focus | Suggested Path | What You Will Find |
| :--- | :--- | :--- |
| **AI Systems Architects & Tool Builders** | `02_AI-Systems-Architecture/00` through `06` | `Halcyon` XO + `4-Wave` orchestration, Optane FTS5/RRF retrieval, `32.5M`/`195M` `/usage` telemetry, `24/24` GitHub Pro rulesets, and `squad-local` offloading. |
| **Enterprise & Regulated Product Engineers** | `01_Products/Arclight-Security-ERP.md` + `03_Architecture-Deep-Dives/*` | Multi-tenant Firestore boundaries, FLSA / `34 Pa. Code § 231.43(d)(2)` integer-cents math, SHA-256 license checks, and live WebRTC PTT with wiretap carve-outs. |
| **Mobile, Media, Clinical & Hardware Developers** | `SonoPrep-iOS.md`, `Deterministic-Video-Production-Engine.md`, `Retail-Operations-PWAs.md`, `Additive-CAD-and-Hardware-Fixtures.md` | App Store StoreKit 2 manifests, `-14 LUFS` Remotion rendering, `<35ms` HID scanner isolation, iOS WebKit audio lock recovery, and pause-print CAD tolerances. |

---

## Public Release & Sanitization Guarantees

- **Viewing Options:** Open directly inside GitHub's native Markdown & Mermaid viewer, mount this directory locally as a standalone Obsidian vault, or deploy via Quartz v4 (`index.md` landing page).
- **Strict Air-Gap Sanitization:** This showcase contains zero proprietary credentials, API keys, RFC-1918 LAN IP ranges, local mDNS suffixes, workstation filesystem paths, personal/employee names, channel handles, or private store identifiers. A standalone pre-commit air-gap firewall validates every added diff line prior to staging and release.

---

## Core Engineering Benchmarks Summary

| System Pillar | Benchmark / Constraint | Mechanism Behind Guarantee |
| :--- | :--- | :--- |
| **Specialist Dispatch** | `<= 2,000` tokens / `<= 35` lines/slice | Deterministic `squad-context` compiler + `8`-step trim ladder |
| **Optane Knowledge Search** | `1.29 ms` lexical / `996/996` vector parity | SQLite WAL FTS5 BM25 (`5:2:1`) + `14d` recency + `k=60` RRF |
| **Quota & Dual-Model Coding** | `32.5M` 5h / `195M` 7d · `-24%` burn / `-19%` time | `Orchestrator (Argon/Carbon)` + `Gemini 4 Hydrogen` + `/usage` live lock |
| **Local Open-Weight Offload** | `0` cloud tokens (`5`-model M1 Max CLI) | `squad-local`: `nomic-embed-text`, `hermes3:8b`, `qwen2.5-coder:14b`, `deepseek-r1:14b`, `qwen3:14b` |
| **Pre-Commit, Rulesets & Releases** | `< 5 ms` hook · `24/24` Pro Rulesets (`12` repos) | Blob/media/secret guard (`13/13`), `pre-push` (`5/5`), `<5s` `fleet release` / `rollback` |
| **Infrastructure Health** | **`23/23` invariants in `0.55s`** | Parallel 3-node probe (incl. 24/7 no-sleep & Wi-Fi lock) + 4-step DR restore proof |
