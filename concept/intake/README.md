# Concept Intake — Drop Zone

This is the **single drop folder** for any new Cuddle Pirates concept material that needs analysis or incorporation. Drop anything you have — written notes, voice memos, images, sketches, screenshots, links, half-finished story beats. Don't worry about format or organization.

## How to use

1. Drop files directly into this folder (or any subfolder). Filename can be anything.
2. For **text snippets / voice transcripts / loose ideas** that aren't already a file, add them to [`notes.md`](notes.md) — append at the bottom with a date stamp.
3. When you're ready to do a Section G analysis pass, ping the assistant: *"Analyze the intake folder for Section G."*

## What lives where

| Path | What goes here |
|---|---|
| `concept/intake/` (this folder) | **RAW DROP ZONE** — unfiltered material; assistant reads but does not reorganize |
| `concept/intake/notes.md` | Inline text dump — quick ideas, voice-memo transcripts, references to films/books/IP |
| `concept/intake/images/` | New concept art, sketches, screenshots, mood frames |
| `concept/intake/audio/` | Voice memos, music references, score sketches |
| `concept/intake/external-refs.md` | Links to films, books, games, IP for tone/style/structure reference |
| `concept/inventory.json` (parent dir) | LOCKED canonical manifest of the 2023 Midjourney references — do not edit by hand |
| `story-bible/` | Canon — written ONLY after Section G is filled |

## Suggested intake template (optional)

When you have a moment, jot down whatever you can answer for Section G into [`notes.md`](notes.md) — even fragments help:

- **G1 — One-paragraph pitch:** genre, audience, tone, hook
- **G2 — Demo scope:** how many hero characters / environments / props for the reel
- **G3 — Vertical slice:** what 30–90 seconds are we shooting for the demo
- **G4 — Style:** ✅ already locked stylized; only fill if overriding
- **G5 — IP ownership:** Andy solo, Andy + Amanda, or studio post-equity

## What the assistant will do with this folder

When asked to analyze, the assistant will:

1. Read every file in `intake/` (not just `notes.md`)
2. View any new images and pull style/character/environment cues
3. Cross-reference against the 2023 references in [`../inventory.json`](../inventory.json) to flag continuity or drift
4. Produce a Section G draft with confidence levels per question
5. NOT promote anything to canon — `story-bible/` only updates after you explicitly approve the draft

## What NOT to do

- Don't put canon material here — that goes in `story-bible/` only after approval
- Don't delete files; if something is superseded, add a note in [`notes.md`](notes.md) saying so
- Don't worry about file naming — assistant handles that
