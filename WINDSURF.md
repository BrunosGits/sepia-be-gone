# Windsurf Skill: sepia-be-gone

## Command
`/sepia-be-gone` in Cascade

## Description
Removes yellow/orange/sepia AI color casts from generated images while preserving layout, text, logos, and products.

## When to Use
- "Remove yellow tint"
- "Fix warm filter"  
- "Make less orange"
- "Neutralize colors"
- "Clean whites"
- "Remove sepia/vintage look"

## Workflow
1. Read `prompts/neutral_color_balance.md` from skill directory
2. Apply prompt to image editing task
3. Preserve: layout, composition, products, logos, labels, prices, addresses, all text
4. Target: 5600K daylight, clean whites, neutral blacks, accurate colors
5. Avoid: yellow tint, orange cast, warm filter, sepia, amber, golden hour, vintage

## Critical Text Warning
For posters/flyers with exact text (prices, addresses):
> "Generative editing may distort text. Generate background only, add text in design tool."

## Negative Prompt (if supported)
```
yellow tint, orange cast, warm filter, sepia, amber lighting, vintage color grading, old painting, golden hour, aged paper, brown overlay, muddy colors, oversaturated orange, excessive warmth, cream whites, brown blacks
```