---
name: sepia-be-gone
description: Remove yellow/orange/sepia AI color casts from generated images while preserving layout, text, logos, and products
version: 1.0.0
author: BrunosGits
---

# Skill: sepia-be-gone

## Trigger Conditions

Activate when user says any of:
- "remove yellow tint" / "remove yellow filter"
- "fix warm filter" / "make less warm" / "too warm"
- "neutralize colors" / "neutral color balance"
- "clean whites" / "whites look cream" / "whites are yellow"
- "remove orange cast" / "too orange"
- "remove sepia" / "looks vintage" / "old photo look"
- "fix AI yellow filter" / "AI yellow tint"
- "5600K" / "daylight balanced" / "neutral lighting"

## Core Behavior

When triggered, the agent MUST:

1. **Preserve exactly:**
   - Original layout and composition
   - All products, packaging, logos, labels
   - All visible text: prices, addresses, product names, body copy
   - Overall design structure and spacing

2. **Apply color correction:**
   - Neutral daylight-balanced white balance (5600K)
   - Clean whites (RGB ~255,255,255 — not cream/yellow)
   - Deep neutral blacks (RGB ~0,0,0 — not brown)
   - Accurate product/brand colors
   - Natural contrast, crisp commercial lighting

3. **Explicitly avoid:**
   - Yellow tint, orange cast, warm filter
   - Sepia tone, amber lighting, golden-hour grading
   - Vintage look, old painting effect, aged paper
   - Brown overlay, muddy colors, oversaturated warmth
   - Cream whites, brown blacks

4. **Never:**
   - Redesign the image
   - Change composition
   - Alter text, labels, logos, or product placement intentionally
   - Add new elements not in the original

## Prompt Reference

Use the prompt template in `prompts/neutral_color_balance.md` for image editing tasks.

## Negative Prompt Terms

If the image tool supports negative prompts, include:
```
yellow tint, orange cast, warm filter, sepia, amber lighting, vintage color grading, old painting, golden hour, aged paper, brown overlay, muddy colors, oversaturated orange, excessive warmth, cream whites, brown blacks
```

## Limitations

- **Text distortion**: Generative image editors may alter text. For posters/flyers with critical text (prices, addresses), recommend: generate background only → add text in design tool.
- **Artistic intent**: Do not apply if warm/vintage/sepia IS the desired style.
- **Extreme casts**: Very heavy orange/yellow may require iterative correction.

## Example Invocation

> User: "Can you fix the yellow tint on this poster?"
> Agent: *Applies sepia-be-gone skill, uses neutral_color_balance.md prompt, preserves all text/layout*