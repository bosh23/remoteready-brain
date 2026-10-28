---
name: dashboard
description: Build the Remote Ready weekly or monthly metrics dashboard from Kit, GA4, Meta Ads and Instagram numbers. Use when I say /dashboard, "how are we doing", "weekly numbers", "metrics", or paste/export analytics data.
---

# /dashboard

Turns my raw numbers into one dashboard I can read in 2 minutes. I'm good at the story, not at wrangling data, so do the wrangling and show me the story.

## Inputs (use what's available, ask only for what's missing)
1. **Kit** (subscribers, new signups by source/form, email opens/clicks). Use the Kit connector if available; otherwise ask me for a CSV export.
2. **GA4** (sessions, `sign_up` events, top sources, landing page conversion). Ask me for an export or screenshot numbers.
3. **Meta Ads** (spend, impressions, clicks, `Lead` events per ad). Ask for the Ads Manager CSV export.
4. **Instagram** (followers, reach, saves, shares, DMs per post). Screenshot or numbers I paste.
5. Save every raw file I give you to `data/<YYYY-MM-DD>/` so we keep history. Never edit raw files.

## What to show (from marketing-strategy.md "What we measure")
- **Headline numbers:** email subscribers (total + new this period), signups by source, cost per signup per ad, live session attendance and sales once they exist.
- **Progress to the decision signal:** subscribers vs ~100, weeks since go-live vs 6 (launch-plan.md).
- **Ad test:** cost per signup per ad (one ad per problem), side by side. This is the main input for picking the first offer.
- **Content signal:** which pillar got the most saves, shares, replies, and signups.
- **Secondary:** followers and reach. Keep them small on the page.

## Rules
- Compute everything in code (Python), never in my head. Show the period and date range on every number.
- Rates only divide matching periods (no full-month spend ÷ partial-week results).
- Small numbers: when a difference is a few signups, say it's not a real signal yet.
- Cookie opt-outs undercount GA4 and Meta. Kit is the ground truth for signups.
- Don't invent or estimate missing numbers. Show "—" and list what's missing.

## Output
1. One HTML dashboard: `dashboards/<YYYY-MM-DD>.html`, self-contained, Remote Ready colors (Ink #1A1A2E, Purple #6B4EFF, Lavender #C9B8F0, Mint #BDEBD5, off-white #F7F5FA), Manrope/Inter, readable on a phone.
2. Below the charts, **3 lines max**: what changed, what it means, one thing to do next week.
3. Append one line to `data/log.csv`: date, subscribers, new signups, spend, cost per signup, notes. This builds the trend over time.
4. If the numbers suggest a persona or offer insight, propose (don't make) an update to `icp-personas.md` validation log.
