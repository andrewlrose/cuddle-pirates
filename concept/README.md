# Concept — Visual Style Analysis

Source: 22 Midjourney generations + curated desktop saves from October 2023, manifested in [`inventory.json`](inventory.json).

## Visual style — locked

The existing references converge on a coherent aesthetic. This is **the look** — Section G of Round 2 cannot override these without re-generating reference art.

| Dimension | Value | Evidence |
|---|---|---|
| **Medium feel** | Painterly / illustrated / storybook | Brushy soft edges, no hard lineart, atmospheric perspective |
| **Character proportion** | Plush / doll / chibi — oversized heads, huge round eyes | Consistent across all 3 archetypes |
| **Palette** | Teal-cyan dominant, gold/cream accents, warm reds for costume | Recurring on >80% of refs |
| **Lighting** | Backlit moons, dreamy bloom, volumetric clouds | Captain-on-deck-at-sunset framing common |
| **Costume** | Tricorn hats, captain coats, epaulettes, beards on most refs | Old-world pirate iconography played sincere |
| **Environment language** | Sea-as-cloudscape, "vast seas of imagination" — ocean and sky bleed together | Prompt-level + visual confirmation |
| **Tone register** | Whimsy + melancholy (a knowing innocence, not infantile) | Adventure Time / Mark Ryden / Jean-Baptiste Monge adjacency |

## Pipeline implications (settles Round 2 questions)

- **K3 — RESOLVED:** Style is stylized plush, not photoreal. Custom stylized
  rigs are the default; MetaHuman is the fallback abstraction seam.
- **K4 — RESOLVED:** Concept (Midjourney) → Mesh → handcrafted UE5 lookdev.
  The bedroom environment for the pilot episode is the demo hero env.
- **Demo hero environment:** Juniper's bedroom (not a ship deck — corrected from
  earlier inference pass).

## MJ Username Artifact — The "Doctor" Prefix

`"doctor"` appearing at the start of every prompt string in the 2023 MJ outputs
is simply Andy's **Midjourney username**, which Midjourney automatically prepends
to all image filenames and prompt records. It has no creative meaning whatsoever
— not a character title, not a style direction. Ignore it entirely when reading
any prompt signature in this project.

## Character Archetypes (corrected — napkin-canonical)

The real canon roster comes from the napkin. The MJ images map as follows:

1. **Sir Fuzzy Drake** — 4 images. Canon name confirmed (Sir Francis Drake).
   The visual development in these refs is the most on-model for the napkin.
2. **Anne Bunny** — 4 images (originally labeled "Bunny Pirate"). Maps to
   Anne Bonny → Anne Bunny from the napkin roster. Anthropomorphic bunny form.
3. **MJ Experiment — Captain archetype** — 12 images (originally "Doctor Suave
   Charming"). Unmapped. Possible visual reference for Jean LaFluffe or the lead
   captain character once the crew lead is decided. Do not use this as a character
   name.

## Treatment in Volta catalog (when per-project catalog ships)

Each archetype above maps to a `Character` in Volta with:
- `tier=REFERENCE` initially (concept seed, not approved hero)
- `approval_status=pending` until Andy promotes
- `references=[...]` populated from `inventory.json` paths
- Promotion path: `REFERENCE → CONCEPT → MODEL → RIG → HERO`
