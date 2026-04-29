# LeadSpot.AI Landing Pages

Static landing-page variants for LeadSpot.AI — the AI-native CRM with auto-logged
desktop activity, plain-English queries, and a 60-second hold + cancel toast
that keeps your screen on your machine.

## Variants

- **`variant-e-command-ai/`** — Live primary variant. Cmd+K query palette hero,
  word-by-word blur-in headline, scroll-driven zoom on feature cards,
  conversational AI with explicit send/queue confirmation, comparison table
  vs. spreadsheet/HubSpot/Gong, founder note, $39/mo founder pricing.
- **`variant-a-stripe-quiet/`** — Quieter Stripe-style variant.
- **`variant-c-indie-honest/`** — Indie-honest founder-led variant.
- **`variant-d-bento-dark/`** — Bento-grid dark variant.

## Local preview

```bash
open variant-e-command-ai/index.html
```

Each variant is a single self-contained `index.html` (CSS + JS inline). No
build step.

## Pre-launch checklist

The current `variant-e-command-ai/` has three remaining placeholders, each
marked with a red dashed outline + `⚠ REPLACE BEFORE SHIP` badge so they're
impossible to miss:

- [ ] Social-proof avatars + testimonial quote in the hero
  (`data-placeholder="swap-when-real"`)
- [ ] Urgency counter "23 of 100 spots taken" — should be wired to a real
  Stripe-driven count (`data-placeholder="swap-with-real-counter"`)
- [ ] Loom thumbnail click target — currently `#install`, should link to a
  real recorded 60-second demo

To remove ALL placeholder badges in one shot once everything's real:
1. Find/remove the `[data-placeholder]` CSS block in the `<style>` section
2. Strip the remaining `data-placeholder="..."` attributes (≤3 occurrences)

## Stack

Pure static HTML — no framework, no build, no dependencies. Google Fonts are
loaded from Google's CDN. The `assets/` folder inside each variant holds
locally-served images (currently `mike.png` for the Loom thumbnail + founder
note avatar).
