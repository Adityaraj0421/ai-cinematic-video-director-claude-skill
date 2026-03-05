---
name: ai-storyboard-to-video
description: This skill should be used when the user asks to "convert a storyboard to video prompts", "turn a script into AI video", "plan a video sequence", "create a shot list", "build an AI film timeline", "break down a scene for video generation", or mentions storyboard conversion, shot-by-shot planning, or multi-scene AI video production workflows.
---

# AI Storyboard to Video

## Overview

A structured pipeline for converting written storyboards, scripts, or scene descriptions into complete AI video production packages. Each scene becomes a self-contained prompt set — start frame, animation, camera, and editing instructions — ready for any AI video generation tool.

This skill bridges the gap between narrative writing and technical video generation prompts.

## When to Use

- Converting a written script or storyboard into AI video prompts
- Planning a multi-scene AI video sequence from a narrative outline
- Building a complete shot list with camera and editing instructions
- Producing an AI short film, ad, or social media video from a concept

## The Pipeline

```
STORYBOARD → SCENE BREAKDOWN → SHOT LIST → PROMPT PACKAGE → EDITING TIMELINE
```

### Stage 1 — Scene Breakdown

Parse the storyboard into discrete scenes. Each scene is one continuous location and time block.

**Scene boundary triggers:**
- Location change
- Time jump (hours, days, flashback)
- Major mood shift
- Character entrance/exit that resets the visual

```
SCENE [N]
  Location:   [Where]
  Time:       [When — time of day, weather, season]
  Characters: [Who is present — reference character sheets]
  Emotion:    [Core emotional tone]
  Duration:   [Target clip length in seconds]
  Summary:    [One-sentence description of what happens]
```

### Stage 2 — Shot List

Break each scene into individual shots. Follow the **one action per shot** rule.

Each shot defines:

| Element | Description |
|---------|-------------|
| **Shot #** | Sequential number within the scene |
| **Type** | Wide / Medium / Close-up / Extreme close-up / Over-the-shoulder |
| **Subject** | Who or what is in frame |
| **Action** | Single specific action |
| **Camera** | Movement type, lens, angle |
| **Duration** | Target seconds for this clip |

**Shot type progression** — follow cinematic convention:
1. **Establishing wide** — orient the viewer in the space
2. **Medium action** — show the primary event
3. **Close-up reaction** — emotional beats and details
4. **Cutaway/insert** — environmental detail or object

### Stage 3 — Prompt Package

For each shot, generate the complete prompt set:

```
## Shot [N] — [Brief Label]

### Start Frame Prompt
[Full image generation prompt with lighting, lens, composition, character attributes]

### Animation Prompt
[Specific action and camera movement description]

### Camera Settings
[Movement type, lens, angle, shake level, speed]

### Duration
[Target seconds]

### Editing Notes
[Speed ramps, transition to next shot, audio cues]
```

### Stage 4 — Editing Timeline

After all shots are generated, produce the assembly timeline:

```
## Editing Timeline

| Shot | Duration | Transition | Speed | Audio |
|------|----------|-----------|-------|-------|
| 1    | 3s       | Cut       | 1x    | Ambient city |
| 2    | 4s       | Cut       | 1x    | Footsteps |
| 3    | 2s       | Speed ramp| 0.5x→1x | Music swell |
| ...  | ...      | ...       | ...   | ... |

Total runtime: [sum]s
```

## Output Format

When converting a storyboard, always return the complete package:

```
## Production Overview
[Title, genre, target runtime, character sheets referenced]

## Scene Breakdown
[All scenes with location, time, characters, emotion, duration]

## Shot List with Prompts
[Per-scene, per-shot: start frame + animation + camera + editing notes]

## Editing Timeline
[Full assembly table with transitions, speed, and audio]

## Production Notes
[Technical recommendations, generation order, consistency reminders]
```

## Consistency Enforcement

1. **Reference character sheets in every prompt** — paste locked attributes from `ai-character-sheet-generator`
2. **Lock lighting per scene** — all shots within a scene share time-of-day, color temperature, and light direction
3. **Lock wardrobe per scene** — unless a costume change is scripted, clothing stays identical
4. **Match eyelines across shots** — if character A looks right in shot 2, character B looks left in shot 3
5. **Maintain spatial continuity** — if a door is on the left in the wide shot, it stays on the left in close-ups

## Scene Duration Guidelines

| Content | Recommended Duration |
|---------|---------------------|
| Establishing wide shot | 2-4 seconds |
| Action shot | 3-5 seconds |
| Dialogue reaction | 2-3 seconds |
| Slow-motion detail | 2-3 seconds (at 0.5x) |
| Transition/cutaway | 1-2 seconds |

Keep individual clips short. AI video tools produce cleaner results in 3-5 second clips than in 10+ second clips.

## Common Mistakes

| Mistake | Fix |
|---------|-----|
| No establishing shot | Always open a new scene with a wide shot |
| Overloading a single shot with multiple actions | One action per shot — edit together in post |
| Inconsistent lighting across shots in same scene | Lock time-of-day and light direction per scene |
| Missing character sheet references in prompts | Paste locked attributes into every start frame prompt |
| No editing timeline | Always produce the assembly table — generation without editing plan wastes effort |
| Clips too long (8-10+ seconds) | Target 3-5 seconds per clip for best quality |

## Integration with Other Skills

This skill works as the final stage in a three-skill pipeline:

```
ai-character-sheet-generator  →  ai-cinematic-video-director  →  ai-storyboard-to-video
       (characters)                    (shot craft)                  (full production)
```

1. Build character sheets first with **ai-character-sheet-generator**
2. Apply directorial rules from **ai-cinematic-video-director** to each shot
3. Use this skill to assemble everything into a production-ready package

## Additional Resources

For genre-specific templates, multi-character scene blocking, and parallel action editing, consult **`references/production-templates.md`**.
