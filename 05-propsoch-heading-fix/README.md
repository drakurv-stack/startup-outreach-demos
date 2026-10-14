# Demo 05 — Propsoch hero heading fix

**Startup:** Propsoch (propsoch.com) — buyer-centric homebuying advisory platform, Bengaluru. $2M seed (June 2026).

## Observed issue (verified 2026-10-14)

The homepage hero renders **two `<h1>` tags** — separate mobile and desktop hero markup both ship in the served HTML (verified via curl raw HTML of https://propsoch.com/). Screen readers announce two competing page titles, and search engines split the ranking signal.

## What this demo fixes

A before/after audit of the hero heading:
1. **One `<h1>`** — duplicate mobile/desktop hero markup merged; responsive CSS replaces the duplication.
2. **Accessible rotator** — rotating words live in an `aria-live="polite"` region so screen readers announce each word.
3. **Honest assistive text** — the sr-only label now describes the animation instead of contradicting it.

Single self-contained `index.html` — no build step, no external assets, mobile-first, styled to Propsoch's brand (orange #FF6D33).

> Concept demo only — not affiliated with Propsoch. Built to illustrate a real, observed website issue and its fix.
