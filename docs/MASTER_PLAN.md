# CuddlePirates × Volta — Master Plan

**Author:** Andy Rose
**Created:** 2026-05-23
**Horizon:** Now → Q3 2026 founding-principals pitch (with long-horizon feature/series note)
**Cadence assumption:** ~15–25 hrs/week, solo, alongside the Lightspeed LA day job
**Scope of this plan:** CuddlePirates (creative target) + Volta (production pipeline). *Bear Suit Man is intentionally out of scope.*

---

## 1. The relationship in one sentence

**Volta is the pipeline; CuddlePirates is the proof.** Volta is an AI-assisted virtual-production pipeline (Concept → Mesh → Rig → Anim → FX → Comp → Export) built as a real Python CLI. CuddlePirates is the first demo IP, and its only near-term job is to produce a 30–60-second vertical slice that proves Volta works — the centerpiece of a Q3 2026 pitch to four founding equity principals.

---

## 2. Scope & target of each project

### CuddlePirates — the creative target

| Dimension | Definition |
|---|---|
| **Near-term deliverable** | A 30–60s rendered vertical slice: the infiltration sequence from the pilot (*The Sock-topuss*). |
| **Long-horizon ambition** | A full CGI feature/series — *deferred until the studio exists and is funded.* Not on this plan's critical path. |
| **Style (locked)** | Stylized painterly plush / storybook. NOT photoreal. |
| **Hero assets for the slice** | 2 hero characters (Sir Fuzzy Drake + 1 TBD) · 1 hero environment (Juniper's bedroom) · 1 hero prop (The Fluffy Dutchman). |
| **Creative canon** | Round 2 locked (30/30 questions). IP, tone, beat sequence all defined. |
| **Open creative items** | G5 IP ownership (Andy's call) · 2nd hero character selection · story-bible canon still placeholder · K3 rig conflict resolved toward custom stylized rigs. |

### Volta — the production pipeline

| Dimension | Definition |
|---|---|
| **What it is** | A single-CLI orchestration layer that makes a 5-person boutique operate like a 50-person pipeline: local-first (M6), AI-augmented (not AI-driven), approval-gated, cost-visible, reusable. |
| **Near-term target** | Be able to take the CuddlePirates vertical slice **end-to-end** — and emit real per-stage cost telemetry. |
| **Built today** | SQLite catalog with tiers/provenance/approval gates, CLI surface (~841 lines), QA validators, ATLAS bridge sync, basic ComfyUI + Meshy clients, FFmpeg/social export, BVH mocap ingest, HIK templates. |
| **Phase-2 stubs (block the reel)** | Full-pipeline orchestration (`volta run` / `runner.py`), film export via UE5 Movie Render Queue → EXR/ProRes, auto-rig, Cascadeur mocap cleanup. |
| **Long-horizon target** | Internal-only product; multi-tenancy/billing deferred. Possible external licensing only after the pipeline is proven. |

### The central tension to resolve

> **The pipeline cannot yet render the very deliverable it exists to prove.** Film export is stubbed, end-to-end orchestration is stubbed, and the reel is "in production." The pitch deck is written in present tense while the rendering path doesn't run end-to-end. Closing that gap is the whole game between now and Q3.

---

## 3. Goals

### Primary goal (this plan)
Render the CuddlePirates vertical slice through Volta, capture real cost telemetry, finalize the deck, and pitch the four principals in Q3 2026.

### Supporting goals
1. **Volta:** Make the reel-critical path real — orchestration, stylized-rig path (Concept→Mesh→UE5), film export (MRQ→EXR + MP4 dailies), and stage-cost telemetry surfaced to the deck.
2. **CuddlePirates:** Lock remaining creative (G5 ownership, 2nd hero, pilot-slice story-bible canon) and build the four hero assets through to HERO tier.
3. **Pitch:** Finalize the deck with real numbers + rendered reel + principal bios + I3/I4 answers; run Wave 1 (Producer, Artist, Editor) then Wave 2 (VP Supervisor).

### Long-horizon goal (off critical path)
Convert a successful pitch into a funded boutique studio that produces the CuddlePirates feature/series — pipeline as the asset, IP as the proof.

### Definition of done (pitch-ready)
- 30–60s reel rendered at 4K (EXR master + MP4 daily), with scratch-or-locked audio.
- `volta run` produces the slice end-to-end and logs per-stage cost; cost-model slide uses **real** numbers, not placeholders.
- Deck Wave-1 sections complete with bios + I4 NLE answer; reel embedded.
- A documented fallback (beat board + partial reel) exists in case rendering slips.

---

## 4. The master plan — phased, with timeline

Today is **2026-05-23**. Target Wave-1 pitch: **week of Sept 7, 2026** (~15 weeks out). Because the work is solo, engineering capability and creative build interleave rather than fully parallelize: **each pipeline stage must work before the creative asset for that stage can flow through it.**

### Phase 0 — Decisions & foundation lock · *Now → ~Jun 1 (Week 0–1)*
- Resolve **G5 IP ownership** (recommendation in docs: Andy solo, keeps footage licensable).
- Choose the **2nd hero character** from the roster.
- Send **I3/I4 outreach** to principals (VP Supervisor gold-standard pipeline; FX Editor NLE + round-trip format) — answers feed the deck's EXPORT + telemetry slides.
- Stand up creative tracking: scaffold the CuddlePirates production board + finish **per-project catalog migration** (`~/.volta/` → `<project>/.volta/`, `volta init`).
- **Exit criteria:** ownership decided, 2nd hero named, principal questions sent, CuddlePirates catalog live.

### Phase 1 — Pipeline-to-reel engineering · *Jun 1 → Jun 28 (Week 1–5)* — **critical path**
- Build the **`runner.py` orchestrator** (`volta run UID`): archive-on-rerun + auto-cascade across stages.
- Implement **film export**: UE5 Movie Render Queue → 4K EXR + ProRes, plus the always-on MP4 dailies lane.
- Wire the **stylized-rig path**: Concept (MJ) → Meshy mesh → Blender cleanup → custom UE5 stylized rig (no MetaHuman dependency for heroes).
- Enforce **approval gate** for `tier=HERO` (`volta approve / reject`).
- Add **stage-cost telemetry** (Meshy credits + GPU-seconds + compute hours) surfaced to a summary the deck can quote.
- **Exit criteria:** a throwaway test asset goes ingest→export and prints real per-stage cost.

### Phase 2 — Hero asset build · *Jun 15 → Jul 19 (Week 3–9, overlaps Phase 1)*
- **Sir Fuzzy Drake** through the full promotion path to HERO (cloth/plush sim baked at rig).
- **2nd hero character** through the same path.
- **Juniper's bedroom** environment (Concept → Mesh → handcrafted UE5 lookdev — no pure PCG).
- **The Fluffy Dutchman** prop (pillowcase hull cloth sim, legs underneath).
- Promote **story-bible canon** for the pilot slice from placeholder → locked (characters, world, the infiltration beats).
- **Exit criteria:** all four hero assets at HERO tier in the catalog with approvals + cost logged.

### Phase 3 — Vertical slice production · *Jul 13 → Aug 9 (Week 8–11)*
- Block the **30–60s infiltration sequence** in UE5 Sequencer (window drop → hall-light freeze → bed landing → ragdoll acrobatics → bow).
- **ANIM:** silent physical-comedy timing; full-body ragdoll response to the simulated sound/light event.
- **FX:** cloth/soft-body on pajamas, pillowcase hull, sails/rigging; light dust/atmosphere.
- **COMP:** two-light-source lighting design (warm hall light = threat, cool moonlight = safe) — the comedy beat is a lighting cut.
- **Exit criteria:** locked cut (playblast-approved), scratch audio in place.

### Phase 4 — Render, finish & telemetry capture · *Aug 3 → Aug 30 (Week 11–14)*
- **Render** via `volta run` → 4K EXR master + MP4 dailies (this is the real test of Phase 1).
- **Editorial** assembly + sound pass (VO/score/SFX as discrete stems) + color.
- **Capture real stage telemetry** from the production run → replace every placeholder in the cost-model slide.
- **Exit criteria:** delivered reel + a real cost table.

### Phase 5 — Pitch finalization & delivery · *Aug 24 → Sept 13 (Week 13–16)*
- Update deck: embed reel, drop in **real telemetry**, add **principal bios**, answer **I4** in the EXPORT slide.
- **Wave 1 pitch:** Producer + Artist + Editor (already aware of CuddlePirates).
- **Wave 2 pitch:** Senior VP Supervisor, after I3 is answered and Wave 1 lands.
- **Exit criteria:** all three Wave-1 pitches delivered; Wave-2 scheduled.

### Long-horizon track (post-pitch, off critical path)
Feature/series scoping, studio formation, funding model, and series-bible expansion — planned only once principals are signed and the pipeline is proven.

---

## 5. Critical path & dependencies

```
Phase 0 decisions ─┬─> Phase 1 pipeline engineering ──┐
                   │                                   ├─> Phase 4 render (needs Phase 1 export + Phase 3 cut)
                   └─> Phase 2 hero assets ─> Phase 3 production ──┘
                                                                   └─> Phase 5 pitch (needs reel + telemetry)
```

The hard gate: **film export + `runner.py` (Phase 1) must work before Phase 4 can render.** If Phase 1 slips, everything downstream slips. Treat Phase 1 as the project's spine.

---

## 6. Risks & mitigations

| Risk | Likelihood | Mitigation |
|---|---|---|
| Phase-1 engineering (MRQ export, orchestration) takes longer than budgeted | High | Start Phase 1 immediately; timebox; the deck already supports a **beat-board fallback** if the reel isn't fully rendered. |
| Solo bandwidth (~20 hrs/wk) collides with day-job crunch | Medium-High | Sprint-based milestones; keep the slice scope tiny (1 env, 2 chars, 1 prop, 30–60s); cut to 30s if needed. |
| Telemetry numbers don't materialize → cost slide stays placeholder | Medium | Bake telemetry capture into Phase 1 so it's automatic by Phase 4, not a separate task. |
| Style drift (AI output fights the painterly look) | Medium | Lock style refs early; keep MetaHuman strictly as a non-hero fallback seam per K3. |
| Principals unavailable in Q3 / scheduling | Medium | Send I3/I4 outreach in Phase 0; pre-book pitch windows. |

---

## 7. Immediate next actions (this week)

1. Decide **G5 IP ownership**.
2. Pick the **2nd hero character**.
3. Send **I3 + I4** questions to the relevant principals.
4. Run the **per-project catalog migration** and scaffold the CuddlePirates production board.
5. Begin **`runner.py` + film-export** spike (Phase 1 spine).

---

*This plan covers CuddlePirates + Volta only. Bear Suit Man, studio-business formation, and the long-horizon feature/series are explicitly out of the near-term critical path.*
