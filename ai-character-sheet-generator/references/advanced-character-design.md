# Advanced Character Design

## Expression Variants

Beyond the four canonical reference angles, generate expression variants for emotional range:

| Expression | Use Case |
|-----------|----------|
| **Neutral** | Default reference, most scenes |
| **Smiling** | Positive interactions, joy |
| **Serious/Focused** | Work scenes, tension |
| **Angry** | Conflict, confrontation |
| **Surprised** | Plot reveals, reactions |
| **Sad/Pensive** | Emotional beats, loss |

### Expression Prompt Modifier

Append to the base front-view prompt:

```
Expression: [target expression], subtle and natural, not exaggerated.
Eyes conveying [emotion], mouth [specific position].
```

Keep all other attributes identical — only the facial expression changes.

## Wardrobe Variants

When a character changes outfits across scenes, create a separate wardrobe variant sheet rather than modifying the base sheet.

### Wardrobe Sheet Structure

```
CHARACTER: [Name] — Wardrobe Variant [N]: [Label]
BASE SHEET: [Reference to original character sheet]

CLOTHING CHANGE:
  Top:        [New description]
  Bottom:     [New description]
  Footwear:   [New description]
  Accessories: [Changes only — carry forward unchanged items]

ALL OTHER ATTRIBUTES: [Unchanged — reference base sheet]
```

Generate a new front-view reference for each wardrobe variant. Side/back/3-quarter views are optional unless the outfit has distinctive features from those angles (e.g., backpack, cape, back print).

## Multi-Character Ensemble Sheets

When building a cast of characters:

### Ensemble Consistency Rules

1. **Generate all characters in the same session** — model consistency is higher within a single generation run
2. **Use identical lighting and background** across all characters
3. **Establish relative height** — generate a lineup image with all characters side by side
4. **Differentiate deliberately** — ensure each character has at least 3 visually distinct attributes (hair color, clothing palette, build)

### Ensemble Lineup Prompt

```
Full-body lineup of [N] characters standing side by side on neutral gray background.
Left to right:
  Character A: [key distinguishing features, height]
  Character B: [key distinguishing features, height]
  Character C: [key distinguishing features, height]
Soft diffused studio lighting, 35mm lens, full body visible, photorealistic.
```

This establishes relative scale and visual contrast between characters.

## Age Progression

For characters that appear at different ages:

1. Lock **bone structure** (face shape, nose, jawline) — these don't change
2. Modify **age-dependent attributes** — skin texture, hair color/thickness, posture, weight
3. Generate separate sheets for each age bracket
4. Label clearly: `[Name] — Age 25`, `[Name] — Age 55`

## Lighting Variants

The canonical sheet uses neutral studio lighting. For scenes with dramatic lighting, generate additional lighting reference shots:

| Lighting | Prompt Modifier |
|----------|----------------|
| **Golden hour** | Warm golden side light from the left, long shadows, orange rim light |
| **Night/neon** | Cool blue ambient, colored neon rim lights, deep shadows |
| **Overcast** | Flat diffused daylight, no hard shadows, muted colors |
| **Interior warm** | Warm tungsten key light, soft fill, amber tones |
| **Dramatic** | Single hard light from above-right, deep contrast, film noir |

Generate a front-view under each lighting condition to verify the character reads well in different environments.

## Hands and Props

Hands are among the most error-prone elements in AI generation. Reduce errors by:

1. **Specifying hand position explicitly** in every prompt — "hands relaxed at sides, fingers naturally curled"
2. **Locking ring/watch placement** — "silver watch on left wrist, no rings"
3. **Generating a dedicated hand close-up** if the character frequently holds props

### Prop Reference

For characters who carry recurring props (weapon, instrument, bag, phone):

```
Close-up of [CHARACTER NAME]'s hands holding [PROP].
[Hand attributes from character sheet]. [Prop description — material, color, size, condition].
Neutral background, soft lighting, 85mm macro lens, high detail.
```
