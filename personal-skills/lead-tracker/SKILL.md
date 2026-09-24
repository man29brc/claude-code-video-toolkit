---
name: lead-tracker
description: Log and track leads for WVS, CSC Balaji and UCF in one Google Sheet — source, product, stage, next follow-up — and report progress against the 15-leads-per-week target, conversion by stage, and which sources actually work. Use when the user says "new lead", "log this lead", "update lead", "how many leads this week", "lead report", "who should I follow up today", or pastes enquiry details.
---

# Lead Tracker

**Target: at least 15 leads a week** across the businesses, growing steadily. The tracker shows where leads come from and where they get stuck.

## 1. The sheet

One Google Sheet named **"Lead Tracker"** in the user's Drive (use `search_files`; if missing, ask once, then create it with the Google Drive connector).
Columns:

| Date | Name | Business (WVS/CSC/UCF) | Product (Term/Health-CSC/MF-SIP/Home loan/PAN/Other/Donor/Volunteer) | Source (Instagram/Facebook/Google profile/WhatsApp/Referral partner/Ads/Other) | Content that brought them | Stage | Next action | Next follow-up date | Value (₹ est.) | Notes |

Stages: **New → Contacted → Qualified → Meeting/Docs → Proposal → Won / Lost (reason)**

**Privacy:** name and phone or city only. **Never** store PAN, Aadhaar, bank or policy numbers, income proofs or health details.

If Drive isn't available, keep the log as a table in the chat and give the user CSV text to paste.

## 2. Logging

When the user mentions a lead ("Priya from Alkapuri asked about a term plan on Instagram"), extract the fields, confirm in one line, and append the row. Ask only for missing **Business, Product and Source**. Always set a next follow-up date (default: tomorrow for New).

Update stages the same way ("Priya → proposal sent").

## 3. Daily: "who to follow up today"

List the leads whose follow-up date is today or overdue, grouped by business, with the suggested next message (hand off to **whatsapp-closer** for the wording).

## 4. Weekly report (also used by weekly-mentor-checkin)

```
**Week <dates>: <N> leads / target 15** <✅ or gap of X>

| Business | New leads | Won | Conversion |
|---|---|---|---|

**By source:** <source: leads, won>. Best: <X> · Wasted effort: <Y>
**By content:** top 3 posts/reels that brought leads
**Stuck at:** <stage with the most drop-off> → <one fix>
**Overdue follow-ups:** <n>
```

Then one direct recommendation (≤50 words): what to do more of next week and why.

## Rules
- Never invent leads or numbers. Report only what's logged.
- Keep the three businesses distinct in reports, even though they share one sheet.
