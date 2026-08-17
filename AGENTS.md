# Agent Instructions: sepia-be-gone

## When to Use

Trigger this skill when the user request involves removing warm color casts from images:
- "remove yellow tint" / "yellow filter"
- "too warm" / "make less warm" / "fix warm colors"
- "neutralize colors" / "neutral color balance"
- "clean whites" / "whites are yellow/cream"
- "orange cast" / "too orange"
- "sepia" / "vintage look" / "old photo"
- "AI yellow filter" / "AI warm tint"

## Behavior

1. **Read the prompt template**: `prompts/neutral_color_balance.md`
2. **Apply to the image editing task** with these priorities:
   - Preserve: layout, composition, products, logos, labels, prices, addresses, ALL text
   - Correct: color temperature → 5600K daylight neutral
   - Eliminate: yellow tint, orange cast, sepia, amber, golden hour, vintage grading
3. **Never redesign** — only color correction

## For Posters with Critical Text

Warn the user:
> "Generative image editing can distort text. For exact prices, addresses, product names: generate the background/product visual without text, then add text in Figma/Canva/Photoshop/Illustrator."

## Quick Reference

| User Says | Agent Does |
|-----------|------------|
| "Remove yellow tint" | Apply neutral_color_balance.md prompt |
| "Fix the warm filter" | Same + emphasize 5600K daylight |
| "Poster text must stay exact" | Warn about text distortion, suggest design tool workflow |
| "Make it less orange" | Same + boost negative prompt orange terms |