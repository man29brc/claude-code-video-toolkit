---
name: content-calendar
description: Build a monthly content strategy and idea bank for the user's businesses (WVS, CSC Balaji, UCF NGO) — content pillars, a month of post and Reel ideas, festival/seasonal hooks, and a posting rhythm. Use when the user asks for content ideas, what to post, a content plan or calendar for the month, content pillars, or says they've run out of ideas.
---

# Content Calendar

This is the **monthly strategy**. The weekly-social-planner skill turns it into scheduled posts, and reel-script-writer turns Reel ideas into scripts.

## 1. Setup

- **Which business?** WVS, CSC Balaji, or UCF (NGO). Do one business per calendar. If the user wants all three, do them one after another, clearly separated.
- Load that business's profile (offer, audience, location, language, tone, CTA) from memory or preferences. If missing, ask for it in one message.
- **Which month** (default: next month), **how many posts per week** (default: 4, of which 2 are Reels), and **the main goal this month** (enquiries, followers, trust, donations, volunteers, or a specific launch or campaign).
- If performance insights exist (from the instagram-performance-analysis skill, or memory), use them: do more of what worked.

## 2. Content pillars (3–4 per business)

Define pillars that fit the business, each with a one-line purpose. Typical set:
- **Educate:** tips, how-tos, myths, common mistakes, "how it works"
- **Trust / proof:** customer stories, before/after, behind the scenes, team, process
- **Offer:** services, pricing, how to book or apply, FAQs
- **Community / timely:** festivals, local events, deadlines, trends
- For **UCF:** Impact stories · The cause explained · Volunteers & partners · Ask (donate / join)

Suggested mix: ~40% educate, ~30% trust, ~20% offer, ~10% timely/community.

## 3. Dates that matter

List the month's relevant hooks for the business's region: Indian festivals and national days, seasonal needs (exams, monsoon, harvest, tax/filing deadlines, school admissions), and awareness days that fit (especially for UCF). **Only include dates you are confident about.** Mark uncertain ones "verify date".

## 4. Output

```
## <Business> · <Month Year> · Goal: <goal>

**Pillars:** <pillar: purpose> × 3–4

**Key dates:** <date – occasion – post angle>

| Week | Day | Format (Reel/Carousel/Post/Story) | Pillar | Idea / hook | CTA |
|---|---|---|---|---|---|

**Evergreen idea bank (10 spares):** numbered one-liners for when a slot needs filling.
```

Rules for ideas:
- Each idea is specific and filmable ("3 documents to bring for ___"), not vague ("post about services").
- Write the hook as the viewer would hear it in the first 2 seconds.
- Keep it realistic: mostly phone-filmable, low-effort formats, with at most 1–2 "big" pieces a month.

End with: "Want me to script the Reels (reel-script-writer) or schedule week 1 (weekly-social-planner)?"

## Rules
- Never invent facts, prices, results, testimonials, or scheme details. Use `[placeholder]`.
- Keep the three businesses' calendars separate. They can share a festival, but each gets its own angle.
- Offer to save the pillars to memory so next month builds on them.
