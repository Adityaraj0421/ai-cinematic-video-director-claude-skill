---
name: ai-film-production
description: This skill should be used when the user asks to "make me a film", "produce an AI video", "create a short film", "build a full video production", "run the film pipeline", "generate a complete video from this concept", or describes a multi-scene AI video project that needs characters, shots, and editing. Orchestrates the full AI film production pipeline from concept to delivery.
---

# AI Film Production Pipeline

## Overview

An orchestrator that runs the complete AI film production pipeline — from concept to delivery-ready prompt packages. Coordinates three sub-skills in sequence, gating each stage on user approval before advancing.

Say "make me a short film about X" and this skill handles the rest.

## The Pipeline

```
CONCEPT → CHARACTERS → SHOTS → PRODUCTION PACKAGE
           Stage 1      Stage 2      Stage 3
```

### Stage 1 — Character Design

**Sub-skill:** `ai-character-sheet-generator`

1. Identify all characters from the concept
2. For each character, generate a locked character sheet:
   - Identity (name, role, age, archetype)
   - Visual attributes (face, hair, build, clothing, distinctive features)
   - Four reference angle prompts (front, side, back, three-quarter)
3. Present all character sheets to the user

**Gate:** User approves all character sheets before proceeding.

### Stage 2 — Shot Craft

**Sub-skill:** `ai-cinematic-video-director`

1. Break the concept into discrete scenes
2. For each scene, apply the five core rules:
   - Start frame first
   - Production quality images
   - Structured six-element prompts (WHO/WHERE/ACTION/CAMERA/MOOD/PACING)
   - Character consistency (reference locked sheets from Stage 1)
   - One action per shot
3. Generate start frame prompt + animation prompt + camera settings for each shot

**Gate:** User reviews shot prompts before proceeding.

### Stage 3 — Production Assembly

**Sub-skill:** `ai-storyboard-to-video`

1. Compile all shots into a numbered shot list
2. Build the editing timeline with transitions, speed, and audio layers
3. Add production notes (generation order, consistency reminders)
4. Deliver the final production package

**Gate:** User receives the complete package.

## Smart Routing

Not every request needs all three stages. Skip stages when the user provides partial inputs:

| User Provides | Skip To |
|--------------|---------|
| Concept only | Stage 1 (full pipeline) |
| Character sheets already done | Stage 2 |
| Character sheets + shot descriptions | Stage 3 |
| Script or storyboard text | Stage 1 for characters, then Stage 3 |

**Detection rules:**
- If the user mentions existing character sheets or provides character descriptions with locked attributes → skip Stage 1
- If the user provides a shot list or detailed scene descriptions with camera directions → skip to Stage 3
- When in doubt, start from Stage 1

## Output Format

The final production package contains all outputs from all three stages:

```
## Production Overview
[Title, genre, target runtime, number of scenes, number of shots]

## Character Sheets
[Per-character: identity, locked attributes, four reference angle prompts]

## Shot List with Prompts
[Per-scene, per-shot: start frame + animation + camera + editing notes]

## Editing Timeline
[Full assembly table: shot number, duration, transition, speed, audio]

## Production Notes
[Generation order, consistency checklist, tool recommendations]
```

## Stage Interaction Rules

1. **Character sheets feed into every shot prompt** — paste locked attributes from Stage 1 into every start frame prompt in Stage 2
2. **Shot craft rules apply to every shot** — the five rules from `ai-cinematic-video-director` are non-negotiable, even under time pressure
3. **The editing timeline references every shot** — no shot exists without a place in the timeline
4. **Consistency compounds** — skipping a stage risks breaking continuity downstream

## Behavior

When this skill is active, operate as an **AI film producer** coordinating the full pipeline:

- Run stages in order, presenting output at each gate
- Reference sub-skills by name when executing each stage
- Never skip a gate — always get user approval before advancing
- If the user wants to revise a stage, go back to that stage without losing downstream work
- Track which characters, scenes, and shots have been completed

## Common Mistakes

| Mistake | Fix |
|---------|-----|
| Jumping straight to shots without character sheets | Always run Stage 1 first unless user provides pre-built sheets |
| Generating all shots before user reviews any | Present shots per-scene, get approval, then continue |
| Forgetting to paste character attributes into shot prompts | Every start frame prompt must include the locked attributes verbatim |
| No editing timeline | Stage 3 always produces the assembly table — clips without a timeline are unusable |
| Skipping a gate because the user seems eager | Gates exist to catch problems early — always pause for approval |

## Additional Resources

For a complete worked example showing the full pipeline from concept to final package, consult **`references/pipeline-example.md`**.
