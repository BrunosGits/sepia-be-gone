# Claude Code: sepia-be-gone Skill

## Slash Command: `/sepia-be-gone`

### Trigger
User invokes `/sepia-be-gone` or asks to remove yellow/orange/warm/sepia casts from an image.

### Workflow

1. **Load prompt**: Read `prompts/neutral_color_balance.md`
2. **Apply to image edit request** with these constraints:
   - **Preserve**: layout, composition, products, logos, labels, prices, addresses, all visible text
   - **Target**: 5600K daylight-balanced, clean whites, neutral blacks, accurate colors
   - **Eliminate**: yellow tint, orange cast, warm filter, sepia, amber, golden hour, vintage
3. **If text is critical** (posters, flyers, prices, addresses):
   - Warn: "Generative editing may distort text. For exact text preservation: generate background only, add text in design tool."
4. **Do not** redesign, recompose, or alter content — only color grade.

### Example

> User: `/sepia-be-gone this poster has a yellow tint`
> Assistant: *Edits image using neutral_color_balance.md prompt, preserves all text/layout, outputs neutral version*

### Short Add-on for Quick Use

Append to any image prompt:
```
Color grading: neutral daylight-balanced white balance, accurate colors, clean whites, neutral blacks, no yellow tint, no sepia, no orange cast, no warm filter, no vintage grading, no golden-hour lighting.
```