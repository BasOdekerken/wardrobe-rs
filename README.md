# Ensemble
 
A personal wardrobe management and outfit recommendation tool. Catalog your
clothing, generate outfit combinations, rate them, feed in inspiration
photos, and (eventually) get AI-assisted styling advice and wardrobe gap
recommendations.
 
## Goals
 
- Catalog every clothing item I own with structured metadata and a photo.
- Generate outfit combinations from that catalog, taking body type and
  styling tips into account.
- Let me rate generated (and manual) outfits so the system improves over
  time.
- Accept inspiration photos found online and use them to bias future
  suggestions toward that style.
- Eventually recommend specific new items to buy that would fill real gaps
  in the wardrobe.
## Approach
 
- **Language/stack:** Rust, using Leptos + Axum for a full-stack web app,
  SQLite for storage.
- **License:** MIT OR Apache-2.0 (standard for Rust projects).
- **Recommendation logic:** start with simple, hand-written rules (color
  matching, layering, formality), then later add AI-assisted suggestions.
## What it needs to track (roughly)
 
- **Clothing items** — category, color, material, which layer it works as,
  formality, season, tags, a photo.
- **My body profile** — body type and styling preferences, used to bias
  recommendations.
- **Outfits** — combinations of items, with a rating and notes.
- **Inspiration photos** — images I feed in, plus whatever style
  attributes get extracted from them.
Exact fields and schema to be nailed down during Phase 1.
 
## Build order / phases
 
- [ ] **Phase 1 — Wardrobe catalog:** add/edit items, upload photos, tag
      them, browse/filter the collection. No AI, no recommendation logic
      yet.
- [ ] **Phase 2 — Body profile:** a settings page for body type and style
      preferences.
- [ ] **Phase 3 — Rule-based outfit generator:** hand-written scoring
      logic only (color, layering, formality).
- [ ] **Phase 4 — Rating + feedback storage.**
- [ ] **Phase 5 — AI layer:** add AI-assisted suggestions, comparing a
      local model against an API-based one.
- [ ] **Phase 6 — Wardrobe gap analysis** and purchase recommendations.