---
name: weekly-buffer-planner
description: Plan a week of social media posts for the user's businesses (WVS, CSC Balaji, UCF NGO) and schedule them in Buffer. Use when the user asks to plan the week's content, fill the posting calendar, schedule posts, or "do this week's Buffer". Plans, drafts captions, gets approval, then creates the posts in Buffer.
---

# Weekly Buffer Planner

**Nothing is published or scheduled without the user's explicit approval of the final plan.**

## 1. Scope

Ask (in one message, only what's unknown):
- Which business(es) this week: WVS, CSC Balaji, UCF, or several? Plan each business separately, with each brand on its own channels only.
- Which week (default: next Monday–Sunday) and time zone (default: Asia/Kolkata, IST).
- How many posts per business (default: 3–5), and what's already filmed or ready?
- Anything happening this week: offers, events, deadlines, festivals, campaigns?

Load each business's profile (offer, audience, language, tone, CTA) from memory, preferences, or project files. If missing, ask the same four profile questions as the reel-script-writer skill.

## 2. Check Buffer

Using the Buffer connector:
1. `get_account`. If there are several organizations, name them and confirm which one to use.
2. `list_channels`: map each business to its channels. Confirm the mapping with the user the first time and suggest saving it to memory.
3. `list_posts` for the target week, so you don't double-book slots or repeat recent topics.
4. Optionally `get_aggregated_post_metrics` for the last 30 days. Mention what performed best and lean the plan toward it.

If the Buffer connector isn't available, still produce the plan and tell the user how to connect Buffer.

## 3. Plan

Content mix per business per week (adjust to the post count):
- **Value / educate:** a tip, how-to, or common mistake
- **Proof:** a customer result, a behind-the-scenes look, or (for UCF) impact and a real story
- **Offer / ask:** the service CTA, or (for UCF) donate or volunteer
- **Timely:** a festival, local event, or deadline, if relevant

Posting times: default to evenings 7–9 PM IST and late mornings 11 AM–1 PM. Prefer times that the metrics show work better.

## 4. Present for approval

```
**Week of <date> · <Business>**

| Day & time (IST) | Channel(s) | Type | Post idea | Media needed | Status |
|---|---|---|---|---|---|

**Captions**
1. <Day> — <full caption with CTA and hashtags>
...
```

Mark items needing media the user doesn't have yet as **"needs media"**. For Reel slots, offer to write the script (reel-script-writer skill).

Ask: "Approve all, or tell me what to change?"

## 5. Schedule (after approval only)

- Use `create_post` for each approved post, with the exact `channelId` from `list_channels` and the approved time.
- Posts marked "needs media": create them as **drafts or ideas** (`create_idea`), not scheduled posts.
- Then `list_posts` to verify, and report back with a short table (scheduled / drafted / failed, and why).

## Rules
- Never invent facts, prices, results, or testimonials. Use `[placeholder]`.
- Don't cross-post one business's content to another business's channels.
- If any scheduling call fails, stop, report which succeeded, and don't retry blindly.
