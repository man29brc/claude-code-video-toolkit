---
name: finance-compliance-checker
description: Check WVS (Wealth Vriddhi Sahyak) content — Reels, scripts, captions, posts, ads, WhatsApp messages, carousels, Google profile posts — against Indian mutual fund (SEBI/AMFI) and life insurance (IRDAI) promotion rules before it's published. Use whenever content mentions mutual funds, SIP, investing, returns, insurance, policies, term plans, ULIPs, or tax saving, and before any WVS content is scheduled or sent. Also use when the user asks "is this compliant" or "can I post this".
---

# Finance Compliance Checker (WVS)

WVS = Wealth Vriddhi Sahyak: an **AMFI-registered mutual fund distributor** and an **IRDAI-licensed life insurance agent** empanelled with ICICI's life insurer. One non-compliant post can risk the licence, so run this on **every** WVS piece before it goes out.

> This is a practical checklist, not legal advice. Rules change. For anything marked **Ask**, confirm with the insurer's compliance team / branch or AMFI's current guidelines.

## How to run

1. Read the content: script, on-screen text, caption, hashtags, voiceover, thumbnail text, and any ad copy.
2. Check every rule below. Quote the exact problem line.
3. Output:

```
**Verdict:** ✅ OK to post / ⚠️ Fix first / ⛔ Don't post / 📨 Needs insurer approval

| # | Problem (quoted) | Rule | Fix (rewritten line) |
|---|---|---|---|

**Required additions:** <disclaimer text + where it goes (screen/caption/voice)>
**Fixed version:** <full corrected caption/script if changes were needed>
```

## Mutual funds (SEBI / AMFI)

- **Identity:** say "AMFI-registered Mutual Fund Distributor" and show the **ARN** (ask the user for it once, then keep it in memory). **Never** use "advisor", "adviser", "financial advisor", "IFA", "wealth manager", or "investment expert". Those titles need SEBI RIA registration. "Sahyak" as a brand name is fine.
- **Risk disclaimer:** include "Mutual fund investments are subject to market risks, read all scheme related documents carefully." In the caption **and** on screen for videos, where it must be legible. Voice it if the ad is audio-visual. **Ask:** the current SEBI/AMFI rules on on-screen duration and size.
- **No return promises:** ⛔ "guaranteed", "sure-shot", "double your money", "safe returns", "fixed returns", "risk-free", "best fund". Illustrations like "₹5,000 SIP at an assumed 12%" are OK **only if** clearly labelled as an assumed rate, for illustration, not a promise, and not tied to a specific scheme.
- **Past performance:** don't quote a scheme's returns unless in the SEBI-prescribed format. Safer: don't quote scheme returns at all.
- **No specific scheme "tips"** or "buy this fund now" calls. Education (what a SIP is, compounding, goal planning) is fine.
- **No comparisons** that make MFs look guaranteed versus FDs, PPF, etc. Comparison must be fair and mention risk.
- **No finfluencer tie-ups:** don't pay or partner with unregistered influencers who make return claims.

## Life insurance (IRDAI)

- **📨 Insurer approval:** under IRDAI advertising rules, an agent's advertisements generally need the **insurer's prior approval**. Treat any post that promotes insurance products or your insurance services as needing approval, and flag it. Pure education with no product or offer may not, but **Ask** the insurer's compliance.
- **Name products correctly:** if you name a plan, use its exact name and UIN, with "Insurance is the subject matter of solicitation" (commonly required). Safer: talk about categories (e.g. term insurance) rather than named plans.
- **Don't sell insurance as an investment.** No "insurance + guaranteed returns", no ULIP-versus-MF return comparisons, no "tax-free guaranteed income".
- **No rebates or freebies:** ⛔ "cashback", "gift on buying a policy", "first premium discount". Rebating is prohibited.
- **Tax claims:** "Tax benefits as per prevailing tax laws, subject to change." No exact rupee tax-saving promises.
- **No fear-mongering or misleading claims** ("your family will be on the street").

## Both

- Content from the insurer or AMC: use their approved creatives as-is. Don't edit their numbers.
- Testimonials and client stories: get written consent. No return or claim-amount claims. **Ask** before using testimonials in WVS **ads**. Google reviews themselves are fine.
- Don't post client names, policy numbers, PAN or Aadhaar, or screenshots with personal data.
- Storyline Reels with fictional characters: add "Characters are fictional, for illustration" if they could be mistaken for real clients.

## Handy disclaimer block (adapt, then verify)

```
AMFI-registered Mutual Fund Distributor | ARN-[XXXXX]
Mutual fund investments are subject to market risks, read all scheme related documents carefully.
Insurance is the subject matter of solicitation. For more details on risk factors, terms and conditions, please read the sales brochure carefully before concluding a sale.
Tax benefits as per prevailing tax laws, subject to change. For education only; not investment advice.
```
Use only the lines that apply (MF lines for MF content, insurance lines for insurance content).
