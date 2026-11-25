---
title: Hathcock Labs — Public Engineering & Product Documentation
description: Authoritative public documentation book covering Hathcock Labs' AI multi-agent engineering architecture, Squadron Harness v1, HALCYON Flight Deck voice PWA, regulated security ERP, iOS clinical exam preparation, retail hardware PWAs, and parametric CAD systems.
tags:
  - documentation
  - architecture
  - ai-systems
  - portfolio
  - hathcock-labs
updated: 2026-11-25
---

# Hathcock Labs — Engineering & Product Documentation Showcase

Welcome to the public engineering knowledgebase for **Hathcock Labs** (**19 chapters** across products, AI cognitive infrastructure, systems deep dives, and milestone logs). This repository serves as a deep architectural manual covering how we design, verify, and ship production software for high-consequence environments—anchored by our flagship **7-part AI Systems Architecture series** detailing how **`Halcyon` (XO & Flight Director)**, **18 domain-specialized engineering agents**, external auditor **`Muse`**, sub-millisecond hybrid memory, **18-upgrade context-efficiency engineering (~20× token reduction)**, and **`24/24` zero-bypass rulesets** work in concert under human architectural control.

> [!NOTE]
> **Universal Format:** Browse directly on **GitHub**, open the folder as a standalone **Obsidian** vault, or publish as a static documentation site with **Quartz v4**. Every cross-reference uses standard relative Markdown links.

---

## Engineering Highlights at a Glance

- **`Halcyon` XO, Squadron Harness v1 & 18 Native Specialists (`02_AI-Systems-Architecture/`):** Driven by a single-source-of-truth **`squadron.json`** registry (`18` natively discovered `agents/*.md`, **`-82.6%` compact roster**) and executed via **`squad-harness`** (code-enforced 4-Wave Mission Runner + Micro-Chunk DAG Swarm, atomic local NVMe mission state, standalone Wave 3 **Break-It Gate (`Sentinel` + `Aegis`, `0 CRIT/HIGH`)**, **12-case adversarial specialist eval suite**, and `204` lifecycle hook tests enforcing `fcntl.flock` OOM build serialization on `12 GB` RAM).
- **HALCYON Flight Deck Voice PWA & Local Apple Silicon M1 Max v1.2 (`06-Ambient-Mobile-Dispatch-and-Local-Inference.md`):** Local FastAPI + persistent warm NDJSON bridge + installable Android/iPadOS PWA delivering **~4× lower latency (`8.5–11.5s` → `2.32s` warm first token)**, `16 kHz` WAV TTS (`0.29s`), 3-way sentence streaming, `scribe_v1` Push-to-Talk (`audio/mp4` Safari fallback), dual-channel `---` voice framing, `76px` 64-bar visualizer, zero-token Tailscale Serve auth (`--no-proxy-headers`, W3C Fetch Metadata, `/assets/*`-only `sw.js`), and an in-house zero-token knowledge graph (`62` notes / `94` nodes / `743` edges). Backed by **3-model M1 Max co-residency (`15.13 GB` / `32 GiB`):** `nomic-embed-text` (`0.34 GB`) + `qwen3:8b` (`5.12 GB` @ **`36.9 tok/s`**, **`93–95%` payload compression** via `squad-context --compress-local`) + `qwen2.5-coder:14b` (`9.67 GB` @ **`21.4 tok/s`** Wave 0 Zod/Vitest scaffolding) at **`0` evictions, `0 MB` swap, `0` cloud tokens**.
- **18-Upgrade Engineering ROI (~20× Token Cut) & Zero-Bloat `modern-web-guidance` Fleet Audit:** Slashed static prompt tax (`11.5 KB` rules, `4 → 1` MCP prune, `<= 3.5 KB` blackboard, `<100 ms` `<= 4 KB` symbol maps), proven end-to-end on Arclight Wave 0 + Sprint 2.5 (**`80.5m`**, **`~1.38M` est tok**, **`0` quota walls**), and wired on-demand **`npx modern-web-guidance@latest`** audits across 10 apps where specialist Keep/Drop filtering eliminated **`26/47` false positives** while hardening React 19 `<dialog>` portals, Safari 18.2–26.1 scrollbars, iOS 15.0 `1dvh`/`1svh` fallbacks, and `bfcache`-safe hosting headers.
- **Auto-Hydrated Local NVMe Worktrees, Scoped Anti-Slop, Tree Stamps & `30/30` Doctor:** Isolates active development inside `fleet wt` worktrees, gates every commit under `<5 ms` (`>2 MB` blob / media / SQLite / secret + 5-Category Air-Gap Firewall + **scoped Anti-Slop**), eliminates duplicate `pre-push` test runs safely via **consume-once verified tree stamps (`HEAD^{tree}`, `0700`, `60s` TTL)**, locks **12 repositories** under **`24/24` zero-bypass GitHub Pro Rulesets**, and verifies **`30/30`** cross-node, governance, and **automated stale-model hygiene** invariants via `squad-doctor`.
- **Production Systems Across Regulated & Media Domains:** Tri-State security ERP + live PTT (**Arclight `v0.7.1`**: **`1,098/1,098` tests**, **`42` Gen-2 functions (`enforceAppCheck: true`)**, **`474.9 KB` max chunk**, `0` `oxlint` across `360` files, `0 CRIT/HIGH` across `3` adversarial rounds), App Store-ready iOS vascular board prep (`421` items, `34/34` unit + `15/15` E2E), programmatic `1080×1920` `60fps` `-14 LUFS` video engine (`33/33` unit, Grade `6.6–9.0`), `<35ms` floor hardware PWAs, and parametric OpenSCAD NFC enclosures.

---

## Recommended Reading Tracks

### Track A · AI & Systems Engineers (Start Here for Multi-Agent Architecture)
If you came for how we avoid LLM context rot, hallucinations, and runaway token burn across real multi-package production repositories:
1. [00 · Cognitive Architecture Overview](02_AI-Systems-Architecture/00-Cognitive-Architecture-Overview.md) — Why single-context chat coding collapses and how our 3-node heterogeneous topology separates compute cleanly.
2. [01 · The 18-Specialist Squadron](02_AI-Systems-Architecture/01-The-18-Specialist-Squadron.md) — Profiles of all 18 domain roles, `-82.6%` compact roster, inter-agent seams, progressive-disclosure `SKILL.md` loading, and Wave 3 Adversarial Break-It Passes.
3. [02 · Five-Tier Memory & Hybrid RRF Retrieval](02_AI-Systems-Architecture/02-Five-Tier-Memory-and-Hybrid-RRF.md) — `<100 ms` `<= 4 KB` sharded symbol maps, `<= 3.5 KB` rolling blackboards, `<1.5 ms` Optane SQLite FTS5 BM25 + 14-day recency fused via Reciprocal Rank Fusion (`k = 60`).
4. [03 · Differential Context & Quota Governance](02_AI-Systems-Architecture/03-Differential-Context-and-Quota-Governance.md) — `<= 2,000`-token compiler, 18-upgrade static prompt tax cuts (`11.5 KB` rules, `4 → 1` MCP prune), `204` lifecycle hook tests, 27-model routing, and the **~20× production token benchmark** (`80.5m`, `~1.38M` est tok, `0` quota walls).
5. [04 · Adversarial Verification & Fact-Locked AI](02_AI-Systems-Architecture/04-Adversarial-Verification-and-Fact-Locked-AI.md) — Two-node adversarial research (`Scout` ↔ `Muse`), zero-bloat `modern-web-guidance` Keep/Drop filtering (`26/47` false positives dropped), 12-case adversarial evals, and temperature-zero schema-locked production AI.
6. [05 · Autonomous DevOps & Zero-Trust Gates](02_AI-Systems-Architecture/05-Autonomous-DevOps-and-Zero-Trust-Gates.md) — **Squadron Harness v1 + Micro-Chunk DAG Swarm** (`squad-harness`), auto-hydrated local NVMe worktrees (`fleet wt`), `<5ms` blob/secret & scoped Anti-Slop hooks, consume-once `HEAD^{tree}` (`0700`, `60s` TTL) tree stamps, **`24/24` zero-bypass Pro Rulesets**, **`30/30` diagnostic doctor**, and verified DR restores.
7. [06 · Ambient Mobile Dispatch, HALCYON Flight Deck & Local Inference](02_AI-Systems-Architecture/06-Ambient-Mobile-Dispatch-and-Local-Inference.md) — **HALCYON Flight Deck** (`2.32s` warm voice PWA, ~4× cut, zero-token Tailscale Serve auth, `62`-note / `94`-node / `743`-edge graph), zero-RAM `inotify` triggers, and **Apple Silicon M1 Max v1.2** 3-model co-residency (`15.13 GB` / `32 GiB`, `36.9 tok/s` `93–95%` compression, `21.4 tok/s` Wave 0 scaffolding).

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
| **Local Apple Silicon Co-Residency v1.2** | **`15.13 GB` / `32 GiB` (`3` models) · `36.9` / `21.4 tok/s`** | `nomic-embed-text` (`0.34 GB`) + `qwen3:8b` (`5.12 GB`, `93–95%` compression) + `qwen2.5-coder:14b` (`9.67 GB`, Wave 0 scaffold), `0` evictions, `0` cloud tokens |
| **HALCYON Flight Deck Voice PWA** | **`2.32s` warm first token (~4× cut) · `0.29s` `16 kHz` WAV** | Warm NDJSON bridge, 3-way sentence queue, `scribe_v1` PTT, zero-token Tailscale Serve auth, `62`-note / `94`-node / `743`-edge graph |
| **Squadron Harness v1 & MWG Audit** | **4-Wave DAG + 12-case evals · `26/47` FPs filtered** | Code-enforced mission runner, standalone Wave 3 Break-It Gate (`0 CRIT/HIGH`), on-demand `npx modern-web-guidance@latest` across 10 apps |
| **Pre-Commit, Stamps & Rulesets** | `< 5 ms` hook · `HEAD^{tree}` `0700` `60s` stamps · `24/24` Rulesets | Blob/media/secret + scoped Anti-Slop, consume-once verified tree stamps, auto-hydrated `fleet wt` |
| **Cross-Node Diagnostic Health** | **`30/30` automated invariants (`squad-doctor`)** | Parallel 3-node probe + rule/symlink/archive/TTL/hook/roster parity + **stale-model hygiene** |
