---
name: instagram-carousel
description: Write and design Instagram carousel posts (swipeable multi-slide posts) for the user's businesses (WVS, CSC Balaji, UCF NGO) — slide copy, caption, and a finished design in Canva when connected. Use when the user asks for a carousel, slides for Instagram, swipe post, infographic post, tips post, or checklist post.
---

# Instagram Carousel

Carousels get saved and shared, and are great for tips, checklists, step-by-steps, myths vs facts, and impact stories.

## 1. Brief

- **Which business?** WVS, CSC Balaji, or UCF. Load the profile (tone, language, CTA, brand colours/logo if known) from memory or preferences.
- **Topic and goal.** If the user has only a vague topic, propose 3 angles and let them pick:
  - Checklist ("5 documents you need for ___")
  - Mistakes ("4 mistakes people make with ___")
  - Step-by-step ("How to ___ in 4 steps")
  - Myth vs fact
  - Story (before → turning point → after), best for UCF impact
- **Slides:** default 7 (range 5–10). **Size:** 1080×1350 portrait (4:5), unless the user says square.

## 2. Write the slides

```
**Slide 1 (cover):** Hook ≤8 words + small subtitle. Must make people swipe.
**Slides 2–N-1:** One idea per slide. Headline ≤6 words + body ≤20 words.
**Last slide:** CTA (save / share / call / WhatsApp / donate) + handle or contact.
```

Then the **caption** (hook, 2–4 lines of value, CTA, "Save this for later"), **5–8 hashtags**, and **alt text** (one line).

Show the copy and get approval before designing. Changes are cheaper at this stage.

## 3. Design

**If the Canva connector is available:**
1. Check for a brand kit (`list-brand-kits`) and use it if there's one for this business. Ask which kit if several.
2. Generate an Instagram post design with the approved slide text (`generate-design` / `generate-design-structured`, one page per slide), in the brand kit's colours and fonts.
3. Show the result/link. Offer tweaks, then export as PNG/JPG (`export-design`) if the user wants the files.
Read each Canva tool's schema before calling it. Don't guess parameters.

**If Canva isn't connected:** give a simple design spec the user can build in any app: background colour, text colour (hex), font style, where the logo goes, and one visual idea per slide. Keep it consistent across slides.

Design rules: big text (readable on a phone), high contrast, lots of empty space, the same layout on every slide, a slide number or swipe cue ("→") on the cover, and the logo small on the last slide only.

## Rules
- Never invent facts, prices, eligibility rules, or statistics. Use `[placeholder]` and flag it.
- CSC / government-service info: say "check the latest rules" when details can change.
- UCF: dignified imagery. No identifiable beneficiaries without consent.
