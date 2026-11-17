---
title: Domain-Adaptive Anti-Slop Design System
description: Replacing generic dark-slate AI dashboard clones with domain-specific visual archetypes, OKLCH color tokens, Safari-safe native primitives, and automated DOM/WCAG verification.
tags:
  - design-system
  - ui-ux
  - accessibility
  - webkit
  - oklch
updated: 2026-11-17
---

# Domain-Adaptive Anti-Slop Design System

Left unguided, modern LLM code generators converge on the exact same interface: a dark `#07090e` backdrop, purple/cyan glow pills, four identical-height KPI cards pinned across the top of every page, and custom `<div class="modal-overlay">` popups that trap keyboard focus and break on iOS Safari.

Our design system rejects one-size-fits-all templates in favor of **domain-adaptive craftsmanship**—matching surface luminance, typography, layout density, and browser primitives to the physical environment where the software actually runs.

> [!IMPORTANT]
> **Zero Dashboard Filler Rule:** Never invent placeholder widgets or guessed telemetry counters just to make a grid look symmetrical. Every view centers on one clear primary focal point backed by authentic domain data.

---

## Three Distinct Visual Archetypes

| Archetype | Target Environment | Surface & Typography Choices | Why It Fits |
| :--- | :--- | :--- | :--- |
| **Daylight Enterprise Operations** | Dispatch Consoles, Compliance, Payroll & Client Portals ([Arclight](../01_Products/Arclight-Security-ERP.md)) | Warm-stone `#F6F6F3` canvas, crisp `#FFFFFF` sheets with `1px` `#E2E4E8` rules, `#F0EFEA` `248px` left rail, `#111315` ink, `#1D4ED8` cobalt accent. **3-tier type:** `Instrument Sans` (UI), `Newsreader` serif (formal invoices & legal notices), `IBM Plex Mono` `tabular-nums` (telemetry). | Dispatchers and HR auditors work 8–12 hour shifts under fluorescent office light reading dense tables and legal documents—not dark sci-fi HUDs. Explicit ban on identical 4-KPI-box top grids. |
| **Clinical Calm Study UI** | Medical Board Exam Prep ([SonoPrep](../01_Products/SonoPrep-iOS.md)) | Focused high-contrast dark clinical surface tuned for extended Doppler trace readability, generous `45–75ch` reading measures, physiological box-breathing overlays, and zero decorative chrome. | Ultrasound diagnostics live on dark monitor screens; reducing cognitive clutter keeps test anxiety low and keeps velocity tables legible. |
| **Thumb-Zone Hardware Utility** | Phone-First Floor & Asset Trackers ([Retail PWAs](../01_Products/Retail-Operations-PWAs.md)) | `375px` mobile-first viewport locked to `100dvh`, `>= 44×44px` tap targets, `@container` responsive cradle grids, high-contrast status pills, and instant scan feedback. | Supervisors walk aisles one-handed; cards and buttons must adapt cleanly to narrow handheld containers without pinching or scrolling horizontally. |

---

## Technical Token & Motion Foundations

### 1. Perceptual Color via OKLCH + `color-mix()`
Instead of maintaining brittle hand-picked hex shades for hover states and badges, core tokens are declared in **OKLCH** and mixed dynamically toward `--surface`:

```css
:root {
  color-scheme: light dark;
  --surface: oklch(98% 0.01 255);
  --text: oklch(20% 0.02 255);
  --accent: oklch(52% 0.19 258);
  --accent-soft: color-mix(in oklch, var(--accent) 14%, var(--surface));
  --border-hairline: color-mix(in oklch, var(--text) 10%, var(--surface));
}
```

Mixing toward `--surface` rather than applying raw alpha transparency guarantees predictable WCAG contrast across both daylight and dark themes.

### 2. Purposeful Typography & Structural Motion
- **Fluid Display & Tabular Data:** Headlines scale smoothly with `clamp()` and `text-wrap: balance` to prevent orphaned single words, while every live clock, currency figure, and rate applies `font-variant-numeric: tabular-nums` so numbers never jitter when updating.
- **Motion Budget (`150ms` / `250ms`):** Micro-interactions run in `150ms`, drawers/modals in `250–400ms`, animating **only `transform` and `opacity`** with `@media (prefers-reduced-motion: reduce)` fallbacks and zero cumulative layout shift (`CLS < 0.1`).

---

## Safari & iOS WebKit Resilience Primitives

Many web apps look spotless in desktop Chromium while failing quietly on iOS Safari and Capacitor WKWebView. Every component follows strict platform rules:

- **Native `<dialog>` Over Ad-Hoc `div` Overlays:** All modals open via `.showModal()` for automatic top-layer stacking, focus trapping, `Esc` dismissal, and focus return. Backdrop light-dismiss pairs `pointerdown` and `pointerup` `getBoundingClientRect()` coordinate checks (never `e.target === dialog` or unsupported `closedby="any"`), ensuring dragging text selection out onto the backdrop never closes a dialog prematurely.
- **Root `color-scheme` & WebKit Bug 311752:** Declaring `<meta name="color-scheme">` alongside `:root { color-scheme: ... }` eliminates white initial flash-of-unstyled-content (FOUC), while strictly banning CSS transitions on `scrollbar-color` avoids Safari scrollbar flickering.
- **Deferred Form Validation & VoiceOver Sync:** Inputs use `:user-invalid` rather than raw `:invalid` so fields do not flash red mid-keystroke. Required inputs initialize with `aria-invalid="false"` and bind `aria-describedby` error hints only when invalid so screen readers stay accurate.
- **Semantic Landmarks:** Search bars use native `<search>`, and background app shells receive `inert` whenever non-`<dialog>` side sheets open.

---

## Automated Pre-Ship Visual & WCAG Gate

Before any UI change ships, an automated Playwright visual gate inspects rendered DOM geometry across **`320px`**, **`375px`**, **`768px`**, and **`1440px`** viewports:
1. **Zero Horizontal Overflow:** `scrollWidth <= clientWidth` across every viewport.
2. **Zero Clipped Controls:** Every interactive control fits inside its container with minimum `>= 24×24px` (`>= 44×44px` mobile touch) dimensions.
3. **Zero Core Accessibility Regressions:** Contrast `>= 4.5:1` for body text (`>= 3:1` for large text/UI icons), explicit `<label>` bindings, valid `alt` attributes, single `<h1>`, and visible `:focus-visible` outlines.
