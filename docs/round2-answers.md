# Round 2 — Locked Answers (Sections G–M)

Source: `e:\dev\ATLAS\docs\Volta_Questionaire_Rd2.docx` — extracted 2026-04-25 (S39).
Napkin synopsis provided by Andy 2026-04-25 (S39) — authoritative IP source for G.

All sections locked. Items tagged `(ASK)` route to a principal, not back to Andy.

---

## G. The IP — Cuddle Pirates

| # | Question | Answer |
|---|---|---|
| G1 | One-paragraph pitch | *Cuddle Pirate Theater is a children's animated series about a merry band of plushie pirates — the Cuddle Pirates — who commandeer bedtime to put on a show. Each night the crew sneaks into a child's bedroom, dodges the parent, and performs acrobatic ragdoll antics before telling a bedtime story. Once everyone is asleep, they steal all the comfiest pillows and softest blankets in all the world — fluffy plunder bound for Puff-tooga, their Cuddle Pirate Island. The crew sails aboard The Fluffy Dutchman, a ship that doubles as a pillowcase (legs sticking out the bottom when they need to escape). The characters are caricatures of history's most famous pirates and explorers, reimagined as plush toys in fuzzy pajama costumes: Sir Fuzzy Drake, Marco Pillow, Vasco PaJamas, Anne Bunny, Jean LaFluffe, and others — designed as caricatures of Raylan's uncles and grandpas.* |
| G2 | Hero count for demo reel | **2 hero characters + 1 hero environment + 1 hero prop.** Characters: Sir Fuzzy Drake (confirmed) + 1 TBD from roster. Environment: Juniper's bedroom (pilot ep setting). Hero prop: The Fluffy Dutchman. |
| G3 | Story moment / vertical slice | **30–60s infiltration sequence from the pilot:** Pirates drop through Juniper's window → hall light flickers (Mom moving) → Pirates freeze → light passes → land on bed → ragdoll acrobatics → Juniper laughs silently → Pirates bow. One env, 2–3 chars, cloth/plush sim throughout. |
| G4 | Style target | **Stylized plush/storybook — locked.** Confirmed by both the napkin (plushie pirates in fuzzy pajamas) and the 2023 MJ references. |
| G5 | IP ownership | **OPEN — Andy's call.** Recommendation: Andy solo — keeps demo footage licensable without principal approval. |

> **Note on "Doctor" in MJ filenames:** `"doctor"` is Andy's Midjourney username,
> automatically prepended to all MJ output filenames and prompt strings. It has no
> creative meaning. Ignore it entirely when reading any concept reference filename.

---
## H. Studio / Business Model

| # | Question | Answer |
|---|---|---|
| H1 | How are the four principals being recruited? | **Equity partners.** |
| H2 | Studio revenue model? | **Both — original IP + service work.** Asset library + reuse tracking matters most; dashboard becomes a sales tool. |
| H3 | Studio name? | **Not yet.** "Volta" = pipeline only. |
| H4 | Funding picture? | **Bootstrapped from Andy's savings.** True garage start-up. |
| H5 | Geographic / remote model? | **Hybrid, all principals in LA.** Possible central location at the Senior VP Supervisor's studio. |

## I. The Four Principals

| # | Question | Answer |
|---|---|---|
| I1 | VFX Producer — bottom-up cost model in deck? | **YES.** Built on Volta's actual stage cost telemetry. |
| I1b | VFX Producer seniority? | **Senior production manager.** |
| I2 | Multi-disciplinary artist — single most important demo? | **Speed (concept → rigged in a day), THEN creative control (no AI black boxes). Breadth is inconsequential.** |
| I3 | VP Supervisor — gold-standard pipeline? | **(ASK PRINCIPAL)** — well-versed in many; may not have one. |
| I4 | FX Editor — toolchain (DaVinci / Premiere / Avid)? Round-trip format? | **(ASK PRINCIPAL)** — guess: Avid or DaVinci. |
| I5 | Pitch order? | **Producer + Artist + Editor first (already aware of Cuddle Pirates), VP Supervisor after.** |

## J. Volta Product Positioning

| # | Question | Answer |
|---|---|---|
| J1 | Volta strictly internal, or eventual product? | **Internal-only for now** — optimize for studio's specific workflow. Multi-tenancy/billing/support stubbed for later. |
| J2 | If product, who's the buyer? | **Undetermined until pipeline is proven.** |
| J3 | Moat claim? | **"AI-augmented orchestration on local hardware (M6)" — cost-structure moat.** |

## K. Cuddle Pirates → Volta Scope Mapping

| # | Question | Answer |
|---|---|---|
| K1 | Stages out-of-scope for demo? | Demo = **2–4 minute animated short.** |
| K2 | Demo audio? | **Yes** — VO + score + SFX. |
| K3 | Rig pipeline for hero characters? | **Custom stylized rigs are the default. MetaHuman remains a fallback abstraction seam** for any photoreal sub-asset (e.g. a cameo human). Custom facial animation solutions are first-class, not stubbed. *(Resolved 2026-04-25 — overrides original "MetaHuman-first" wording in the questionnaire to fit the painterly/storybook style.)* |
| K4 | Environment approach? | **Concept (Midjourney) → Mesh (Meshy/photogrammetry) → handcrafted UE5 lookdev.** Pure UE5 PCG procedural is rejected (fights the painterly aesthetic). AI-driven (Promethean / Blockade Labs) deferred — may slot in for set-dressing later. *(Locked 2026-04-25.)* |

## L. Timeline, Hardware, Infrastructure

| # | Question | Answer |
|---|---|---|
| L1 | Pitch target date? | **Q3 2026.** |
| L2 | M6 with ComfyUI online? | **🟡 In progress** per HANDOFF. **Volta on M6 first.** |
| L3 | Other artists testing during R&D? | **Solo until principals signed.** |
| L4 | Backup / DR posture? | **M6 only copy + manual external-drive sync** for now. |

## M. Pre-Scaffolding Confirmations

| # | Question | Answer |
|---|---|---|
| M1 | Cuddle Pirates at `e:\dev\projects\CuddlePirates\` with own bridge? | **YES.** ✅ scaffolded 2026-04-25 (this commit). |
| M2 | New ATLAS pillar for "Studio" or fold under existing? | **Cuddle Pirates under projects, studio business under career.** |
| M3 | Volta catalog `~/.volta/` → `<project>/.volta/`? | **Per-project.** ✅ placeholder dir created in this scaffold. |
| M4 | Draft pitch deck this session? | **No — focus on Volta engineering. Deck = separate session.** |

---

## 8-Item Execution Path (post-Round-2)

1. ✅ **Scaffold `e:\dev\projects\CuddlePirates\`** — done 2026-04-25 (S39)
2. ⬜ Build `volta/runner.py` orchestrator (archive-on-rerun + auto-cascade)
3. ⬜ `approval_status` on `Asset` model + `volta approve / reject` enforced for tier=HERO
4. ⬜ Per-project catalog migration: `~/.volta/` → `<project>/.volta/` + `volta init`
5. ⬜ Meshy credit + ComfyUI GPU-seconds telemetry → ATLAS daily-briefing surface
6. ⬜ Stylized-rig-first path with MetaHuman as fallback abstraction seam (per K3 locked answer)
7. ⬜ Defer client-facing web dashboard to post-3–6mo milestone
8. ⬜ Pitch deck markdown draft, per-principal sections (separate session per M4)
