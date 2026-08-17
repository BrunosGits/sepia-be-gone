# Before → After Examples

> **Add your 3 image pairs here.** Replace placeholder paths with actual images.

---

## Example 1: Supermarket Promo Poster

**Problem**: Yellow/orange cast on promotional poster — cream whites, amber shadows, inaccurate brand blues

| Before (Yellow Tint) | After (Neutral) |
|:---:|:---:|
| ![Before](examples/images/before/poster-yellow.jpg) | ![After](examples/images/after/poster-neutral.jpg) |

**Preserved**: Price ($3.99), address (123 Main St), product placement, logo, layout  
**Fixed**: 5600K daylight balance, clean whites, neutral grays, accurate brand blues  
**Prompt used**: Full prompt from `prompts/neutral_color_balance.md`

---

## Example 2: Food Photography

**Problem**: Golden "appetizing" overlay — brownish greens, yellow whites, artificial warmth

| Before (Warm Filter) | After (Color-Accurate) |
|:---:|:---:|
| ![Before](examples/images/before/food-warm.jpg) | ![After](examples/images/after/food-neutral.jpg) |

**Preserved**: Food appeal, composition, plating  
**Fixed**: Fresh greens, clean whites, natural meat tones, no golden overlay  
**Prompt used**: Food variant from `prompts/neutral_color_balance.md`

---

## Example 3: Cinematic / Fantasy Art

**Problem**: Heavy orange/teal grading — orange skin tones, teal shadows, sepia haze

| Before (Orange/Teal) | After (Neutral Fantasy) |
|:---:|:---:|
| ![Before](examples/images/before/cinematic-orange.jpg) | ![After](examples/images/after/cinematic-neutral.jpg) |

**Preserved**: Composition, characters, mood, detail  
**Fixed**: Natural skin, neutral shadows, readable text, no orange cast  
**Prompt used**: Cinematic variant from `prompts/neutral_color_balance.md`

---

## How to Add Your Images

1. Create directories:
   ```bash
   mkdir -p examples/images/before examples/images/after
   ```

2. Add your 3 before/after pairs:
   ```
   examples/images/before/poster-yellow.jpg
   examples/images/after/poster-neutral.jpg
   examples/images/before/food-warm.jpg
   examples/images/after/food-neutral.jpg
   examples/images/before/cinematic-orange.jpg
   examples/images/after/cinematic-neutral.jpg
   ```

3. The markdown above will render automatically on GitHub.