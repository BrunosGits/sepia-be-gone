# sepia-be-gone

> A portable prompt skill to generate AI images without the yellow/orange/sepia filter. Works with opencode, Claude Code, Codex, Cursor, Windsurf, VS Code Copilot, and any image generator.

---

## The Problem: Why AI Images Look Yellow

AI image models don't just "learn from old paintings." The yellow/orange cast comes from **token bias** in training data:

| Prompt Keyword | Statistical Association | Result |
|----------------|------------------------|--------|
| `cinematic` | Orange/teal grading (Hollywood LUTs) | Heavy amber cast |
| `golden hour` | Warm sunset lighting | Extreme yellow/orange |
| `premium`, `luxury` | Warm "golden" commercial photography | Cream whites, brown blacks |
| `appetizing` (food) | Golden food photography overlays | Greens→brown, whites→cream |
| `studio lighting` | Often tungsten (3200K) not daylight | Warm color temperature |
| `dramatic lighting` | Chiaroscuro with warm key lights | Orange shadows |

**RLHF amplifies this**: Human raters consistently prefer warmer images for "appeal," so models learn warmth = quality.

---

## What This Skill Does

**Preserves:** Layout, composition, products, logos, labels, prices, addresses, all visible text  
**Applies:** Neutral 5600K daylight balance, clean whites, neutral blacks, accurate colors  
**Removes:** Yellow tint, orange cast, warm filter, sepia, amber, golden hour, vintage grading

---

## Quickstart

### opencode
```bash
git clone https://github.com/BrunosGits/sepia-be-gone.git ~/.config/opencode/skill/sepia-be-gone
# Use: /sepia-be-gone
```

### Claude Code
```bash
git clone https://github.com/BrunosGits/sepia-be-gone.git ~/.claude/skills/sepia-be-gone
# Use: /sepia-be-gone
```

### Codex / Generic Agents
```bash
git clone https://github.com/BrunosGits/sepia-be-gone.git .github/skills/sepia-be-gone
# Use: /sepia-be-gone
```

### Cursor
Copy `CURSOR.md` to `~/.cursor/rules/sepia-be-gone.mdc` or project `.cursor/rules/`  
Use: `@sepia-be-gone` in chat

### Windsurf
Copy `WINDSURF.md` to `~/.codeium/windsurf/skills/sepia-be-gone/`  
Use: `/sepia-be-gone` in Cascade

### VS Code Copilot
Add `VSCODE.md` content to `.github/copilot-instructions.md` or settings  
Use: "Use sepia-be-gone skill" in chat

### Any Image Generator (DALL-E, Midjourney, GPT-4o, Gemini, Firefly, etc.)
```bash
cat prompts/neutral_color_balance.md | pbcopy
# Paste at end of your prompt
```

---

## The Prompt (Copy-Paste Ready)

**Full prompt** → `prompts/neutral_color_balance.md`

**Short add-on** (append to any prompt):
```
Color grading: neutral daylight-balanced white balance, accurate colors, clean whites, neutral blacks, no yellow tint, no sepia, no orange cast, no warm filter, no vintage grading, no golden-hour lighting.
```

**Negative prompt** (if supported):
```
yellow tint, orange cast, warm filter, sepia, amber lighting, vintage color grading, old painting, golden hour, aged paper, brown overlay, muddy colors, oversaturated orange, excessive warmth, cream whites, brown blacks
```

---

## Before → After Examples

See [`EXAMPLES.md`](EXAMPLES.md) for 3 case studies:
1. **Supermarket promo poster** — cream whites → pure whites, amber shadows → neutral
2. **Food photography** — golden overlay → color-accurate greens/meats
3. **Cinematic/fantasy** — orange/teal grading → neutral daylight

---

## When to Use

- "Remove the yellow tint"
- "Make this less warm"  
- "Fix the AI yellow filter"
- "Whites look cream/yellow"
- "Food looks orange"
- "Poster looks vintage but shouldn't"

---

## Limitations

| Limitation | Workaround |
|------------|------------|
| Generative editors distort text | For posters with exact prices/addresses: generate background only, add text in Figma/Canva |
| Deliberate warm/vintage style | Don't use — this skill forces neutral |
| Extreme orange casts (sunset) | May need 2-pass editing |
| Local color casts only | Use generative inpainting for specific regions |

---

## Repository Structure

```
sepia-be-gone/
├── README.md                          # This file
├── SKILL.md                           # opencode skill (primary)
├── AGENTS.md                          # Codex/opencode adapter
├── CLAUDE.md                          # Claude Code adapter
├── CURSOR.md                          # Cursor IDE rule
├── WINDSURF.md                        # Windsurf Cascade skill
├── VSCODE.md                          # VS Code Copilot instructions
├── LICENSE                            # MIT
├── prompts/
│   └── neutral_color_balance.md       # The reusable prompt
└── EXAMPLES.md                        # Before/after gallery
```

---

## License

MIT — see [`LICENSE`](LICENSE)