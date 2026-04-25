# Principal-Routed Open Questions

Items from Round 2 that **cannot be answered by Andy** — they need a real conversation with the relevant principal. Each entry stays open until the principal answers; do not invent answers, do not let these block the pipeline build.

Last updated: **2026-04-25** (S39).

---

## Senior VP Supervisor

### I3 — Gold-standard pipeline reference
> *Source: Round 2 Section I, question 3*

**Question:** Do they have a specific pipeline they consider gold standard? Examples:
- ILM StageCraft (LED-volume virtual production)
- Disguise (real-time content / xR stages)
- Wētā Wellington workflow (Manuka / Gazebo / proprietary stack)
- Epic / The Mandalorian-style UE-driven VP
- Something else, or no canonical favorite

**Why we need it:** This is the most technically skeptical audience of the four. The deck section pitched at this principal needs to either (a) speak their gold standard's vocabulary, or (b) confidently position Volta against multiple gold standards if they're pipeline-agnostic.

**Status:** OPEN — Andy's note: "Need to ask the principal what his gold standard is. He might not have one, being well versed in many pipelines."

**When to ask:** Pre-pitch conversation. After Producer/Artist/Editor pitches land per I5 ordering.

**Fallback if unanswered before deck:** Position Volta as **pipeline-agnostic AI orchestration** — frame the M6/local-compute moat as the differentiator regardless of which gold standard is in the room.

---

## FX Editor

### I4 — Toolchain + round-trip format
> *Source: Round 2 Section I, question 4*

**Question:** Two parts —
1. **NLE:** Avid Media Composer? DaVinci Resolve? Adobe Premiere? Something else?
2. **Round-trip expectation:** EDL? AAF? XML? OMF? Or is MP4 dailies + manual conform acceptable?

**Why we need it:** Volta's `EXPORT` stage has to produce something the editor can drop straight into their cut. If they expect AAF round-tripping with timecode + audio stems, Volta needs that lane in v1. If MP4 dailies are fine, EXPORT can be much simpler.

**Status:** OPEN — Andy's guess: "Avid or DaVinci."

**When to ask:** This principal is in the first-wave pitch group (Producer/Artist/Editor). Ask before the pitch — ideally as a pre-pitch one-on-one so the deck's EXPORT slide reflects their actual toolchain.

**Fallback if unanswered before deck:** Show **both** Avid (AAF) and DaVinci (XML) round-trip lanes as planned outputs, with MP4 dailies as the always-on fallback. Multi-format positions the export lane as flexible without committing to one wrong choice.

---

## Tracking

| ID | Principal | Question | Status | Blocked since |
|---|---|---|---|---|
| I3 | Senior VP Supervisor | Gold-standard pipeline reference | OPEN | 2026-04-25 |
| I4 | FX Editor | NLE + round-trip format | OPEN | 2026-04-25 |

When an answer comes in:
1. Move the locked answer into [`round2-answers.md`](round2-answers.md)
2. Mark the row above CLOSED with date
3. Note any deck/pipeline implications in [`../.atlas-bridge/memory.json`](../.atlas-bridge/memory.json) `recent_decisions`
