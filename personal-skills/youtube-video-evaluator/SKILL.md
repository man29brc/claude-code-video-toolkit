---
name: youtube-video-evaluator
description: Judge whether a YouTube video is worth the user's time. Use when the user shares a YouTube link, a video transcript, or a video description/chapter list and asks if it is useful, worth watching, relevant, or what to take from it. Produces a watch/skim/skip verdict, which timestamps to watch, what to skip, and concrete actions.
---

# YouTube Video Evaluator

Goal: save the user time. Tell them whether to watch, which minutes matter, and what to do with it.

## 1. Get the content (try in order, stop when you have enough)

1. **What the user pasted.** A description with chapters/key points is often enough. A transcript is best.
2. **Fetch it yourself.** Try the video page with a web fetch tool; for the transcript, try `yt-dlp --skip-download --write-auto-subs` if a shell is available.
3. **Search.** Search the video ID and title. Transcript and summary sites (youtubesummary.com and similar) often have it. **Check the video ID matches** before using anything.
4. **Ask.** If all of that fails, ask the user to paste the transcript: on YouTube, open the description → **Show transcript**, then copy the text.

Always tell the user what you based the verdict on (full transcript, description only, or a third-party summary). Say plainly if you did not see the visuals.

Watch for a **different video ID** in pasted chapter links versus the link the user gave. If they differ, say so.

## 2. Work out what "helpful" means for this user

Before judging, check what you know about the user: memory, preferences, project files, connected tools, and skills they already have. The user runs three lines of work (WVS, CSC Balaji, and UCF, an NGO), creates short-form video content, and uses Claude with connectors and skills. If the relevant goal is unclear, judge against their general setup and say one line about which goal would sharpen the verdict.

**Judge against what they already have, not in the abstract.** A great beginner video is a skip for someone already doing it.

## 3. Output format (keep to this)

```
**Verdict: <Watch / Skim ~N minutes / Skip>.** <one sentence why>

<1–2 lines: what the video is — title, creator, length, core idea>

**Watch these parts:**
| Timestamp | Why it's worth it for you |
|---|---|

**Skip:** <sections and why — usually "you already have/do this">

## What to apply
1. <concrete action, tied to their business or setup>
2. ...
(2–3 items max)

<one-line offer to set up item 1>
```

Rules:
- Verdict first. No long preamble.
- Time estimate for "Skim" = the sum of the recommended sections.
- Flag clickbait honestly (e.g. "'99%' is marketing, not a measurement").
- Flag anything outdated, risky (security, sharing sensitive data) or a sales funnel.
- Never invent timestamps. If there are no chapters, describe sections instead.
- List the sources you used at the end if any came from the web.
