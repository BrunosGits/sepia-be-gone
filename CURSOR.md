---
description: Remove yellow/orange/sepia AI color casts from generated images
globs: ["**/*"]
alwaysApply: false
---

# Cursor Rule: @sepia-be-gone

## Usage

Type `@sepia-be-gone` in Cursor Chat when you want to remove warm color casts from an image.

## Behavior

When invoked, the agent will:

1. **Preserve**: layout, composition, products, logos, labels, prices, addresses, all text
2. **Apply**: neutral 5600K daylight balance, clean whites, neutral blacks, accurate colors
3. **Remove**: yellow tint, orange cast, warm filter, sepia, amber, golden hour, vintage grading
4. **Never**: redesign, change composition, alter text/labels intentionally

## Prompt Template

Use the prompt from `prompts/neutral_color_balance.md` (in this skill directory).

## For Posters with Exact Text

> "Generative editing may distort text. For exact prices/addresses: generate background only, add text in Figma/Canva."

## Quick Add-on

Append to any image generation prompt:
```
Color grading: neutral daylight-balanced white balance, accurate colors, clean whites, neutral blacks, no yellow tint, no sepia, no orange cast, no warm filter, no vintage grading, no golden-hour lighting.
```