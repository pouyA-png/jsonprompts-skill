---
name: jsonprompts
description: Converts any user prompt/idea into a high-quality, copy-paste-ready JSON MVP prompt. Use whenever the user asks for a JSON prompt, video prompt, image prompt, ad creative prompt, cinematic scene, VFX shot, product reveal, social content prompt, automation/workflow prompt, or says "json prompt" / "mach mir einen json prompt daraus". MVP means minimum structure, maximum effect.
---

# JSONPrompts Skill

## Purpose

Use this skill whenever the user asks for:

* a JSON prompt
* an MVP prompt
* a video prompt
* an image prompt
* a prompt for AI tools
* a cinematic prompt
* a product reveal prompt
* a social media creative prompt
* an automation/workflow prompt
* a structured generation prompt

The goal is to turn any vague user idea into a **clean, powerful, copy-paste-ready JSON MVP prompt**.

MVP means: **minimum structure, maximum effect**.
Do not overcomplicate the JSON. Make it strong, direct, and usable.

---

# Core Output Rule

By default, output only a valid JSON object inside a code block.

Do not explain too much unless the user asks.

The JSON should be:

* clean
* readable
* structured
* specific
* production-ready
* easy to paste into video/image/AI tools

---

# Internal Thinking Process

Before writing the JSON, internally identify:

1. **Main intent**
   What does the user want to create?

2. **Medium**
   Is it video, image, ad, automation, website, SaaS, script, voiceover, product shot, or social content?

3. **Subject**
   What is the central object, person, brand, scene, product, or action?

4. **Mood / energy**
   Examples: brutal, premium, cinematic, clean, luxury, aggressive, emotional, dark, futuristic, realistic.

5. **Visual style**
   Examples: photorealistic, cinematic, 4K, macro, product-commercial, drone shot, handheld, luxury real estate, VFX trailer.

6. **Camera / motion**
   For video prompts, always define movement clearly.

7. **Lighting**
   Lighting is critical. Always describe it.

8. **Scene sequence**
   For video, define what happens from start to finish.

9. **Constraints**
   Include what must not appear.

10. **Output quality**
    Define resolution, realism, aspect ratio, sharpness, detail level.

---

# Default JSON Structure for Video Prompts

Use this structure for most video-generation requests:

```json
{
  "prompt": "",
  "style": "",
  "camera": {
    "movement": "",
    "lens": "",
    "motion": ""
  },
  "lighting": {
    "type": "",
    "details": ""
  },
  "environment": {
    "location": "",
    "atmosphere": ""
  },
  "animation": {
    "sequence": []
  },
  "duration": "",
  "aspect_ratio": "",
  "quality": "",
  "negative_prompt": ""
}
```

---

# Video Prompt Rules

For video prompts, always make the prompt cinematic and action-based.

A strong video prompt should include:

* starting frame
* main transformation or action
* camera movement
* lighting behavior
* atmosphere
* texture details
* final hero shot
* what should not appear

Use strong visual language:

* slow cinematic hover
* dramatic push-in
* macro close-up
* controlled orbit
* heat distortion
* particles
* realistic shadows
* premium commercial reveal
* high tension
* realistic physics
* sharp surface detail
* final hero shot

Avoid weak language:

* nice
* cool
* beautiful
* make it good
* high quality only
* interesting
* creative

Replace weak words with specific visual direction.

---

# Default JSON Structure for Image Prompts

Use this structure for image-generation requests:

```json
{
  "prompt": "",
  "style": "",
  "composition": {
    "framing": "",
    "angle": "",
    "focus": ""
  },
  "lighting": {
    "type": "",
    "details": ""
  },
  "environment": {
    "location": "",
    "details": ""
  },
  "quality": "",
  "aspect_ratio": "",
  "negative_prompt": ""
}
```

---

# Image Prompt Rules

For image prompts, always define:

* subject
* composition
* angle
* materials
* lighting
* background
* realism level
* camera quality
* what to avoid

For realistic outputs, use:

* photorealistic
* natural lighting
* realistic shadows
* high dynamic range
* sharp details
* professional photography
* no distortion
* no text
* no watermark

---

# Default JSON Structure for Automation / Workflow Prompts

Use this structure when the user wants an AI automation, n8n workflow logic, SaaS flow, API process, or agent instruction:

```json
{
  "goal": "",
  "input_data": [],
  "process": [],
  "decision_rules": [],
  "output_format": {},
  "constraints": [],
  "quality_checks": [],
  "negative_instructions": []
}
```

---

# Automation Prompt Rules

For automation prompts, focus on:

* exact input fields
* logic steps
* conditions
* fallback handling
* output schema
* error prevention
* clean variable names

Do not write vague automation prompts.
Make the logic executable and unambiguous.

---

# Prompt Strength Formula

Every great JSON MVP prompt should follow this formula:

**Subject + Action + Style + Camera + Lighting + Details + Sequence + Constraints**

Example logic:

* Subject: molten lava sports emblem
* Action: forms from volcanic cracks
* Style: ultra-realistic cinematic commercial
* Camera: slow hover, macro close-up, orbit
* Lighting: lava glow, dark shadows
* Details: smoke, sparks, heat distortion
* Sequence: darkness → cracks → lava → formation → hero shot
* Constraints: no text, no people, no watermark

---

# Negative Prompt Rules

Always include a `negative_prompt` for visual generation.

Use it to block:

* low quality
* blurry output
* cartoon look
* fake textures
* distorted shapes
* bad anatomy if people are involved
* text
* captions
* labels
* watermark
* logos if not requested
* extra objects
* overexposed lighting
* unrealistic reflections
* messy composition

For real estate prompts, also block:

* fake furniture
* changed architecture
* distorted walls
* wrong windows
* wrong doors
* collage
* white borders
* labels
* people
* animals

---

# Brand / Logo Handling

If the user asks for a real brand logo or known IP, create the prompt if it is just for generation/testing.

If the user mentions commercial usage, add a short legal note after the JSON:

"For commercial use, use a custom brand-safe emblem instead of the protected logo."

Do not interrupt the output unless needed.

---

# Style Rules

Write prompts in English by default because most image/video models respond better to English.

Keep user-facing explanations in the user's language.

For German users, briefly say:

"Hier ist der copy-paste JSON MVP Prompt:"

Then provide the JSON.

---

# Quality Standards

The JSON must feel like it was written by a professional creative director.

Every output should be:

* specific
* visual
* direct
* cinematic
* technically useful
* cleanly structured
* not bloated

Never produce lazy prompts.

Bad:

```json
{
  "prompt": "make a cool lava logo video"
}
```

Good:

```json
{
  "prompt": "Ultra-realistic cinematic product reveal of a molten lava sports emblem forming from cracked black obsidian. The scene begins in darkness as glowing magma veins spread through the surface. Lava rises, flows, and hardens into a sharp emblem shape while sparks, smoke, ash, and heat distortion fill the air. The camera slowly hovers around the emblem with macro close-ups of bubbling lava and glowing edges. Final hero shot: the finished molten emblem floating above fractured volcanic rock, glowing from within.",
  "style": "photorealistic cinematic product commercial, dark volcanic luxury aesthetic, intense high-tension reveal",
  "camera": {
    "movement": "slow hover, controlled orbit, dramatic push-in, macro close-ups",
    "lens": "cinematic wide-angle lens with shallow depth of field",
    "motion": "slow motion, smooth premium commercial movement"
  },
  "lighting": {
    "type": "low-key cinematic lighting",
    "details": "lava glow as the main light source, orange-red reflections, deep shadows, smoky atmosphere, realistic heat shimmer"
  },
  "environment": {
    "location": "dark volcanic obsidian surface",
    "atmosphere": "smoke, ash particles, sparks, glowing magma cracks, heavy cinematic tension"
  },
  "animation": {
    "sequence": [
      "black screen with faint rumbling tension",
      "small glowing cracks spread across obsidian rock",
      "molten lava rises through the fractures",
      "lava streams connect and shape into the emblem",
      "edges harden into dark volcanic crust while the inner core stays glowing",
      "camera orbits slowly around the final emblem",
      "final hero shot with sparks, smoke, and intense lava glow"
    ]
  },
  "duration": "8-12 seconds",
  "aspect_ratio": "16:9",
  "quality": "4K, ultra-detailed, photorealistic, realistic lava simulation, cinematic depth of field",
  "negative_prompt": "cartoon, anime, low quality, blurry, fake lava, plastic texture, flat lighting, text, captions, labels, people, watermark, distorted shape, messy composition, overexposed glow"
}
```

---

# Response Patterns

## If user asks for a video prompt

Output:

```json
{
  "prompt": "...",
  "style": "...",
  "camera": {
    "movement": "...",
    "lens": "...",
    "motion": "..."
  },
  "lighting": {
    "type": "...",
    "details": "..."
  },
  "environment": {
    "location": "...",
    "atmosphere": "..."
  },
  "animation": {
    "sequence": []
  },
  "duration": "...",
  "aspect_ratio": "...",
  "quality": "...",
  "negative_prompt": "..."
}
```

## If user asks for an image prompt

Output:

```json
{
  "prompt": "...",
  "style": "...",
  "composition": {
    "framing": "...",
    "angle": "...",
    "focus": "..."
  },
  "lighting": {
    "type": "...",
    "details": "..."
  },
  "environment": {
    "location": "...",
    "details": "..."
  },
  "quality": "...",
  "aspect_ratio": "...",
  "negative_prompt": "..."
}
```

## If user asks for n8n / automation / SaaS prompt

Output:

```json
{
  "goal": "...",
  "input_data": [],
  "process": [],
  "decision_rules": [],
  "output_format": {},
  "constraints": [],
  "quality_checks": [],
  "negative_instructions": []
}
```

---

# Final Rule

Always make the JSON usable immediately.

No vague text.
No weak descriptions.
No unnecessary explanation.
No bloated schema.
No missing negative prompt for visual generation.

The result should feel like a clean MVP prompt from a top-tier AI creative operator.
