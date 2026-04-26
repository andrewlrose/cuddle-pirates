# Cuddle Pirates

**The first demo IP for Volta** — a stylized animated short used to prove the boutique virtual-production pipeline (Volta) to the four founding principals.

- **Format:** 2–4 minute animated short
- **Style:** Stylized / painterly storybook (NOT photoreal — see [`concept/README.md`](concept/README.md))
- **Audience target:** TBD (Section G of Round 2 — pending fill)
- **Pitch target date:** Q3 2026
- **Compute target:** M6 (Volta-on-M6 first)

## Status

� **Round 2 complete (2026-04-26)** — all 30 questions answered and locked in [`docs/round2-answers.md`](docs/round2-answers.md). Pitch deck live at https://andrewlrose.github.io/cuddle-pirates/pitch/deck-v1.html. G1–G4 canon locked; G5 (IP ownership) pending Andy's call. Principal outreach written for Mike/Matthew/Jessica.

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

## Active work items

| ID | Item | Status |
|----|------|--------|
| cp-006 | Update deck with G1 (one-para pitch), G2 (hero asset list), G3 (story moment) | Open |
| G5 | IP ownership decision (solo / Andy+Amanda / studio) | Andy's call |
| I3 | VP Supervisor: gold-standard pipeline reference | Awaiting principal |
| I4 | FX Editor: NLE toolchain + round-trip format | Awaiting principal |
| cp-005 | Wire Concept→Mesh→UE5 lookdev path in Volta | Blocked: Volta runner.py |
| cp-002 | Promote MJ references into Volta catalog as REFERENCE-tier assets | Blocked: per-project catalog |

See [`docs/round2-answers.md`](docs/round2-answers.md) for all locked answers (Sections G–M).
See [`docs/principal-questions.md`](docs/principal-questions.md) for I3 and I4 detail.

## Current concept material (2023-10 vintage)

20 Midjourney generations + 2 desktop saves cataloged in [`concept/inventory.json`](concept/inventory.json). Three loose character archetypes are detectable in the prompt strings:

1. **Sir Fuzzy Drake** — "the cuddle pirate sailing through a child's [dream]" (4 refs)
2. **Doctor Suave Charming** — "cuddle pirate sailing the vast seas of [imagination]" (12 refs)
3. **The Bunny Pirate** — "sailing forward through a child's dream" (4 refs)

These are seeds, not canon. Section G will reconcile them.
