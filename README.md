# AI Film Production Pipeline — Claude Skills

A complete AI filmmaking skill suite for [Claude Code](https://claude.com/claude-code). Four interconnected skills that turn Claude into an AI film director, generating structured prompts for AI video tools like Runway, Kling, Sora, and Pika.

Built on real filmmaking principles — not prompt tricks.

## The Pipeline

```
CONCEPT → CHARACTERS → SHOTS → PRODUCTION PACKAGE
            Skill 1     Skill 2       Skill 3
                    ↑ Orchestrated by Skill 4 ↑
```

| Skill | Purpose | Words |
|-------|---------|:-----:|
| **ai-character-sheet-generator** | Locked visual attributes + 4-angle reference prompts | 848 + 598 ref |
| **ai-cinematic-video-director** | 5 core rules + 6-element structured prompts | 919 + 729 ref |
| **ai-storyboard-to-video** | Script-to-shot-list pipeline + editing timeline | 959 + 960 ref |
| **ai-film-production** | Orchestrator — runs all 3 stages with approval gates | 794 + 1,222 ref |

## Installation

Clone into your Claude Code skills directory:

```bash
git clone https://github.com/Adityaraj0421/ai-cinematic-video-director-claude-skill.git ~/.claude/skills/ai-film-skills
```

Or copy individual skill folders into `~/.claude/skills/`.

All skills auto-register on next Claude Code session — no configuration needed.

## Quick Start

### Full Pipeline (Orchestrator)

Say:
> "Make me a short film about an astronaut discovering a flower on Mars"

The `ai-film-production` orchestrator triggers and runs all three stages:

1. **Stage 1** — Generates character sheets with locked attributes and 4 reference angles
2. **Stage 2** — Applies the 5 filmmaking rules and creates structured shot prompts
3. **Stage 3** — Assembles editing timeline, audio plan, and production notes

Each stage gates on your approval before advancing.

### Individual Skills

Each skill also works independently:

| You say | Skill triggered |
|---------|----------------|
| "Create a character sheet for my protagonist" | `ai-character-sheet-generator` |
| "Generate an AI video prompt for a chase scene" | `ai-cinematic-video-director` |
| "Convert this script into a shot list" | `ai-storyboard-to-video` |

## The 5 Core Filmmaking Rules

These rules are enforced across all skills:

1. **Start Frame First** — Generate an image before animating. Text-to-video without a start frame removes control.
2. **Production Quality Images** — Specify lighting, lens, texture, composition. Bad images make bad video.
3. **Structured Prompts** — Every prompt defines WHO, WHERE, ACTION, CAMERA, MOOD, PACING.
4. **Character Consistency** — Lock every visual attribute in a character sheet. Paste attributes verbatim across all shots.
5. **One Action Per Scene** — Keep each clip focused. Build complexity through editing, not overloaded prompts.

## Skill Architecture

```
ai-character-sheet-generator/
├── SKILL.md                              Identity, attributes, 4-angle prompts
└── references/
    └── advanced-character-design.md      Expressions, wardrobe variants, ensembles

ai-cinematic-video-director/
├── SKILL.md                              5 rules, 6-element prompt structure
└── references/
    └── advanced-techniques.md            LLM expansion, motion control, lens tables

ai-storyboard-to-video/
├── SKILL.md                              4-stage pipeline, shot lists, timeline
└── references/
    └── production-templates.md           Genre templates, blocking, audio planning

ai-film-production/
├── SKILL.md                              Orchestrator — pipeline, routing, gates
└── references/
    └── pipeline-example.md              Full worked example: "The Last Commute"
```

### Progressive Disclosure

Each SKILL.md is kept lean (under 1,000 words) for fast context loading. Detailed content lives in `references/` and loads only when Claude needs it. This prevents burning context tokens on information that isn't relevant yet.

## Output Format

Every production package includes:

```
Character Sheets     — Locked attributes + 4 reference angle prompts per character
Shot Prompts         — Start frame + animation prompt + camera settings per shot
Editing Timeline     — Shot order, duration, transitions, speed
Audio Plan           — Music, ambience, SFX layers with entry/exit points
Production Notes     — Generation order, consistency checklist, tool recommendations
```

## Recommended Tools

| Stage | Tools |
|-------|-------|
| Start frame generation | Midjourney, FLUX Pro, Stable Diffusion XL |
| Video animation | Runway Gen-3, Kling 1.5, Minimax, Sora |
| Editing & assembly | DaVinci Resolve, Premiere Pro, CapCut |
| Audio | Suno, ElevenLabs, Freesound |

## License

MIT
