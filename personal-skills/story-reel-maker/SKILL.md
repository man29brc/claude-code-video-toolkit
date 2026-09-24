---
name: story-reel-maker
description: Create faceless storyline Reels that explain money, insurance, loans or social causes through a short relatable story — for WVS (mutual funds, life insurance), CSC Balaji (home loans, PAN and CSC services) and UCF (NGO). Produces the story script, scene-by-scene visuals (AI image prompts or Canva), voiceover text, on-screen captions and caption/hashtags, and can render the finished video with the claude-code-video-toolkit. Use when the user asks for a story reel, faceless reel, explainer reel, animated reel, or a reel without showing their face.
---

# Story Reel Maker (faceless)

The user prefers **not to be on camera**. Reels are **faceless stories**: a relatable character, a problem, a turning point, and a simple lesson. Trust comes from the **user's own voice** where possible (recorded or cloned), not a face.

## 1. Brief

- **Business:** WVS / CSC Balaji / UCF. Load the profile from memory.
- **Topic / lesson** (e.g. "why a term plan before a car loan", "home loan documents", "SIP vs saving in a bank"). If the user has none, offer 3 ideas.
- **Language:** default Hindi + Gujarati words where natural (audience: Vadodara / Gujarat). Offer Gujarati-only or English.
- **Length:** 30–45s (≈75–110 spoken words).
- **Voice:** the user's own recorded voice (best for trust), a cloned voice, or AI voice.

## 2. Story formula (keep to it)

| Beat | Time | Content |
|---|---|---|
| Hook | 0–3s | A character + a sharp problem. "Rameshbhai earned ₹40,000 a month… and still had ₹0 saved." |
| Problem | 3–12s | What went wrong, shown in 2–3 quick scenes |
| Turning point | 12–25s | The simple idea or lesson (one idea only) |
| Result | 25–35s | Life after, kept realistic. **No promised numbers.** |
| CTA | last 5s | "Comment PLAN / WhatsApp [number] for a free explanation" + the brand |

Characters: local, relatable names and situations (a Vadodara family, a small shop owner, a salaried couple, a first-time home buyer). Keep them respectful and never mock anyone.

## 3. Output

```
**<Business> · <topic> · <length>s · <language>**

| # | Time | Voiceover (spoken) | On-screen text (≤6 words) | Visual (scene description) |
|---|---|---|---|---|

**Image prompts** (one per scene, 9:16, consistent character & style):
1. "<style>, <character description>, <scene>, vertical 9:16, no text"
...
**Caption:** hook line · 2–3 lines · CTA · hashtags (5–8, include local: #vadodara #gujarat)
**Cover text:** ≤4 words
```

Visual style: one consistent style per series (e.g. "flat 2D illustration, warm Indian colour palette"). Keep the same character description in every prompt so the character stays consistent.

## 4. Compliance (mandatory for WVS)

Before finalising **any WVS reel**, run the **finance-compliance-checker** skill: add the disclaimers, no return promises, "Characters are fictional", and flag if insurer approval is needed. For CSC home-loan reels, don't promise approval, rates, or timelines.

## 5. Make the video (choose the route)

- **Canva (in the Claude app):** generate the scenes as a 9:16 video/presentation design with the scene text, then the user adds the voiceover in Canva or CapCut.
- **Any editor (CapCut / InShot):** give the user the images (from the prompts), the voiceover script and the caption timings. They assemble it in about 15 minutes.
- **Full auto render (Claude Code + claude-code-video-toolkit):** use the `concept-explainer-short` template. Write `scenes.json` (per-scene narration + visual), generate the images, voiceover (`gen_vo.py`, which can use the user's cloned voice) and karaoke captions (`gen_captions.py`), then `build.py` renders the finished 9:16 MP4 with music.

Offer to review the finished video with the **reel-reviewer** skill.
