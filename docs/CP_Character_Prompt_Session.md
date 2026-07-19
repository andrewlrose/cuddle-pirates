# Cuddle Pirates — MJ Character Design Session
## Parallel Session | v6.1 | Phase 1 Portraits → Phase 2 Expressions → Phase 3 Ensemble

**Session goal:** Lock canonical portrait for each of the Core 5. Chain `--cref` from best result.
**Priority order:** Drake → Bunny → LaFluff → Vasco → Marco
**Tool:** Midjourney v6.1 (see Model note below)

---

## BEFORE YOU START — Prep Checklist

### Existing reference images (2023 vintage, usable as `--cref`)
- **Drake (4 images):** `E:/OneDrive/Backup_2023oct22/AI/doctor_sir_fuzzy_drake_*.png`
- **Bunny (4 images):** `E:/OneDrive/Backup_2023oct22/AI/doctor_the_bunny_pirate_*.png`
- **LaFluff candidate (12 images):** `E:/OneDrive/Backup_2023oct22/AI/doctor_suave_charming_cuddle_pirate_*.png`
  - ⚠️ **Confirm with Andy:** These 12 images are unmapped — likely Jean LaFluff. Use as `--cref` only after confirming.
- **Vasco + Marco:** No existing reference. Fresh generation only.

### How to use existing images as `--cref`
1. Drag the file into MJ bot channel in Discord → press Enter to send
2. Right-click the uploaded image → **Copy Image Link**
3. Paste URL into prompt as: `--cref [URL] --cw 100`
4. After locking a good new-generation portrait, upload to Imgur → use that URL for all further shots

### Model note
- `--v 6.1` — proven for painterly illustration, good character consistency
- `--niji 6` — alternative if results feel too photographic; optimized for anime/illustrated style
- Run one batch each for v6.1 and niji 6 on Drake to compare before committing

---

## GLOBAL STYLE BLOCK
*Paste this at the end of every CP prompt*

```
bright children's book illustration,
watercolor wash with gouache accents, loose confident linework,
thick friendly outlines, soft brushy edges, no harsh shadows,
warm palette — coral, gold, teal, cream, navy,
painterly storybook aesthetic, whimsy and high adventure,
tactile and huggable, characters feel like plush toys come to life,
Quentin Blake gestural energy, Oliver Jeffers warmth,
Jon Klassen quiet wit, Mary Blair Disney color architecture
```

---

## GLOBAL NEGATIVE PROMPT
*Paste into the /imagine negative field for every generation*

```
photorealistic, 3D render, CGI, harsh linework, cold palette,
dark grim atmosphere, hyperdetailed, anime, manga style,
hard leather, metal buckles, scary, horror, adult content,
realistic fur texture, movie poster
```

---

---

## CHARACTER 1 — SIR FUZZY DRAKE

### Phase 1A — Portrait (establish canonical look)

```
Sir Fuzzy Drake the Cuddle Pirate captain, a strong strapping teddy bear in full captain's regalia,
majestic captain's hat with white feather plume, billowing deep navy pirate coat with gold trim,
finely groomed brown beard, commanding posture, chest out, gazing toward the horizon,
chibi proportions — oversized rounded head, huge expressive eyes, small sturdy body,
warm soft brown teddy bear fur, plush stuffed animal texture throughout,
soft fuzzy pirate costume — no hard leather no metal — all soft plush fabric,
gold epaulettes, burgundy coat lining,
bright children's book illustration,
watercolor wash with gouache accents, loose confident linework,
thick friendly outlines, soft brushy edges, no harsh shadows,
warm palette — coral, gold, teal, cream, navy,
painterly storybook aesthetic, whimsy and high adventure,
tactile and huggable, characters feel like plush toys come to life,
Quentin Blake gestural energy, Oliver Jeffers warmth,
Jon Klassen quiet wit, Mary Blair Disney color architecture
--ar 2:3 --v 6.1
```

> **With 2023 cref (recommended first batch):** append `--cref [drake-2023-url] --cw 100`

---

### Phase 1B — Expression Sheet (run after portrait is locked)
*Replace the pose/expression line only. Keep everything else identical. Use locked portrait as `--cref`.*

**Mood 1 — The Monologue** (mid-speech, one arm extended, crew not listening):
```
[...same prompt...] mid dramatic monologue, one arm extended toward the horizon,
expression passionate and absolute, crew clearly not paying attention in background
--cref [LOCKED-DRAKE-URL] --cw 100 --ar 2:3 --v 6.1
```

**Mood 2 — Sheepish** (redirected by Anne Bunny, slightly caught out):
```
[...same prompt...] slightly sheepish expression, one hand raised in partial surrender,
interrupted mid-monologue, mouth open, dignity slightly compromised
--cref [LOCKED-DRAKE-URL] --cw 100 --ar 2:3 --v 6.1
```

**Mood 3 — Brooding** (quiet, alone, staring at the horizon):
```
[...same prompt...] quiet brooding expression, standing alone at the ship's prow,
staring at the horizon, weight of command visible, the hint of a princess in his lineage
--cref [LOCKED-DRAKE-URL] --cw 100 --ar 2:3 --v 6.1
```

---

---

## CHARACTER 2 — ANNE BUNNY

### Phase 1A — Portrait (establish canonical look)

```
Anne Bunny the Cuddle Pirate First Mate, an anthropomorphic rabbit in practical pirate adventuring gear,
fitted utility vest with coral trim, soft pirate blouse — practical with a touch of femininity,
soft fluffy cream tail slightly raised — she is thinking,
clipboard tucked under one arm, scanning the situation with quiet confident authority,
chibi proportions — oversized rounded head, alert long ears perked upward, wide determined eyes,
warm cream and tan rabbit fur with coral accents throughout,
soft fuzzy pirate costume — no hard leather no metal — all soft plush fabric,
bright children's book illustration,
watercolor wash with gouache accents, loose confident linework,
thick friendly outlines, soft brushy edges, no harsh shadows,
warm palette — coral, gold, teal, cream, navy,
painterly storybook aesthetic, whimsy and high adventure,
tactile and huggable, characters feel like plush toys come to life,
Quentin Blake gestural energy, Oliver Jeffers warmth,
Jon Klassen quiet wit, Mary Blair Disney color architecture
--ar 2:3 --v 6.1
```

> **With 2023 cref (recommended first batch):** append `--cref [bunny-2023-url] --cw 100`

---

### Phase 1B — Expression Sheet (run after portrait is locked)

**Mood 1 — Mission Face** (clipboard in hand, assessing, ears forward):
```
[...same prompt...] clipboard raised, assessing the mission with focused intensity,
ears forward and attentive, expression calm and completely in control
--cref [LOCKED-BUNNY-URL] --cw 100 --ar 2:3 --v 6.1
```

**Mood 2 — Compassion Break** (kneeling to a child's level, mission softening):
```
[...same prompt...] kneeling down to a child's eye level, expression softening into genuine warmth,
the mission paused, clipboard lowered, the softness breaking through the stage director
--cref [LOCKED-BUNNY-URL] --cw 100 --ar 2:3 --v 6.1
```

**Mood 3 — The Cold Stare** (perfectly still, ears flat, one raised eyebrow — she has not raised her voice):
```
[...same prompt...] perfectly still, ears flat back, one eyebrow raised,
expression absolutely calm — colder than anger, she has not raised her voice,
the crew knows they have made an error
--cref [LOCKED-BUNNY-URL] --cw 100 --ar 2:3 --v 6.1
```

---

---

## CHARACTER 3 — JEAN LAFLUFF

> ⚠️ **Confirm before running:** Check `E:/OneDrive/Backup_2023oct22/AI/doctor_suave_charming_*.png`
> — if any of those 12 images match the LaFluff visual direction, use best one as `--cref`.

### Phase 1A — Portrait (establish canonical look)

```
Jean LaFluff the Cuddle Pirate grifter, a tall slender teddy bear in the finest pirate clothes in any room,
aristocratic pirate coat in rich gold and burgundy — far beyond what any mission requires,
well-groomed dark mustache, a permanent twinkle in his eye, one hand resting on his lapel,
a playing card tucked in the breast pocket, a rose in the coat buttonhole,
chibi proportions — slightly elongated silhouette for elegance, expressive hands, warm brown teddy bear fur,
soft luxurious fuzzy pirate costume — no hard leather no metal — all soft plush fabric,
bright children's book illustration,
watercolor wash with gouache accents, loose confident linework,
thick friendly outlines, soft brushy edges, no harsh shadows,
warm palette — coral, gold, teal, cream, navy,
painterly storybook aesthetic, whimsy and high adventure,
tactile and huggable, characters feel like plush toys come to life,
Quentin Blake gestural energy, Oliver Jeffers warmth,
Jon Klassen quiet wit, Mary Blair Disney color architecture
--ar 2:3 --v 6.1
```

---

### Phase 1B — Expression Sheet

**Mood 1 — The Lean** (leaning on one elbow, half-smile, perfectly at ease):
```
[...same prompt...] leaning on one elbow, half-smile, perfectly comfortable in any room,
expression says he has already assessed the situation and found it amusing
--cref [LOCKED-LAFLUFF-URL] --cw 100 --ar 2:3 --v 6.1
```

**Mood 2 — Unbothered Exit** (turning away mid-mission, completely unconcerned):
```
[...same prompt...] turning away from the group mid-mission, coat swirling slightly,
expression of serene contentment — he has spotted something more interesting,
he will absolutely come back
--cref [LOCKED-LAFLUFF-URL] --cw 100 --ar 2:3 --v 6.1
```

**Mood 3 — The Return** (leaping back in, coat billowing, no explanation offered):
```
[...same prompt...] leaping dramatically back into the scene, coat billowing behind him,
expression bright and fully committed, offering zero explanation for his absence,
one hand outstretched toward the crew
--cref [LOCKED-LAFLUFF-URL] --cw 100 --ar 2:3 --v 6.1
```

---

---

## CHARACTER 4 — VASCO PAJAMA

### Phase 1A — Portrait (establish canonical look)
*No existing reference. Fresh generation only.*

```
Vasco Pajama the Cuddle Pirate navigator and inventor, a small slender teddy bear with round spectacles,
perpetually furrowed brow — always running calculations, always worried, always correct,
tool belt with small gadgets and rolled blueprints tucked in, teal-olive pirate coat,
compact slightly hunched posture, pencil tucked behind one ear, blueprint curl visible at his side,
chibi proportions — compact rounded head, large worried eyes magnified behind round lenses,
warm brown teddy bear fur, soft fuzzy pirate costume — no hard leather no metal — all soft plush fabric,
bright children's book illustration,
watercolor wash with gouache accents, loose confident linework,
thick friendly outlines, soft brushy edges, no harsh shadows,
warm palette — coral, gold, teal, cream, navy,
painterly storybook aesthetic, whimsy and high adventure,
tactile and huggable, characters feel like plush toys come to life,
Quentin Blake gestural energy, Oliver Jeffers warmth,
Jon Klassen quiet wit, Mary Blair Disney color architecture
--ar 2:3 --v 6.1
```

---

### Phase 1B — Expression Sheet

**Mood 1 — Deep Work** (bent over blueprints, pencil in mouth, world has ceased to exist):
```
[...same prompt...] bent entirely over a large blueprint, pencil clamped in his teeth,
spectacles slid down his nose, expression of absolute tunnel-vision concentration
--cref [LOCKED-VASCO-URL] --cw 100 --ar 2:3 --v 6.1
```

**Mood 2 — Vindicated** (arms raised — DO YOU SEE? — expression of triumph):
```
[...same prompt...] arms raised above his head, spectacles pushed up in excitement,
expression of absolute vindication — DO YOU SEE, arms wide, slightly unhinged triumph
--cref [LOCKED-VASCO-URL] --cw 100 --ar 2:3 --v 6.1
```

**Mood 3 — The Aftermath** (staring at wreckage, glasses askew, eye twitching):
```
[...same prompt...] staring at a pile of wreckage off-frame, spectacles knocked askew,
one eye twitching slightly, expression of barely-controlled engineering grief,
Marco Pillow's influence is visible even in his absence
--cref [LOCKED-VASCO-URL] --cw 100 --ar 2:3 --v 6.1
```

---

---

## CHARACTER 5 — MARCO PILLOW

### Phase 1A — Portrait (establish canonical look)
*No existing reference. Fresh generation only.*

```
Marco Pillow the Cuddle Pirate second mate, a rotund cheerful teddy bear,
bright cherry-red bandana tied loosely around his neck, deep green vest over a fuzzy cream pirate shirt,
wide infectious smile — constant, absolute, and completely sincere,
arms slightly spread wide in welcoming openness, holding something carelessly in one hand,
chibi proportions — perfectly round oversized head, big warm eyes, body larger than any situation requires,
warm golden-brown teddy bear fur, soft fuzzy pirate costume — no hard leather no metal — all soft plush fabric,
bright children's book illustration,
watercolor wash with gouache accents, loose confident linework,
thick friendly outlines, soft brushy edges, no harsh shadows,
warm palette — coral, gold, teal, cream, navy,
painterly storybook aesthetic, whimsy and high adventure,
tactile and huggable, characters feel like plush toys come to life,
Quentin Blake gestural energy, Oliver Jeffers warmth,
Jon Klassen quiet wit, Mary Blair Disney color architecture
--ar 2:3 --v 6.1
```

---

### Phase 1B — Expression Sheet

**Mood 1 — The Charge** (barreling forward, arms wide, enormous smile, absolute sincerity):
```
[...same prompt...] barreling forward toward the viewer, arms spread wide, enormous smile,
expression of pure wholehearted enthusiasm — he is about to help in a way that will not help
--cref [LOCKED-MARCO-URL] --cw 100 --ar 2:3 --v 6.1
```

**Mood 2 — The Observation** (finger raised, identifying the fatal flaw, completely innocent):
```
[...same prompt...] one finger raised, expression of helpful helpfulness, completely unaware
that what he is about to say will devastate Vasco — he has identified the flaw, out loud,
in front of everyone
--cref [LOCKED-MARCO-URL] --cw 100 --ar 2:3 --v 6.1
```

**Mood 3 — Sincere Apology** (both hands clasped, surrounded by wreckage, he absolutely means it):
```
[...same prompt...] both hands clasped in front of his chest, surrounded by visible wreckage,
expression of deep and absolute sincerity — he is genuinely sorry, he means it completely,
the smile is slightly softer but still there
--cref [LOCKED-MARCO-URL] --cw 100 --ar 2:3 --v 6.1
```

---

---

## PHASE 2 — ENSEMBLE SHOTS
*Run after all 5 portraits are locked. Use all `--cref` URLs together.*

### The Fluffy Dutchman — Crew Shot

```
the Cuddle Pirates crew gathered at the prow of a soft plush pirate ship sailing through cloudscape seas,
left to right: Sir Fuzzy Drake (tall, navy coat, captain's hat), Anne Bunny (cream rabbit, utility vest, clipboard),
Jean LaFluff (slender, gold coat, mustache), Vasco Pajama (small, spectacles, tool belt),
Marco Pillow (round, red bandana, green vest, wide smile),
all five chibi proportions — oversized heads, plush stuffed animal textures,
the ship is soft rounded wood — no hard metal — sails in cream and teal,
ocean and sky blending in dreamy watercolor wash, warm teal and gold,
bright children's book illustration,
watercolor wash with gouache accents, loose confident linework,
thick friendly outlines, soft brushy edges, no harsh shadows,
warm palette — coral, gold, teal, cream, navy,
painterly storybook aesthetic, whimsy and high adventure,
tactile and huggable, characters feel like plush toys come to life,
Quentin Blake gestural energy, Oliver Jeffers warmth,
Jon Klassen quiet wit, Mary Blair Disney color architecture
--ar 16:9 --v 6.1
```

> Add `--cref [best ensemble ref]` once one exists. For first pass, omit `--cref`.

---

## SESSION WORKFLOW SUMMARY

```
Phase 1A: Drake portrait (with 2023 cref)     → pick best → upload to Imgur → save URL
Phase 1A: Bunny portrait (with 2023 cref)     → pick best → upload to Imgur → save URL
Phase 1A: LaFluff portrait (confirm 2023 cref) → pick best → upload to Imgur → save URL
Phase 1A: Vasco portrait (fresh)               → pick best → upload to Imgur → save URL
Phase 1A: Marco portrait (fresh)               → pick best → upload to Imgur → save URL

Phase 1B: Expression sheets for each character (use locked portrait as --cref)
Phase 2:  Ensemble shot (Fluffy Dutchman crew)
Phase 3:  Scene shots — Juniper's bedroom intro, Fluffy Dutchman establishing, heist sequence
```

---

## OPEN QUESTIONS (flag before Phase 2)

| # | Question | Blocks |
|---|---|---|
| 1 | Confirm LaFluff mapping: do the 12 "suave charming" images match Jean LaFluff direction? | Phase 1A LaFluff cref |
| 2 | Demo reel hero cast: character 2 alongside Drake — Anne Bunny confirmed? | Rig priority |
| 3 | v6.1 vs. niji 6 — run one Drake batch in each and pick preferred aesthetic | All subsequent generations |

---

*v1.0 — S176 June 2026. Parallel session to BSM Phase 1 character sheets.*
