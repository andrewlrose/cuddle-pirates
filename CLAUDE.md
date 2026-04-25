# CuddlePirates — Claude Code Context

## What this is
Cuddle Pirates is the **first demo IP for Volta** — a stylized 2-4 minute animated short used to prove the boutique virtual-production pipeline to the four founding principals (VFX Producer, multi-disciplinary artist, Senior VP Supervisor, FX Editor). Pitch target: **Q3 2026**.

## Read first
1. [`README.md`](README.md) — orientation + status
2. [`docs/round2-answers.md`](docs/round2-answers.md) — locked answers from Round 2 questionnaire (Sections H–M); Section G is on hold
3. [`concept/README.md`](concept/README.md) — visual style analysis (locked: stylized painterly/storybook, NOT photoreal)
4. [`concept/inventory.json`](concept/inventory.json) — manifest of source concept images (referenced by absolute path, not duplicated)
5. [`concept/intake/`](concept/intake/) — DROP ZONE for new concept material; analyzed on demand for Section G prep
6. [`story-bible/`](story-bible/) — placeholder canon files; rewritten when Section G fills

## Bridge
- ATLAS bridge contract at [`.atlas-bridge/`](.atlas-bridge/) — same shape as ElmoreCreek and Volta
- Project lives under `ProjectsPM` in ATLAS, NOT under a new "Studio" pillar (per Round 2 M2)
- Studio business itself lives under ATLAS career pillar

## Coupling
- **Depends on Volta** for: catalog tracking, image-to-3D, rig management, QA, export
- **Per-project Volta catalog** lives at `.volta/` — NOT `~/.volta/` (per Round 2 M3)
- **Concept materials** at `E:/OneDrive/Backup_2023oct22/AI` and `E:/OneDrive/Backup_2023oct22/Desktop` — Volta will import these as REFERENCE-tier assets when per-project catalog migration ships

## Open blockers (do not invent answers)
- **Round 2 Section G** (Q1-Q5) — IP definition: one-paragraph pitch, hero counts, story moment, ownership. Story-bible files stay placeholder until filled.
- **K3 conflict flagged**: Round 2 K3 says "MetaHuman for hero characters", but visual analysis says style is stylized → MetaHuman is wrong default. Resolve when Section G is filled.

## What NOT to do
- Don't duplicate concept PNGs into the project tree — they live in OneDrive; reference by path
- Don't write story-bible canon yet — it's placeholder until Section G
- Don't draft the pitch deck here — separate session per Round 2 M4
- Don't promote any character to HERO tier — only Andy approves promotions
