# Volta — Pitch Deck, Wave 1
## For: VFX Producer · Multi-disciplinary Artist · FX Editor

**Version:** Draft v1 — 2026-04-25
**Status:** Working draft. Telemetry numbers are placeholders until execution-path item 5 is live.
**Not in this deck:** Senior VP Supervisor section (Wave 2, after I3 is answered).

---

---

## SLIDE 1 — OPEN WITH THE REEL

> **[PLAY VERTICAL SLICE — 30–60 seconds]**

*The Fluffy Dutchman drifts down through moonlit clouds toward a bedroom window.
Legs stick out the bottom, churning.*

*Sir Fuzzy Drake leads the crew through the window one by one.*

*The hall light flickers. Mom is moving.*

*The Pirates freeze against the wall — plastered flat, not breathing.*

*Light passes. Silence.*

*They land on the bed.*

*They bow for Juniper. Then the ragdoll acrobatics begin.*

*Juniper laughs silently — she cannot wake Mom.*

*The Pirates bow again. The show is over.*

---

**Speaker note:** No introduction before the reel. Walk in, dim the lights, play it.
The reel explains everything; the rest of the deck explains how we built it.

If the reel is not yet rendered: show the beat board (one image per beat above)
with scratch audio or silence. The sequence is the argument.

---

---

## SLIDE 2 — THE SHOW

### Cuddle Pirate Theater

> *"Every night, somewhere between awake and asleep, a band of plushie pirates
> commandeer bedtime. They dodge the parents, perform ragdoll acrobatics for the
> children who can't sleep, tell a bedtime story — and once everyone is out,
> they steal every pillow and blanket in the room and sail home for the most
> legendary pillow fight anyone has ever seen."*

**Format:** 2–4 minute animated short · Children's series
**Style:** Painterly plush / storybook — stylized, not photoreal
**Tone:** Heist comedy first, warmth second. *The Muppets* meet *Pee-wee's Playhouse* in a bedroom at 9pm.
**Pilot episode:** *The Sock-topuss* — Juniper's bedroom. One night. One missing sock.

**What we just showed you was made through Volta.**

---

---

## SLIDE 3 — THE PROBLEM

### What independent animation actually costs

The traditional path for a boutique studio trying to make a 2–4 minute
animated short at this quality level:

| Pain Point | Reality |
| --- | --- |
| **Pipeline** | Designed for 200-person studios. Scaled down, it breaks. |
| **AI tools** | Black boxes. The artist doesn't own the output. No audit trail. |
| **Cost visibility** | You know the invoice. You don't know the per-stage cost until post-production. |
| **Hardware** | Cloud render farms: metered, unpredictable, margin-destroying. |
| **Iteration speed** | Waiting on renders to get notes. Notes kill momentum. |

**The result:** Studios at this scale need a network deal or VC before a single
frame is finished — or they never get off the ground.

**Volta is the other path.**

---

---

## SLIDE 4 — THE SOLUTION: VOLTA

### AI-augmented animation pipeline on local compute

Volta is the production orchestration layer we built for this studio.
It does one thing: it makes a 5-person boutique operate like a 50-person pipeline.

| Principle | What it means |
| --- | --- |
| **Local-first** | M6 Pro hardware. No cloud meter running on every frame. |
| **AI-augmented, not AI-driven** | Every AI step has a human override. The artist is the author. |
| **Approval-gated** | Nothing promotes to the next stage without a sign-off. No black boxes get through. |
| **Cost-visible** | Per-stage telemetry: compute hours, AI credits, GPU-seconds — tracked from INGEST to EXPORT. |
| **Reusable** | Every approved asset lives in the per-project catalog. Original IP + service work both pull from the same asset library. |

**The moat:** AI orchestration on owned hardware changes the cost structure at the bottom end of the market. A boutique with Volta has the leverage that used to require a studio deal.

---

---

## SLIDE 5 — THE PIPELINE

### How Cuddle Pirates was built

*Six stages. One project. Every asset you saw in the reel came through this.*

```
INGEST → RIG → ANIM → FX → COMP → EXPORT
```

---

### INGEST

**What it does:** Takes concept art and reference images, ingests them into the
per-project Volta catalog, assigns tiers (REFERENCE → CONCEPT → MODEL → RIG → HERO),
and creates the approval queue.

**Cuddle Pirates example:**
- 22 Midjourney character concepts for Sir Fuzzy Drake, Anne Bunny, and the Captain archetype → ingested as `tier=REFERENCE`
- Juniper's bedroom: 8 environment refs → ingested as `tier=REFERENCE`
- Every asset sits in `.volta/catalog.db` with provenance, approval status, and cost attribution from day one

**Key feature:** Nothing moves to the next stage until it's approved. The catalog
is the single source of truth. No "we used the wrong version" at comp.

---

### RIG

**What it does:** Takes approved concept into 3D. Concept (MJ) → Mesh (Meshy /
photogrammetry cleanup) → Blender → custom UE5 stylized rig.

**Cuddle Pirates example:**
- Sir Fuzzy Drake: MJ captain concept → Meshy 3D base → Blender cleanup + proportion correction → UE5 custom rig
- Rig is **stylized-first** — plush proportions, huge round eyes, cloth pajama simulation
- No MetaHuman dependency. MetaHuman is the fallback abstraction seam *only* for photoreal sub-assets (e.g., a cameo human hand in frame). The hero characters are fully custom.
- Cloth sim baked in at rig stage: the pajama fabric, the captain's coat, The Fluffy Dutchman's pillowcase hull

**Key feature:** Asset promotion path is timestamped. You can show exactly how long
each stage took, what it cost, and who approved the move.

---

### ANIM

**What it does:** Hero rig → final performance. Physical comedy timing,
silent performance for the heist sequences, cloth interaction with environment.

**Cuddle Pirates example:**
- The infiltration sequence: freeze-against-wall requires full-body ragdoll physics response to simulated sound event
- Ragdoll acrobatics on the bed: timing is silent comedy — no dialogue, performance is entirely physical
- The bow: the Pirates know they're performing. The animation sells the theatricality.

**Key feature:** ANIM inherits cloth sim from RIG. No re-simulation at this stage.
Iteration on performance without re-baking fabric.

---

### FX

**What it does:** Soft-body and cloth simulation on hero assets in environment,
plus any secondary FX (dust motes, light shafts, practical in-world effects).

**Cuddle Pirates example:**
- Pillowcase hull of The Fluffy Dutchman: cloth sim on a moving prop with legs driving contact underneath
- Pajama sleeves catching air during acrobatics
- The Fluffy Dutchman's rigging: rope and sail physics as the ship maneuvers

**Key feature:** FX is scoped. No VDB explosions, no rigid body debris. Everything
in-scope is cloth and soft-body — well-understood, controllable, iteration-friendly.

---

### COMP

**What it does:** Environment + character + FX → final image. Bedroom lighting rig,
atmosphere, the two competing light sources that drive the comedy.

**Cuddle Pirates example:**
- Two light sources as story devices:
  - **Warm hall light** (threat): orange, hard-edged, moves when Mom is moving
  - **Cool window moonlight** (safe): blue-grey, soft, always present
- The comedic timing of the freeze-against-wall beat is entirely a lighting cut.
  The warm light creeps into frame → Pirates freeze. Light retreats → they exhale.
- All COMP work in UE5. Handcrafted lookdev, not procedural generation.

---

### EXPORT

**What it does:** Final delivery package from UE5 → editorial-ready output.

**What Volta delivers — three lanes, always-on:**

| Output | Format | Notes |
| --- | --- | --- |
| 4K master frames | EXR sequence | Full-float, comp-ready, re-deliverable to any future spec |
| MP4 dailies | H.264 / H.265 | Review-ready, same-day, no transcode step |
| Avid round-trip | AAF + audio stems | Timecoded, multi-track, drops straight into Media Composer |
| DaVinci round-trip | XML + audio stems | Timeline-accurate, color-managed for Resolve's node pipeline |

**The principle:** Volta doesn't ask which NLE you use. It delivers all four
formats on every export. You drop in what you need and ignore the rest.
Changing tools mid-production is a config switch, not a re-pipeline.

**On audio:** VO, score, and SFX are in-scope for the final episode. EXPORT
delivers audio as discrete stems (dialogue / score / SFX) so the editor's
mix session has full separation from day one. The demo reel ships with
scratch audio by default; stems follow when the final mix is locked.

---

---

## SLIDE 6 — COST MODEL

### For the VFX Producer

*What did the vertical slice cost to produce through Volta?*
*Figures below are benchmarked estimates based on M6 Pro performance and
current Meshy/ComfyUI credit pricing. Direct compute costs only — artist
time is founder-rate and excluded from this model.*

| Stage | Compute time | AI credits | GPU-seconds | Est. cost |
| --- | --- | --- | --- | --- |
| INGEST (22 concept refs) | 15 min | — | — | < $1 |
| RIG — Sir Fuzzy Drake | 8 hrs total | 10 Meshy credits | 5,400 s | ~$8 |
| RIG — Juniper's Bedroom | 6 hrs total | — | 4,800 s | ~$5 |
| ANIM — infiltration sequence | 10 hrs total | — | — | ~$3 |
| FX — cloth sim passes | 4 hrs total | — | 21,600 s | ~$7 |
| COMP — bedroom lighting | 5 hrs total | — | 28,800 s | ~$10 |
| EXPORT — 4K + MP4 dailies | 45 min | — | 2,400 s | ~$1 |
| **TOTAL — 30–60s reel** | **~34 hrs** | **10 credits** | **~63,000 s** | **~$35** |

*Cost = Meshy credits + marginal M6 power draw. Hardware already owned and amortized.*

**Extrapolated to full episode (2–4 min):**

| Scenario | Projected cost | Assumptions |
| --- | --- | --- |
| 5× linear scale | ~$175 | No asset reuse, fresh environment each episode |
| With catalog reuse (realistic) | ~$90–110 | Bedroom env, hero rigs, FX rigs all carry forward |
| Cloud render equivalent (AWS Deadline) | ~$900–1,200 | g4dn.xlarge spot pricing, comparable 4K quality |
| Traditional boutique outsource | ~$2,000–5,000 | Render farm + pipeline management + retakes |

**The argument:**
Volta on M6 at ~$100 fully burdened vs. $900–1,200 cloud-equivalent for a
full 2–4 minute episode. The gap is the studio's operating margin — or the
difference between needing a network deal and not needing one.

Every asset approved in episode 1 lives in the catalog. Episode 2 starts
with the rigs, environment, and FX already signed off. The per-episode cost
drops with every episode in the series. The cloud bill doesn't.

---

---

## SLIDE 7 — THE ARTIST'S VIEW

### For the Multi-disciplinary Artist

*"Concept to rigged hero character in a day."*

**The Sir Fuzzy Drake promotion path:**

```
MJ concept image (existing)
        ↓  [INGEST — ~5 min, human review]
  catalog.db tier=REFERENCE
        ↓  [APPROVAL: Andy promotes to CONCEPT]
  Meshy 3D base mesh generation
        ↓  [~20 min, automated + human QC]
  Blender cleanup + proportion correction
        ↓  [human artist — ~2–4 hrs]
  catalog.db tier=MODEL
        ↓  [APPROVAL: artist promotes to RIG]
  UE5 custom stylized rig
  (cloth sim, plush proportions, facial rig)
        ↓  [human artist — ~3–4 hrs]
  catalog.db tier=RIG
        ↓  [APPROVAL: promotes to HERO]
  HERO — production-ready
```

**Total elapsed:** 1 day, one artist.
**AI steps:** Meshy 3D base generation (20 min). That's it.
**Everything else:** Human. Supervised. Approved. Owned.

---

### No black boxes. You are the author at every stage.

| What AI does in Volta | What AI does NOT do |
| --- | --- |
| Generate a rough 3D base from concept | Make creative decisions |
| Suggest asset organization | Approve anything |
| Track cost attribution per asset | Generate final animation |
| Surface the next approval item in the queue | Replace the artist |

**The approval gate is real.** Nothing in Volta promotes to the next stage without
a human decision. The artist's name is on the asset. The artist's choices are in
the catalog. The audit trail exists from concept to export.

---

---

## SLIDE 8 — THE REEL, REVISITED

> **[PLAY AGAIN — optional, if the room wants it]**

*Everything you just heard about the pipeline — every stage, every tool —
produced what you saw at the top.*

*The bedroom is the demo environment.*
*Sir Fuzzy Drake is the demo hero character.*
*The Fluffy Dutchman is the demo hero prop.*
*The infiltration sequence is the demo animation.*

*This is not a capability roadmap. This is what Volta does.*

---

---

## SLIDE 9 — THE TEAM

**Andy Rose** — Pipeline Architect / Studio Lead
Mocap post supervisor (Lightspeed LA). Vicon/OptiTrack + MotionBuilder background.
Built Volta on M6 from scratch. Running the studio end-to-end.

---

`[PRINCIPAL 1 — VFX Producer]`
*[Add bio — what they bring to the production management layer]*

---

`[PRINCIPAL 2 — Multi-disciplinary Artist]`
*[Add bio — what they bring to the creative execution layer]*

---

`[PRINCIPAL 3 — FX Editor]`
*[Add bio — what they bring to the editorial / delivery layer]*

---

`[PRINCIPAL 4 — Senior VP Supervisor]`
*[Wave 2 principal — joins after first three pitches land]*

---

---

## SLIDE 10 — THE ASK

### What joining means

This is an **equity partnership.** No salaries in the garage phase.
The studio is bootstrapped from Andy's savings. That means:

- You are a founder, not a hire
- The IP we produce is studio IP — we own it together
- The Volta pipeline is the asset; the content we make with it is how we prove it

---

### What's built

| Item | Status |
| --- | --- |
| Volta pipeline (INGEST → EXPORT) | Scaffolded — in active development |
| CuddlePirates project catalog | Initialized, M1 complete |
| Story bible (pilot episode) | Written — characters, world, 12-chapter structure |
| Concept references (22 MJ images) | Cataloged in inventory.json |
| Demo reel (vertical slice) | `[IN PRODUCTION — Q3 2026 target]` |
| M6 local compute | `[In progress]` |

---

### What the studio looks like in 18 months

A boutique animation studio with:
- One completed animated short (the pilot episode)
- A proven, documented pipeline that other studios can license
- Enough original IP to shop the series
- A cost model that sustains original content without a network deal first

---

### The pitch date: Q3 2026

The reel is the deliverable. The reel proves the pipeline.
The pipeline proves the studio.

**Let's talk.**

---

---

## APPENDIX A — Open Items (fill in before final presentation)

| ID | Item | Owner | Needed for |
| --- | --- | --- | --- |
| I4 | FX Editor NLE + round-trip format (Avid / DaVinci / Premiere) | Andy → ask editor | EXPORT slide (Slide 5 / EXPORT section) |
| TELEMETRY | Volta stage cost numbers | Engineering — exec path item 5 | Cost model slide (Slide 6) |
| REEL | Vertical slice render | Production | Slides 1, 8 |
| BIOS | Principal bios for team slide | Each principal | Slide 9 |

---

## APPENDIX B — What This Deck Does NOT Cover

- **G5 / IP ownership** — not a concern right now, excluded per Andy's direction
- **I3 / Senior VP Supervisor** — Wave 2 only; needs a separate deck section after his gold-standard pipeline preference is known
- **J1/J2 / Volta as product** — internal-only for now; don't bring up in Wave 1 unless asked
- **Series bible depth** — the full 12-chapter pilot structure, extended character roster, and world-building details live in `story-bible/`. Available if principals ask to go deeper.

---

## APPENDIX C — Talking Points by Principal

### VFX Producer
- Lead with the cost model slide (Slide 6)
- Emphasize: per-stage telemetry means you know where the money went *before* the invoice arrives
- Emphasize: catalog reuse = margin on episode 2 is better than episode 1 because the rigs are already approved
- The production management layer of Volta is partially their design problem — invite them in: "We want your approval-gate model to match how you actually run a floor"

### Multi-disciplinary Artist
- Lead with the Sir Fuzzy Drake promotion path (Slide 7)
- Emphasize: the AI step is Meshy (20 min, rough base mesh). Everything after that is the artist.
- Emphasize: the stylized rig is custom — this is not a MetaHuman wrapper. The artist owns the shape.
- This person cares about creative control above everything else. The "no black boxes" argument is the whole pitch for them.
- Invite them: "Which stage do you want to own? Tell us where you want to be in this pipeline."

### FX Editor
- Lead with the EXPORT slide (Slide 5 / EXPORT section)
- Ask the I4 question in the pre-pitch conversation: "Before we finalize the deck — what's your NLE? We've built both Avid and DaVinci round-trip lanes."
- Emphasize: MP4 dailies are same-day, always-on — they can cut a review assembly while COMP is still running
- Emphasize: 4K EXR masters mean any future remaster or deliverable spec change is a re-comp, not a re-render
- This person will want to know about the audio pipeline: VO, score, SFX are all in scope for the final episode (per K2). For the demo reel, audio is scratch-to-locked workflow.
