---
title: Hathcock Labs — Public Engineering & Product Documentation
description: Authoritative public documentation book covering Hathcock Labs' AI multi-agent engineering architecture, regulated security ERP, iOS clinical exam preparation, retail hardware PWAs, and parametric CAD systems.
tags:
  - documentation
  - architecture
  - ai-systems
  - portfolio
  - hathcock-labs
updated: 2026-11-22
---

# Hathcock Labs — Engineering & Product Documentation Showcase

Welcome to the public engineering knowledgebase for **Hathcock Labs** (**19 chapters** across products, AI cognitive infrastructure, systems deep dives, and milestone logs). This repository serves as a deep architectural manual covering how we design, verify, and ship production software for high-consequence environments—anchored by our flagship **7-part AI Systems Architecture series** detailing how **`Halcyon` (XO & Flight Director)**, **18 domain-specialized engineering agents**, external auditor **`Muse`**, sub-millisecond hybrid memory, differential context compilation, and **`24/24` zero-bypass rulesets** work in concert under human architectural control.

> [!NOTE]
> **Universal Format:** Browse directly on **GitHub**, open the folder as a standalone **Obsidian** vault, or publish as a static documentation site with **Quartz v4**. Every cross-reference uses standard relative Markdown links.

---

## Engineering Highlights at a Glance

- **`Halcyon` XO + 18 Native Specialists (`02_AI-Systems-Architecture/`):** Driven by a single-source-of-truth **`squadron.json`** registry (`fleet sync-roster` → `18` natively discovered `agents/*.md` specs, eliminating 4-way config drift and per-session re-definition) with declarative read-only execution locks (`commandExecutionPolicy: off` on `Echo`/`Scout`), Lazy Skill Firewalls (`skills: []` on `Scribe`), **`Tier A1/A2/B/C/D` audit matrices**, and deterministic **`hooks.json`** (`65/65` subprocess tests, `16–28 ms`) enforcing **`4-Wave`** `fcntl.flock` OOM build serialization on `12 GB` RAM.
- **Sub-`1.5 ms` Optane Memory & `<24 KB` Rule Hygiene:** Deduplicated global rules from **`40.7 KB` → `20.4 KB`** (safely under the `24 KB` per-file injection cap so zero guardrails truncate on session boot) via a unified 18-agent roster table, `<1.5 KB` `REPO_MAP.md` maps, `fcntl.flock` rolling `8`-entry blackboards (`93%` init reduction), Optane SQLite WAL FTS5 BM25 + 14-day recency (**`1,015/1,015` embedded sections**), and `768d` vectors + 5-model `squad-local` inference at **`0` cloud tokens** on Apple Silicon.
- **27-Model Dual-Pool Routing & Calibrated Telemetry:** Enforces `<= 2,000`-token subagent dispatches (`8`-step trim ladder + unfenced code-dump rejection) across **27 live models** (`20` Pool 1 Gemini incl. **Gemini 4 Neon** & **Orchestrator Neon** + Hydrogen/Carbon/Argon/3.8 Flash; `7` Pool 2 Claude 5.5 + sunsetting GPT-OSS 120B). Combines runtime delegation (`inherit` → Neon High; `pro`/`flash` → Hydrogen `tiered-xhigh`/`tiered-high`) with explicit `/swarm` pinning (`gemini-4-neon-xhigh` & selective Pool 2 release gates), monitored via **`32.5M` fixed 5-hour buckets** / **`325M` 7-day rolling heuristics** (suppressing false alarms while Pool 1 is unthrottled), live `/usage` header locks (`XX% LIVE`), Pool 2 countdowns (`Cld:XX%/XdXXh`), child-transcript model tracking, and `0.35x` `Gemini 4 Low` tiering.
- **Auto-Hydrated Optane Worktrees, `24/24` Zero-Bypass Rulesets & `29/29` Integrity Doctor:** Isolates active development inside `fleet wt` worktrees with auto-hardlinked nested `functions/node_modules` and monorepo `packages/*/dist`, gates every commit under `<5 ms` (`>2 MB` blob / media / SQLite / secret + 5-Category Air-Gap Firewall), locks **12 repositories** under **`24/24` zero-bypass GitHub Pro `trunk-immutable` & `tags-immutable` Rulesets**, ships `<5s` linear-forward `fleet release` / `fleet rollback`, and verifies **`29/29`** cross-node & governance invariants via `squad-doctor`.
- **Production Systems Across Regulated & Media Domains:** Tri-State security ERP + live PTT (`v0.4.0`: `433/433` unit, `164/164` E2E, `19` Blaze functions, `457.24 kB` max chunk), App Store-ready iOS vascular board prep (`421` items, `34/34` unit + `15/15` E2E), programmatic `1080×1920` `60fps` `-14 LUFS` short-form video engine (`33/33` unit, Grade `6.6–9.0`), `<35ms` floor hardware PWAs, and parametric OpenSCAD NFC enclosures.

---

## Recommended Reading Tracks

### Track A · AI & Systems Engineers (Start Here for Multi-Agent Architecture)
If you came for how we avoid LLM context rot, hallucinations, and runaway token burn across real multi-package production repositories:
1. [00 · Cognitive Architecture Overview](02_AI-Systems-Architecture/00-Cognitive-Architecture-Overview.md) — Why single-context chat coding collapses and how our 3-node heterogeneous topology separates compute cleanly.
2. [01 · The 18-Specialist Squadron](02_AI-Systems-Architecture/01-The-18-Specialist-Squadron.md) — Profiles of all 18 domain roles, inter-agent seams, zero-mention intent routing, lazy `SKILL.md` loading, and tiered release audits.
3. [02 · Five-Tier Memory & Hybrid RRF Retrieval](02_AI-Systems-Architecture/02-Five-Tier-Memory-and-Hybrid-RRF.md) — `<1.5 ms` Optane SQLite FTS5 BM25 + 14-day recency fused via Reciprocal Rank Fusion (`k = 60`) with `768d` local vectors.
4. [03 · Differential Context & Quota Governance](02_AI-Systems-Architecture/03-Differential-Context-and-Quota-Governance.md) — `<= 2,000`-token compiler, 27-model `Gemini 4 Neon` + `Hydrogen` + `/swarm` routing, `<24 KB` rule hygiene, and calibrated `32.5M`/`325M` `/usage` telemetry.
5. [04 · Adversarial Verification & Fact-Locked AI](02_AI-Systems-Architecture/04-Adversarial-Verification-and-Fact-Locked-AI.md) — Two-node adversarial research (`Scout` ↔ `Muse`) and temperature-zero schema-locked production AI.
6. [05 · Autonomous DevOps & Zero-Trust Gates](02_AI-Systems-Architecture/05-Autonomous-DevOps-and-Zero-Trust-Gates.md) — Auto-hydrated Optane worktrees (`fleet wt`), `<5ms` blob/secret hooks, **`24/24` zero-bypass Pro Rulesets** across `12` repos, **`29/29` `squad-doctor`**, and verified DR restores.
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
| **AI Systems Architects & Tool Builders** | `02_AI-Systems-Architecture/00` through `06` | `Halcyon` XO + `squadron.json` native agents, `hooks.json` (`65/65`, `16–28 ms`), Optane FTS5/RRF (`1,015` sections), 27-model Neon/Hydrogen routing, `32.5M`/`325M` `/usage` telemetry, `29/29` doctor, `24/24` Pro rulesets, and `squad-local`. |
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
| **Constitutional Rule Budget** | `20.4 KB` (`<24 KB` cap; down from `40.7 KB`) | Unified 18-agent roster table + Optane memory offload; `0` boot truncation |
| **Optane Knowledge Search** | `1.29 ms` lexical / `1,015/1,015` vector parity | SQLite WAL FTS5 BM25 (`5:2:1`) + `14d` recency + `k=60` RRF |
| **27-Model Routing & Telemetry** | `32.5M` 5h / `325M` 7d est · `Cld:XX%/XdXXh` | `Gemini 4 Neon` + `Hydrogen` + `/swarm` pinning + child-transcript `/usage` lock |
| **Local Open-Weight Offload** | `0` cloud tokens (`5`-model M1 Max CLI) | `squad-local`: `nomic-embed-text`, `hermes3:8b`, `qwen2.5-coder:14b`, `deepseek-r1:14b`, `qwen3:14b` |
| **Lifecycle Hooks & Roster SSOT** | `16–28 ms` hooks (`65/65` tests) · `18` native `agents/*.md` | `hooks.json` (`flock` OOM / Air-Gap / tier floor) + `squadron.json` `fleet sync-roster` |
| **Pre-Commit, Rulesets & Releases** | `< 5 ms` hook · `24/24` Pro Rulesets (`12` repos) | Blob/media/secret guard (`13/13`), `pre-push` (`5/5`), auto-hydrated `fleet wt`, `<5s` `fleet release` |
| **Infrastructure & Governance Health** | **`29/29` automated invariants (`squad-doctor`)** | Parallel 3-node probe + `<22 KB` rule cap, symlink/archive/TTL/canonical-hook & roster parity |
