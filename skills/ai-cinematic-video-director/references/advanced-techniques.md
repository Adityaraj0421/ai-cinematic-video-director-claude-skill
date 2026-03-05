# Advanced Techniques for AI Video Generation

## LLM Prompt Expansion

Use an LLM to expand simple animation ideas into detailed directorial prompts.

### Workflow

1. Provide the start frame image
2. Describe the desired animation in plain language
3. Ask the LLM to convert it into a structured six-element prompt

### Example

**Simple input:**
> A man slowly walking through fog while the camera pushes forward.

**Expanded output:**

```
Subject:  Middle-aged man in a dark overcoat, visible breath in cold air
Location: Dense fog-covered forest path, early morning, muted tones
Action:   Walking slowly forward with deliberate steps, arms at sides
Camera:   Slow dolly push forward at chest height, 50mm lens, shallow DOF
Mood:     Eerie, contemplative, muted color palette with cool blue tones
Pacing:   Very slow, dreamlike rhythm, 0.5x real-time feel
```

This expansion adds specificity the AI video model can act on — lens choice, color temperature, movement speed, atmospheric detail.

## Motion Control

For precise, complex character movements, use motion reference workflows.

### Workflow

1. Record yourself (or an actor) performing the movement with a phone camera
2. Upload the recording to a motion control system (e.g., Move AI, Rokoko)
3. Extract the motion data
4. Transfer the motion skeleton to the AI character

### When to Use

- Dance sequences or choreography
- Fight scenes with specific blocking
- Subtle emotional gestures (shaking hands, nervous pacing)
- Any movement that's difficult to describe in text

Motion reference dramatically improves realism for complex physical actions that prompt text alone cannot reliably describe.

## Slow Motion Trick

Fast actions frequently cause morphing artifacts in AI video — limbs stretching, faces distorting, objects phasing through each other.

### Solution

1. Generate the animation in **slow motion** (describe the action as slow or deliberate)
2. Speed the clip up in post-production editing (2x-4x speed)

### Why This Works

AI video models handle slow, predictable motion far better than fast action. By generating slow and accelerating in editing, the model produces cleaner frames that still look natural at full speed.

### Example

```
Animation Prompt (generate slow):
  The skateboarder performs a kickflip in slow motion, board rotating
  cleanly beneath his feet, camera tracking at waist level.

Editing Note:
  Speed up to 2.5x in post. Add speed ramp: slow at apex, fast on landing.
```

## Camera Language Reference

Common camera movements and when to use them:

| Camera Move | Effect | Best For |
|------------|--------|----------|
| **Dolly in** | Builds tension, draws viewer closer | Emotional reveals, dialogue |
| **Dolly out** | Creates distance, reveals context | Establishing scope, isolation |
| **Tracking shot** | Follows action, creates energy | Chase scenes, walking sequences |
| **Handheld** | Raw, documentary feel | Action, urgency, realism |
| **Crane/jib up** | Reveals scale, creates awe | Landscapes, crowd scenes |
| **Static** | Stability, formality | Portraits, dialogue, tension |
| **Whip pan** | Disorientation, surprise | Transitions, reveals |
| **Slow push** | Subtle tension build | Horror, suspense, contemplation |

## Lens Reference

| Lens | Character | Best For |
|------|-----------|----------|
| **16-24mm** | Wide, dramatic distortion | Environments, architecture, epic scale |
| **35mm** | Natural, slight cinematic feel | Walking scenes, medium shots |
| **50mm** | Closest to human eye | Dialogue, portraits, natural feel |
| **85mm** | Compression, shallow DOF | Close-ups, beauty shots, isolation |
| **135mm+** | Heavy compression, dreamy bokeh | Telephoto portraits, surveillance feel |

## Multi-Shot Sequence Planning

When building sequences of multiple AI-generated clips:

1. **Plan all scenes before generating any** — map the full shot list
2. **Lock the character sheet first** — consistency across every clip
3. **Maintain lighting continuity** — same time of day, same color temperature
4. **Vary shot types intentionally** — wide/medium/close, not randomly
5. **Plan transitions in advance** — know where cuts, dissolves, or speed ramps go
6. **Generate B-roll separately** — environment shots, detail inserts, reaction shots

### Shot List Template

```
SEQUENCE: [Name]
CHARACTER REF: [Character sheet reference]
LIGHTING: [Time of day, color temperature, source direction]

Shot 1 — [Wide/Medium/Close] — [Action description] — [Camera move]
Shot 2 — [Wide/Medium/Close] — [Action description] — [Camera move]
Shot 3 — [Wide/Medium/Close] — [Action description] — [Camera move]
...

TRANSITIONS:
  Shot 1 → 2: [Cut/Dissolve/Speed ramp]
  Shot 2 → 3: [Cut/Dissolve/Speed ramp]

AUDIO NOTES:
  [Ambient sound, music cues, SFX]
```
