# Demo 04 — Minitap alt-text accessibility fix (concept)

**Target:** Minitap — https://www.minitap.ai (Paris; "mini", the AI QA agent for iOS/Android/web regression tests; founder Nico reachable at nico@minitap.ai)

## The issue (verified on the live site, 2026-10-13)

In the raw HTML of https://www.minitap.ai/: **125 of 144 `<img>` tags carry an empty `alt=""` attribute** — including customer logos, testimonial avatars and feature screenshots. Screen readers skip all of them, and image search can't index any of them.

## The fix (this demo)

A self-contained, mobile-first interactive page in Minitap's deep-purple brand:
- **Screen-reader simulator** with a Before/After toggle on a recreated customer-logo + testimonial strip (illustrative placeholder content — not Minitap's real customers).
- **Fix checklist:** logos get `alt="<Company> logo"`, avatars get person + role, screenshots get a one-sentence summary, decorative icons keep `alt=""`, plus an eslint jsx-a11y/alt-text lint rule to prevent regressions.
- Single self-contained `index.html` — no build step, no external assets (placeholder images are inline SVG data-URIs).

> Concept demo only — not affiliated with Minitap. Built to show the fix, not to impersonate.
