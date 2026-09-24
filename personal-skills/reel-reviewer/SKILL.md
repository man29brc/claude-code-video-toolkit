---
name: reel-reviewer
description: Watch and critique a Reel/Short before or after posting — hook, first 3 seconds, pacing, on-screen text, captions, audio, visuals, CTA and (for WVS) compliance — and give a score plus the top fixes and rewritten hooks. Use when the user uploads a video file, shares screenshots or a script of a Reel, or asks "review my reel", "why did this reel flop", "is this reel good", or "what should I fix".
---

# Reel Reviewer

## 1. Get the reel

Instagram and YouTube links usually **can't be opened**. Ask for the **video file** (download it from Instagram: ⋯ → Save/Download, or from the phone gallery).

**If code execution is available and a video was uploaded:**
- Probe it: `ffprobe` for duration, resolution and fps.
- Extract frames: every 0.5s for the first 3s, then every 1.5–2s (`ffmpeg -i in.mp4 -vf fps=... frame_%03d.jpg`). Make a contact sheet if there are many.
- Get the words: transcribe the audio with Whisper if available. Otherwise ask the user to paste the script or voiceover text.
- Look at the frames yourself (text size, safe zones, visual variety).

**If video can't be processed:** ask for 4–6 screenshots (the first frame, 1s, 3s, the middle, the CTA) plus the script and caption.

Say what you actually reviewed (video frames + audio, or screenshots + script).

## 2. Score (each 0–10, one line why)

| Area | What good looks like |
|---|---|
| **Hook (0–3s)** | Problem, curiosity or a number in the first 1–2s. Movement in frame 1. No logo or intro. |
| **Retention / pacing** | A visual change every 1.5–3s. No dead air. Story keeps moving. |
| **On-screen text** | ≤6 words at a time, big, high contrast, **inside the safe zone**: not the bottom ~20% (caption and buttons) or the right edge (icons). |
| **Captions** | Burned-in subtitles for sound-off viewers, in sync with speech. |
| **Audio** | Voice clear and louder than the music. No clipping. Pace 140–170 words/min. |
| **Visual quality** | 9:16, 1080×1920, sharp, consistent style. |
| **Message** | One clear idea the viewer can repeat. |
| **CTA** | One specific action (comment a word / WhatsApp / save) in the last 3–5s. |
| **Compliance (WVS)** | Run **finance-compliance-checker**: disclaimer, ARN, no return promises, insurer approval. |

## 3. Output

```
**Overall: X/10** — <one sentence>
Reviewed: <video frames + audio / screenshots + script>

| Area | Score | Why |
|---|---|---|

## Fix these 3 first
1. <fix> → <why it helps, ≤50 words>
2. ...
3. ...

## Better hooks (pick one)
1. "<hook>"
2. "<hook>"
3. "<hook>"

## Caption fix
<rewritten caption if needed>
```

If the reel is already posted and the user has stats (views, average watch time, skip rate, shares, saves), use them. For example, a high skip rate means fix the hook, and a low watch time means fix the pacing.
Keep it direct and kind. Always give the fix, not just the problem.
