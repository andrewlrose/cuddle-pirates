# Cuddle Pirates

**The first demo IP for Volta** — a stylized animated short used to prove the boutique virtual-production pipeline (Volta) to the four founding principals.

- **Format:** 2–4 minute animated short
- **Style:** Stylized / painterly storybook (NOT photoreal — see [`concept/README.md`](concept/README.md))
- **Audience target:** TBD (Section G of Round 2 — pending fill)
- **Pitch target date:** Q3 2026
- **Compute target:** M6 (Volta-on-M6 first)

## Status

🟡 **Scaffolded 2026-04-25 (S39)** — directory tree and bridge in place; story bible seeded from 2023 Midjourney concept materials and visual analysis. Section G of the Round 2 questionnaire is on hold pending IP definition; once filled, story-bible files get rewritten from placeholders to canon.

## Layout

```
CuddlePirates/
├── .atlas-bridge/        # ATLAS bridge contract (manifest, memory, tasks)
├── .volta/               # Per-project Volta catalog (Q29 confirmed: per-project, not ~/)
├── concept/              # Source concept materials inventory
│   ├── inventory.json    # Manifest of source images (absolute paths, not duplicates)
│   ├── README.md         # Visual style analysis of existing references
│   └── intake/           # DROP ZONE for new concept material (notes, images, audio, refs)
├── story-bible/          # Canon — written/rewritten as Section G fills in
│   ├── characters.md
│   ├── world.md
│   ├── tone-voice.md
│   ├── themes.md
│   └── plot.md
├── pitch/                # Pitch deck working files (deferred per Q30)
├── docs/
│   └── round2-answers.md # Locked Round 2 answers (Sections H–M)
├── package.json
├── CLAUDE.md             # AI agent context for this project
└── .gitignore
```

## Pending (must fill before pitch)

The following questions are **HOLD** until Section G of Round 2 is answered:

- **Q1** — One-paragraph pitch (genre, audience, tone, hook)
- **Q2** — Hero character / environment / prop counts for the demo reel
- **Q3** — Story moment / vertical slice (30s teaser vs 90s trailer)
- **Q4** — ✅ resolved by visual analysis: stylized, NOT photoreal
- **Q5** — IP ownership (solo / Andy+Amanda / studio)

See [`docs/round2-answers.md`](docs/round2-answers.md) for everything else.

## Current concept material (2023-10 vintage)

20 Midjourney generations + 2 desktop saves cataloged in [`concept/inventory.json`](concept/inventory.json). Three loose character archetypes are detectable in the prompt strings:

1. **Sir Fuzzy Drake** — "the cuddle pirate sailing through a child's [dream]" (4 refs)
2. **Doctor Suave Charming** — "cuddle pirate sailing the vast seas of [imagination]" (12 refs)
3. **The Bunny Pirate** — "sailing forward through a child's dream" (4 refs)

These are seeds, not canon. Section G will reconcile them.
