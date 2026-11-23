---
title: Hathcock Labs — Public Engineering & Product Documentation
description: Authoritative public documentation book covering Hathcock Labs' AI multi-agent engineering architecture, regulated security ERP, iOS clinical exam preparation, retail hardware PWAs, and parametric CAD systems.
tags:
  - documentation
  - architecture
  - ai-systems
  - portfolio
  - hathcock-labs
updated: 2026-11-23
---

# Hathcock Labs — Engineering & Product Documentation Showcase

Welcome to the public engineering knowledgebase for **Hathcock Labs** (**19 chapters** across products, AI cognitive infrastructure, systems deep dives, and milestone logs). This repository serves as a deep architectural manual covering how we design, verify, and ship production software for high-consequence environments—anchored by our flagship **7-part AI Systems Architecture series** detailing how **`Halcyon` (XO & Flight Director)**, **18 domain-specialized engineering agents**, external auditor **`Muse`**, sub-millisecond hybrid memory, **18-upgrade context-efficiency engineering (~20× token reduction)**, and **`24/24` zero-bypass rulesets** work in concert under human architectural control.

> [!NOTE]
> **Universal Format:** Browse directly on **GitHub**, open the folder as a standalone **Obsidian** vault, or publish as a static documentation site with **Quartz v4**. Every cross-reference uses standard relative Markdown links.

---

## Engineering Highlights at a Glance

- **`Halcyon` XO + 18 Native Specialists (`02_AI-Systems-Architecture/`):** Driven by a single-source-of-truth **`squadron.json`** registry (`fleet sync-roster` → `18` natively discovered `agents/*.md` specs, **`-82.6%` compact roster**) with declarative read-only execution locks (`commandExecutionPolicy: off` on `Echo`/`Scout`), Lazy Skill Firewalls (`skills: []` on `Scribe`), **`Tier A1/A2/B/C/D` audit matrices**, mandatory Wave 3 **Adversarial Break-It Passes (`Sentinel` + `Aegis`, looping until `0 CRIT/HIGH`)**, and deterministic **`hooks.json`** (`204` lifecycle hook tests) enforcing `4-Wave` `fcntl.flock` OOM build serialization on `12 GB` RAM.
- **18-Upgrade Engineering ROI & ~20× Production Token Reduction:** Slashed static prompt tax across the board—global rules **`21.0 KB` → `11.5 KB` (`-45.6%`)**, progressive-disclosure skill splits, **`<= 3.5 KB` active blackboard cap**, global MCP prune **`4 → 1`** (closing tool-hook bypasses & moving heavy browser MCP to an on-demand disabled plugin), auto-clamping `>400` → `350`-line code reads, single-command `--reporter=dot`/`line` normalization, and `<100 ms` workspace-sharded `<= 4 KB` symbol maps. Proven end-to-end on Arclight Wave 0 (`16.5K` LOC refactor) + Sprint 2.5 + 3 Adversarial Break-It Audits (`22` defects killed): **`80.5 minutes`**, **`~1.38M` est tokens** across `20` specialist runs, **`0` quota walls** (~20× cut vs `~29.6M` raw read tokens across `2` quota resets).
- **Local Apple Silicon Tuning & 27-Model Dual-Pool Routing:** Tuned Apple Silicon inference with Flash Attention + `q8_0` KV cache + `8K` context cap (eliminating `64K` Modelfile eviction thrash: **`qwen3:8b` at `4.8 GB` VRAM / `37 tok/s`** co-resident with pinned **`nomic-embed-text`** at **`0` evictions & `0 MB` swap**), paired with `27` cloud frontier models (`20` Pool 1 Gemini incl. **Gemini 4 Neon** & **Orchestrator Neon** + Hydrogen/Carbon/Argon/3.8 Flash; `7` Pool 2 Claude 5.5 + sunsetting GPT-OSS 120B excluded from routing), monitored via calibrated `32.5M`/`325M` live `/usage` headers (`XX% LIVE`, `Cld:XX%/XdXXh`).
- **Auto-Hydrated Optane Worktrees, Scoped Anti-Slop, Tree Stamps & `30/30` Doctor:** Isolates active development inside `fleet wt` worktrees, gates every commit under `<5 ms` (`>2 MB` blob / media / SQLite / secret + 5-Category Air-Gap Firewall + **scoped Anti-Slop**), eliminates duplicate `pre-push` test runs safely via **consume-once verified tree stamps (`HEAD^{tree}`, `0700`, `60s` TTL)**, locks **12 repositories** under **`24/24` zero-bypass GitHub Pro Rulesets**, and verifies **`30/30`** cross-node, governance, and **automated stale-model hygiene** invariants via `squad-doctor`.
- **Production Systems Across Regulated & Media Domains:** Tri-State security ERP + live PTT (**Arclight `v0.7.1`**: Sprint 2 watchdogs/anti-spoof/QBR + Wave 0 `16.5K` LOC modular decomposition + Sprint 2.5 clean production onboarding & `orgMode` immutability; **`1,098/1,098` tests**, **`42` Gen-2 functions (`enforceAppCheck: true`)**, **`474.9 KB` max chunk**, `0` `oxlint` across `360` files, `0 CRIT/HIGH` across `3` adversarial rounds), App Store-ready iOS vascular board prep (`421` items, `34/34` unit + `15/15` E2E), programmatic `1080×1920` `60fps` `-14 LUFS` video engine (`33/33` unit, Grade `6.6–9.0`), `<35ms` floor hardware PWAs, and parametric OpenSCAD NFC enclosures.

---

## Recommended Reading Tracks

### Track A · AI & Systems Engineers (Start Here for Multi-Agent Architecture)
If you came for how we avoid LLM context rot, hallucinations, and runaway token burn across real multi-package production repositories:
1. [00 · Cognitive Architecture Overview](02_AI-Systems-Architecture/00-Cognitive-Architecture-Overview.md) — Why single-context chat coding collapses and how our 3-node heterogeneous topology separates compute cleanly.
2. [01 · The 18-Specialist Squadron](02_AI-Systems-Architecture/01-The-18-Specialist-Squadron.md) — Profiles of all 18 domain roles, `-82.6%` compact roster, inter-agent seams, progressive-disclosure `SKILL.md` loading, and Wave 3 Adversarial Break-It Passes.
3. [02 · Five-Tier Memory & Hybrid RRF Retrieval](02_AI-Systems-Architecture/02-Five-Tier-Memory-and-Hybrid-RRF.md) — `<100 ms` `<= 4 KB` sharded symbol maps, `<= 3.5 KB` rolling blackboards, `<1.5 ms` Optane SQLite FTS5 BM25 + 14-day recency fused via Reciprocal Rank Fusion (`k = 60`).
4. [03 · Differential Context & Quota Governance](02_AI-Systems-Architecture/03-Differential-Context-and-Quota-Governance.md) — `<= 2,000`-token compiler, 18-upgrade static prompt tax cuts (`11.5 KB` rules, `4 → 1` MCP prune), `204` lifecycle hook tests, 27-model routing, and the **~20× production token benchmark** (`80.5m`, `~1.38M` est tok, `0` quota walls).
5. [04 · Adversarial Verification & Fact-Locked AI](02_AI-Systems-Architecture/04-Adversarial-Verification-and-Fact-Locked-AI.md) — Two-node adversarial research (`Scout` ↔ `Muse`) and temperature-zero schema-locked production AI.
6. [05 · Autonomous DevOps & Zero-Trust Gates](02_AI-Systems-Architecture/05-Autonomous-DevOps-and-Zero-Trust-Gates.md) — Auto-hydrated Optane worktrees (`fleet wt`), `<5ms` blob/secret & scoped Anti-Slop hooks, consume-once `HEAD^{tree}` (`0700`, `60s` TTL) tree stamps, **`24/24` zero-bypass Pro Rulesets**, **`30/30` diagnostic doctor**, and verified DR restores.
7. [06 · Ambient Mobile Dispatch & Local Inference](02_AI-Systems-Architecture/06-Ambient-Mobile-Dispatch-and-Local-Inference.md) — Zero-RAM kernel `inotify` triggers, Flash-Attention + `q8_0` KV + `8K`-cap Apple Silicon inference (`qwen3:8b` `4.8 GB` / `37 tok/s` co-resident with pinned `nomic-embed-text` at `0` evictions & `0 MB` swap), and `squad-local`.

### Track B · Product & Enterprise Architecture Reviewers
Explore the real-world systems built with this toolchain:
- [Arclight Security ERP & CAD](01_Products/Arclight-Security-ERP.md) — Multi-tenant Tri-State (`MD`, `DE`, `PA`) security guard ERP + live PTT (`v0.7.1`: `1,098/1,098` tests, `42` Gen-2 App-Check functions, `474.9 KB` max chunk, clean prod onboarding & `orgMode` lock).
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
| **AI Systems Architects & Tool Builders** | `02_AI-Systems-Architecture/00` through `06` | `Halcyon` XO + `squadron.json` native agents (`-82.6%` roster), `11.5 KB` rules, `4 → 1` MCP prune, `204` hook tests, **~20× token benchmark (`80.5m` / `~1.38M` tok / `0` quota walls)**, Flash-Attn `qwen3:8b`, `30/30` doctor & `24/24` Pro rulesets. |
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
| **Production Sprint Token ROI** | **`~1.38M` est tokens · `80.5m` · `0` quota walls (~20× cut)** | Wave 0 (`16.5K` LOC) + Sprint 2.5 + 3 Break-It Audits (`22` bugs killed) vs `~29.6M` raw read tokens across `2` resets |
| **Static Prompt Tax & Blackboard** | **`11.5 KB` rules (`-45.6%`) · `-82.6%` roster · `<= 3.5 KB` blackboard** | Global MCP prune (`4 → 1`), progressive-disclosure skills, `<100 ms` `<= 4 KB` sharded symbol maps |
| **Specialist Dispatch & Read Guard** | `<= 2,000` tokens · `>400 → 350L` auto-clamp · `--reporter=dot` | `squad-context` compiler + **`204` automated lifecycle hook tests** (`hooks.json`) |
| **Optane Knowledge Search** | `1.29 ms` lexical / `1,015/1,015` vector parity | SQLite WAL FTS5 BM25 (`5:2:1`) + `14d` recency + `k=60` RRF |
| **27-Model Routing & Telemetry** | `32.5M` 5h / `325M` 7d est · `Cld:XX%/XdXXh` | `Gemini 4 Neon` + `Hydrogen` + `/swarm` pinning + child-transcript `/usage` lock |
| **Local Apple Silicon Co-Residency** | **`qwen3:8b` `4.8 GB` / `37 tok/s` · `0` evictions · `0 MB` swap** | Flash Attention + `q8_0` KV cache + `8K` cap co-resident w/ pinned `nomic-embed-text` (`0` cloud tokens) |
| **Pre-Commit, Stamps & Rulesets** | `< 5 ms` hook · `HEAD^{tree}` `0700` `60s` stamps · `24/24` Rulesets | Blob/media/secret + scoped Anti-Slop, consume-once verified tree stamps, auto-hydrated `fleet wt` |
| **Cross-Node Diagnostic Health** | **`30/30` automated invariants (`squad-doctor`)** | Parallel 3-node probe + rule/symlink/archive/TTL/hook/roster parity + **stale-model hygiene** |
