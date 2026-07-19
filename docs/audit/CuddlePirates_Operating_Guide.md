# CuddlePirates — Operating Guide

*Fable creative/business portfolio audit — deep pass, 2026-07-07. Creative workflow with a light tooling layer — there is no dashboard or CLI of its own; the "interface" is a set of folders, documents, and conventions.*

## The day-to-day workflow

1. **New ideas and notes** → drop into `concept/intake/` (the designated drop zone). Story material as files; art as images. Nothing in intake is canon — it's raw input awaiting analysis.
2. **Concept art** → generated in Midjourney (2023 vintage) or, going forward, ComfyUI via Volta. Source images live in the OneDrive reference roots and are *referenced* by `concept/inventory.json` — the rule is reference, don't copy into the repo.
3. **Story development** → `story-bible/` Markdown files (characters, world, plot, themes, tone-voice, plus deep-dev files for Ann Bunny and the sock mechanic). **Canon changes are human-only** — AI sessions propose in conversation; Andy edits/locks the files.
4. **Scripts and boards** → spec scripts as PDF (e.g. "Laundry Day"), storyboard keyframes under `docs/`.
5. **Pipeline proof** → when assets move toward 3D, they go through **Volta** (`volta mesh`, QA gates, export) with the per-project catalog at `.volta/` once Volta's catalog migration lands.
6. **Status to ATLAS** → `.atlas-bridge/` carries project health into ATLAS's ProjectsPM; task board is `TASK_BOARD.md`.

*Plain language: think of it as three shelves — a messy inbox (`concept/intake/`), a carefully curated reference binder (`inventory.json` pointing at OneDrive), and the official show bible (`story-bible/`, which only Andy may change). Volta is the workshop next door where approved designs get turned into 3D.*

## Key documents and what they rule

| Document | Authority |
|----------|-----------|
| `CLAUDE.md` | Working rules for AI sessions; read first. (Note audit finding CP-4: its "story-bible is placeholder" line is stale.) |
| `docs/round2-answers.md` | Locked decisions from the Round 2 questionnaire (Sections H–M). Section G is the open blocker; K3 has a flagged conflict. |
| `concept/README.md` | The locked visual style: stylized painterly/storybook, not photoreal. |
| `concept/inventory.json` | Manifest of the 97 curated concept images — archetypes, prompts, source paths. |
| `story-bible/` | Show canon. Core-5 cast locked 2026-04-25; hero pair for the demo still TBD. |
| `TASK_BOARD.md` | Open work items. |

## What "working correctly" looks like

- Nothing new is duplicated into the repo tree; new references get inventory entries instead.
- Story-bible edits happen only by Andy's hand (or with his explicit approval in-session), and locked sections cite their source and date.
- The Section G blocker stays visibly open until answered — no invented pitch copy, hero counts, or ownership language anywhere.
- `.eml_quarantine/` stays quarantined; no personal correspondence in new material.

## Manual vs. assisted

- **Manual (Andy):** all canon locks, HERO-tier promotions, style rulings, pitch decisions, Section G answers.
- **AI-assisted:** intake analysis, character/world brainstorming, prompt-library expansion (`docs/AI_Prompt_Library.md`), continuity checking against the bible, board/beat suggestions.
- **Automated:** nothing yet — automation arrives with Volta integration (catalog import, QA gates).

## Current blockers (from the project's own docs)

- **Section G** (one-paragraph pitch, hero counts, key story moment, ownership) — everything downstream of it waits.
- **K3 conflict** — "MetaHuman for heroes" vs locked stylized look; resolve alongside Section G.
- **Demo hero pair TBD** — must be chosen before any rigging starts.
