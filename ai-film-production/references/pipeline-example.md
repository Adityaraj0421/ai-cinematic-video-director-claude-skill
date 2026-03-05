# Pipeline Example: "The Last Commute"

A complete worked example showing the full pipeline from concept to final production package.

## Concept

> A 30-second cinematic short about a man's final commute through a rain-soaked city at night before leaving town forever. Mood: melancholic, reflective, visually rich.

---

## Stage 1 — Character Design

### Character: Marcus

**Identity:**
```
Name:      Marcus
Role:      Protagonist — departing city dweller
Age Range: Early 30s
Archetype: Quiet professional, emotionally guarded
```

**Locked Visual Attributes:**

| Category | Locked Values |
|----------|--------------|
| Face | Oval face, warm brown skin with natural texture, dark brown deep-set eyes, thick eyebrows, broad nose, full lips, clean-shaven, slight under-eye shadows |
| Hair | Black coily hair, short fade, well-maintained |
| Build | Average height, lean build, slightly rounded shoulders, weary posture |
| Clothing | Charcoal wool overcoat over dark gray hoodie, black jeans, worn white sneakers, black backpack on right shoulder |
| Distinctive | Silver stud earring in left ear, small tattoo of a compass on right wrist |
| Hands | No rings, silver watch on left wrist, short fingernails |

**Front View Prompt:**
```
Front view of a 32-year-old Black man with an oval face.
Warm brown skin with natural texture, dark brown deep-set eyes,
thick eyebrows, broad nose, full lips, clean-shaven, slight under-eye shadows.
Black coily hair, short fade, well-maintained. Lean build, slightly rounded
shoulders, weary posture.
Wearing a charcoal wool overcoat over a dark gray hoodie, black jeans,
worn white sneakers. Black backpack on right shoulder.
Silver stud earring in left ear. Silver watch on left wrist.
Neutral gray studio background, soft diffused lighting,
85mm portrait lens, photorealistic, high detail, no motion blur.
```

*(Side, back, and three-quarter prompts follow the same pattern with angle changed.)*

**Gate: User approves character sheet.**

---

## Stage 2 — Shot Craft

### Scene Breakdown

```
Scene 1 — City street at night
  Location:   Rain-soaked urban street, neon reflections on wet asphalt
  Time:       Late night, after rain, streetlights and neon signs
  Characters: Marcus (alone)
  Emotion:    Melancholic solitude
  Duration:   ~30 seconds total across all shots
```

### Shot List

**Shot 1 — Establishing Wide**

Start Frame Prompt:
```
Wide shot of a rain-soaked city street at night. Wet asphalt reflecting
neon signs and streetlights in blue, pink, and amber. Steam rising from
a subway grate. Empty sidewalk. Deep perspective vanishing point.
Cinematic composition, 24mm lens, deep focus, film grain.
```

Animation Prompt:
```
Camera slowly pushes forward down the empty street. Rain mist drifts
across frame. Neon reflections shimmer on wet ground. Ambient city glow.
```

Camera: Slow dolly push, 24mm, eye level, no shake.
Duration: 5s | Transition: Dissolve

---

**Shot 2 — Medium Tracking**

Start Frame Prompt:
```
Medium shot of Marcus walking along a rain-soaked sidewalk at night.
[PASTE FULL CHARACTER ATTRIBUTES HERE]
Charcoal wool overcoat slightly damp, hood of gray hoodie pulled up
partially. Black backpack on right shoulder. Walking with hands in
coat pockets, weary posture, looking slightly downward.
Wet asphalt reflecting neon in background, 35mm lens, shallow DOF,
cinematic night lighting with cool blue ambient and warm neon rim light.
```

Animation Prompt:
```
Marcus walks steadily forward, camera tracking beside him at waist height.
Subtle handheld motion. His breath is faintly visible in cold air.
Background neon slides past out of focus.
```

Camera: Handheld tracking, 35mm, waist level, subtle shake.
Duration: 6s | Transition: Cut

---

**Shot 3 — Close-Up Reflection**

Start Frame Prompt:
```
Close-up of Marcus's face in profile, looking to the right.
[PASTE FACE ATTRIBUTES HERE]
Rain droplets on his cheek and overcoat collar. Cool blue ambient
light from the left, warm neon orange rim light from the right.
Slight under-eye shadows. Expression: pensive, mouth relaxed, eyes
distant. 85mm lens, very shallow DOF, background completely blurred
into bokeh circles of light.
```

Animation Prompt:
```
Very slow push-in on Marcus's face. His eyes shift slightly, looking
forward. A single rain drop trails down his cheek. Minimal movement —
the shot is about stillness.
```

Camera: Slow dolly push, 85mm, eye level, no shake.
Duration: 4s | Transition: Dissolve

---

**Shot 4 — Wide Departure**

Start Frame Prompt:
```
Wide shot from behind Marcus walking away down a long city street.
[PASTE BUILD AND CLOTHING ATTRIBUTES HERE]
Black backpack on right shoulder, hands in coat pockets. Wet asphalt
stretching ahead, streetlights creating a corridor of warm pools of light.
Steam rising from the ground. The street narrows into a vanishing point.
24mm lens, deep focus, cinematic composition, film grain.
```

Animation Prompt:
```
Marcus continues walking away from camera. Camera remains static.
He slowly diminishes in frame as the distance grows. Ambient steam
drifts across the bottom of frame.
```

Camera: Static, 24mm, chest height, locked off.
Duration: 7s | Transition: Fade to black

---

**Shot 5 — Detail Insert: Compass Tattoo**

Start Frame Prompt:
```
Extreme close-up of a right wrist with a small compass tattoo.
Warm brown skin with natural texture. Rain droplets on skin surface.
The compass needle points forward. Charcoal wool overcoat sleeve
pulled back slightly. Cool blue ambient light, soft focus background.
85mm macro lens, very shallow DOF, photorealistic, high detail.
```

Animation Prompt:
```
SLOW MOTION — a rain drop lands on the compass tattoo and splashes
in slow motion. Camera holds steady. Subtle ambient light flickers.
```

Camera: Static, 85mm macro, extreme close-up, no shake.
Duration: 3s (at 0.5x, speed to 1x in edit) | Transition: Cut to Shot 4

**Gate: User approves shot prompts.**

---

## Stage 3 — Production Assembly

### Editing Timeline

| Shot | Type | Duration | Transition | Speed | Audio |
|------|------|----------|-----------|-------|-------|
| 1 | Wide establishing | 5s | Dissolve | 1x | Rain ambience, distant city hum |
| 2 | Medium tracking | 6s | Cut | 1x | Footsteps on wet concrete, rain |
| 5 | Detail insert | 3s | Cut | 0.5x→1x | Rain drop impact SFX, music swell |
| 3 | Close-up profile | 4s | Dissolve | 1x | Music continues, rain fades |
| 4 | Wide departure | 7s | Fade to black | 1x | Music resolves, silence, rain |

**Note:** Shot 5 (compass detail) is inserted between Shots 2 and 3 for emotional pacing — the tattoo symbolizes direction, placed right before the reflective close-up.

**Total runtime:** ~25 seconds (within 30s target)

### Audio Plan

```
Layer 1 — MUSIC
  Track: Minimal piano, sparse and melancholic, minor key
  Entry: Shot 2 (fades in under footsteps)
  Swell: Shot 5 (rain drop moment)
  Resolve: Shot 4 (final note as he walks away)

Layer 2 — AMBIENCE
  Type: Night rain city — wet streets, distant traffic, dripping
  Consistent across: Shots 1-4

Layer 3 — SFX
  Shot 1: Subway steam hiss
  Shot 2: Footsteps on wet pavement (rhythmic)
  Shot 5: Single rain drop impact (amplified)
  Shot 4: Footsteps fading into distance
```

### Production Notes

- **Generation order:** Shot 1 first (establishes lighting), then Shot 2 (introduces character), then Shot 3, 5, 4
- **Consistency:** All shots use the same rain-soaked night palette — cool blue ambient + warm neon accents
- **Slow-motion trick:** Shot 5 generated at 0.5x, speed to 1x in edit for cleaner rain drop animation
- **Character attributes:** Paste Marcus's locked attributes into every prompt — do not paraphrase
