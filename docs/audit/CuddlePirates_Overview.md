# CuddlePirates — Project Overview & Recommendations Summary

*Fable creative/business portfolio audit — deep pass, 2026-07-07.*

## What this project is (plain language)

CuddlePirates is an **animated short in development** — plush-toy pirates in fuzzy pajamas, caricatures of historical pirates (and, affectionately, of Raylan's uncles and grandpas), aimed at a 2–4 minute stylized piece. It has a second job that's just as important as the first: it is the **demo IP for Volta**, Andy's virtual-production pipeline. The plan is to prove that one supervisor plus AI tools can take a show from concept art to finished short — and CuddlePirates is the show.

What exists today: a locked visual style (painterly storybook, deliberately *not* photoreal), a locked core cast of five characters, a 1,266-line story bible, a spec script ("Laundry Day") with storyboards, 97 curated Midjourney concept images with a proper inventory manifest, and pitch-analysis documents. Target: pitch to the four founding principals in Q3 2026.

## What it's trying to achieve

Two things at once: a lovable, pitchable kids' property, and living proof that the Volta pipeline works end-to-end. The project's own docs are unusually disciplined about which decisions are locked, which are open (Section G — the one-paragraph pitch and hero cast — is the standing blocker), and what no one is allowed to invent.

## How well it's achieving that

Creatively, it's in strong shape for pre-production — real script, real boards, coherent world rules, documented decisions. Operationally there are four things worth fixing, none of them creative: family emails are only half-quarantined out of the repo and would travel with it if it were ever published (the most important finding, CP-3); the repo carries ~805MB of images including a duplicated snapshot, against its own "reference, don't copy" rule (CP-2); the declared connection to Writers_Room doesn't actually exist — canon is growing outside the family's approval-gated story engine (CP-1); and the entire visual identity traces to a single 2023 OneDrive backup folder with no second copy and no file fingerprints (CP-5/CP-6).

One honest self-contradiction needs a human pass: CLAUDE.md still says the story bible is "placeholder — don't write canon yet," while the story bible itself declares the core cast locked (CP-4).

## Recommendations summary (plain language)

1. **Finish the email quarantine and keep the repo private.** Commit the pending deletions; family correspondence stays out of anything publishable. (CP-3 — High.)
2. **Decide the Writers_Room question on purpose** — plug the story bible into the shared engine, or formally declare Volta-only. (CP-1 — Medium.)
3. **Cut the repo weight**: one copy of the docs snapshot, not two; intake bulk lives in the referenced OneDrive roots. (CP-2 — Medium.)
4. **Fingerprint and back up the concept art** — fill the inventory's empty sha256 fields and copy the OneDrive source folders to the family backup drive. (CP-5/CP-6 — [Data-Ownership].)
5. **Reconcile the "placeholder vs locked" contradiction** and resolve the MetaHuman-vs-stylized conflict when Section G is answered. (CP-4.)

Full detail: `CuddlePirates_Audit_Report.md` in this folder.
