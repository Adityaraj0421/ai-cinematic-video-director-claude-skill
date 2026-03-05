# Production Templates

## Genre-Specific Templates

### Action Sequence

```
SEQUENCE: [Action Scene Name]
PACING: Fast cuts, 2-3 seconds per shot
CAMERA STYLE: Handheld, dynamic angles, 24-35mm lenses

Shot 1 — WIDE — Establishing the arena
  Start Frame: Wide shot of [location], [lighting], [atmosphere]
  Animation: Camera slowly pushes forward into the space
  Duration: 3s | Transition: Hard cut

Shot 2 — MEDIUM — The trigger
  Start Frame: Medium shot of [character], tense posture, [location context]
  Animation: Character turns sharply / draws weapon / begins sprint
  Duration: 2s | Transition: Hard cut

Shot 3 — CLOSE-UP — The impact
  Start Frame: Close-up of [action detail — fist, weapon, face]
  Animation: SLOW MOTION — action completes in 0.5x speed
  Duration: 3s | Transition: Speed ramp to 2x

Shot 4 — WIDE — The aftermath
  Start Frame: Wide shot showing result of action, dust settling
  Animation: Camera slowly pulls back, ambient motion
  Duration: 4s | Transition: Dissolve
```

### Dialogue Scene

```
SEQUENCE: [Conversation Scene Name]
PACING: Slower cuts, 3-5 seconds per shot
CAMERA STYLE: Static or slow dolly, 50-85mm lenses, shallow DOF

Shot 1 — WIDE — Two-shot establishing
  Start Frame: Wide shot showing both characters, [location], [lighting]
  Animation: Minimal — ambient background motion, characters breathing
  Duration: 4s | Transition: Cut

Shot 2 — MEDIUM CLOSE-UP — Speaker A
  Start Frame: MCU of [Character A], [expression], [85mm, shallow DOF]
  Animation: Subtle head movement, lips parting as if speaking
  Duration: 3s | Transition: Cut

Shot 3 — OVER-THE-SHOULDER — Speaker B reacts
  Start Frame: OTS from behind Character A, Character B in focus
  Animation: Character B reacts — nod, eye shift, expression change
  Duration: 3s | Transition: Cut

Shot 4 — CLOSE-UP — Emotional beat
  Start Frame: Tight close-up on [character]'s eyes/face, [emotion]
  Animation: Slow push-in, 85mm, very subtle — 2px of movement
  Duration: 3s | Transition: Dissolve
```

### Montage / Time Passage

```
SEQUENCE: [Montage Name]
PACING: Medium cuts, 2-4 seconds, rhythm-driven
CAMERA STYLE: Mixed — variety of angles and lenses

Shot 1 — DETAIL — [Activity close-up]
  Duration: 2s | Transition: Dissolve

Shot 2 — MEDIUM — [Character doing activity, different time]
  Duration: 3s | Transition: Dissolve

Shot 3 — WIDE — [New location or time of day]
  Duration: 3s | Transition: Dissolve

Shot 4 — CLOSE-UP — [Progress indicator — clock, calendar, changing light]
  Duration: 2s | Transition: Cut to next scene

AUDIO: Music-driven pacing — cuts align with beat
```

### Establishing / Mood Sequence

```
SEQUENCE: [Location/Mood Reveal]
PACING: Slow, atmospheric, 4-6 seconds per shot
CAMERA STYLE: Smooth dolly/crane, 24-50mm, deep focus

Shot 1 — EXTREME WIDE — Landscape/cityscape
  Animation: Slow crane up or drone push forward
  Duration: 5s | Transition: Dissolve

Shot 2 — WIDE — Closer environmental detail
  Animation: Slow lateral tracking shot
  Duration: 4s | Transition: Dissolve

Shot 3 — MEDIUM — Human presence in environment
  Animation: Static or very slow push-in
  Duration: 4s | Transition: Cut to action
```

## Multi-Character Scene Blocking

When multiple characters share a scene, plan spatial relationships before generating:

### Blocking Map

```
SCENE BLOCKING — [Scene Name]

Camera Position: [Front/side/overhead diagram description]

    [Char A]          [Char B]
    facing right      facing left
    seated            standing
    frame left        frame right

Background Elements:
  Left:   [Window / door / wall detail]
  Center: [Table / space between characters]
  Right:  [Bookshelf / props / environment]
```

### Multi-Character Rules

1. **Lock spatial positions** — if Character A is on the left in wide shot, they stay on the left in all shots of this scene
2. **Maintain eyeline direction** — character looking right in their close-up must match the spatial layout
3. **Generate wide shot first** — establish the spatial relationship, then generate individual shots matching it
4. **180-degree rule** — camera stays on one side of the action line between characters

## Parallel Action Editing

When cutting between simultaneous events in different locations:

### Cross-Cut Structure

```
PARALLEL SEQUENCE: [Name]

THREAD A — [Location A]          THREAD B — [Location B]
Shot A1 — Wide establishing
                                  Shot B1 — Wide establishing
Shot A2 — Medium action
                                  Shot B2 — Medium action
Shot A3 — Close-up tension
                                  Shot B3 — Close-up tension
Shot A4 — Climax                  Shot B4 — Climax (simultaneous)

INTERCUT PATTERN: A1, B1, A2, B2, A3, B3, A4+B4
PACING: Accelerating — cuts get shorter toward climax
```

### Cross-Cut Rules

1. **Establish both locations independently** before intercutting
2. **Increase cutting frequency** as tension builds
3. **Match energy levels** — if Thread A intensifies, Thread B should too
4. **Use visual contrast** — different color temperatures or lighting between locations helps the viewer track which thread is active

## Audio Planning

AI video is silent — plan audio in the editing timeline:

### Audio Layer Template

```
AUDIO PLAN — [Sequence Name]

Layer 1 — MUSIC
  Track: [Genre/mood description]
  Entry: Shot [N]
  Exit: Shot [N]
  Notes: [Swell at shot X, drop at shot Y]

Layer 2 — AMBIENCE
  Type: [City / nature / interior / crowd]
  Consistent across: Shots [N-N]

Layer 3 — SFX
  Shot [N]: [Sound effect — footsteps, door, impact]
  Shot [N]: [Sound effect]

Layer 4 — DIALOGUE (if applicable)
  Shot [N]: [Character line — to be recorded or generated separately]
```

## Continuity Checklist

Before finalizing any production package, verify:

- [ ] All character sheets referenced in every start frame prompt
- [ ] Lighting consistent within each scene (time of day, color temperature)
- [ ] Wardrobe consistent within each scene (unless scripted change)
- [ ] Spatial positions maintained across shot types
- [ ] Eyeline directions match blocking map
- [ ] Camera stays on correct side of 180-degree line
- [ ] Editing timeline accounts for every generated shot
- [ ] Audio layers planned for final assembly
- [ ] Total runtime calculated and within target
