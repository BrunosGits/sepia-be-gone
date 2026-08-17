# VS Code Copilot: sepia-be-gone Skill

## Installation

Add this to `.github/copilot-instructions.md` in your project:

```markdown
## sepia-be-gone Skill

When user asks to remove yellow/orange/warm/sepia tint from images:
- Preserve layout, composition, products, logos, labels, prices, addresses, ALL text
- Apply neutral 5600K daylight-balanced white balance
- Clean whites (not cream/yellow), neutral blacks (not brown)
- Accurate product/brand colors
- Eliminate: yellow tint, orange cast, warm filter, sepia, amber, golden hour, vintage grading
- Never redesign or alter text/content intentionally

Use prompt from: prompts/neutral_color_balance.md

For posters with critical text: warn about generative text distortion, suggest design tool workflow.
```

## Usage in Copilot Chat

> "Use sepia-be-gone skill on this image — remove the yellow tint"

> "Apply neutral color balance, preserve all text and layout"

## Quick Prompt Add-on

Append to any image generation prompt in Copilot:
```
Color grading: neutral daylight-balanced white balance, accurate colors, clean whites, neutral blacks, no yellow tint, no sepia, no orange cast, no warm filter, no vintage grading, no golden-hour lighting.
```