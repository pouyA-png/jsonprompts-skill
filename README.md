# jsonprompts

A [Claude Code](https://claude.com/claude-code) skill that converts any idea into a clean, copy-paste-ready **JSON MVP prompt** — for AI video generation, image generation, ad creatives, and automation workflows.

**MVP means: minimum structure, maximum effect.** No bloated schemas, no vague adjectives — just production-ready prompts you can paste straight into Veo, Sora, Kling, Runway, Midjourney, or your n8n/agent pipeline.

## What it does

You say:

> json prompt für ein 15 sec video von einem lava nike zeichen wie es gebaut wird

You get:

```json
{
  "prompt": "Ultra-realistic cinematic product reveal of a molten lava emblem forming from cracked black obsidian...",
  "style": "photorealistic cinematic product commercial, dark volcanic luxury aesthetic",
  "camera": { "movement": "slow hover, controlled orbit, dramatic push-in", "lens": "cinematic wide-angle, shallow depth of field", "motion": "slow motion, smooth premium movement" },
  "lighting": { "type": "low-key cinematic", "details": "lava glow as the only light source, orange-red reflections, deep shadows" },
  "environment": { "location": "dark volcanic obsidian surface", "atmosphere": "smoke, ash particles, sparks, glowing magma cracks" },
  "animation": { "sequence": ["darkness", "glowing cracks spread", "lava rises and forms the emblem", "edges harden to volcanic crust", "final hero shot"] },
  "duration": "15 seconds",
  "aspect_ratio": "16:9",
  "quality": "4K, ultra-detailed, photorealistic, cinematic depth of field",
  "negative_prompt": "cartoon, low quality, blurry, text, watermark, distorted shape, people"
}
```

## Supported prompt types

| Type | Schema includes |
|---|---|
| **Video** | prompt, style, camera, lighting, environment, animation sequence, duration, negative_prompt |
| **Image** | prompt, style, composition, lighting, environment, quality, negative_prompt |
| **Automation / n8n / agents** | goal, input_data, process, decision_rules, output_format, constraints, quality_checks |

Every visual prompt ships with a proper `negative_prompt` — always.

## Install

```bash
mkdir -p ~/.claude/skills/jsonprompts
curl -o ~/.claude/skills/jsonprompts/SKILL.md \
  https://raw.githubusercontent.com/pouyA-png/jsonprompts-skill/main/SKILL.md
```

Or clone directly into your skills folder:

```bash
git clone https://github.com/pouyA-png/jsonprompts-skill.git ~/.claude/skills/jsonprompts
```

## Usage

In any Claude Code session:

```
/jsonprompts <your idea>
```

Or just ask naturally — "json prompt for ...", "make this a video prompt", "gib mir einen image prompt" — the skill triggers automatically.

## Core principles

- **Prompt strength formula:** Subject + Action + Style + Camera + Lighting + Details + Sequence + Constraints
- Prompts are written in **English** (models parse it best), explanations stay in your language
- Strong visual language ("controlled orbit", "heat distortion", "final hero shot") — never weak filler ("nice", "cool", "high quality")
- Output is a single valid JSON object in a code block, ready to paste

## License

MIT
