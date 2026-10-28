# Product marketing context – Remote Ready

The borrowed marketing skills in `.claude/skills/` look for this file first. It points to the real source files in this repo; read the ones the task needs instead of asking me for context.

- Positioning, category, competitors: `positioning.md`
- Audience, personas, trigger moments: `icp-personas.md`
- Offers, prices, status, lead magnets: `offers-pricing.md`
- Voice, messaging pillars, words to avoid: `voice-messaging.md`
- Channels, funnel, content pillars, what we measure: `marketing-strategy.md`
- Stages, decision signal, ad test, income math: `launch-plan.md`

Quick facts:
- Remote Ready (remoteready.mk): Macedonian career brand for people who want to find and grow in remote roles. Group programs and workshops in Macedonian. B2C first, B2B (HR/L&D) as a separate track.
- Stage: go-live / trust phase. No paid offer yet. Primary conversion: email signup.
- Stack: static site on Netlify (repo bosh23/remoteready-site), Kit for email (form 10050233), GA4 (G-XCMFF2Y16Y) with `sign_up` key event, Meta pixel (1513343753991604) with `Lead`. Cookie banner with opt-out, so tracking undercounts.
- Ads: Meta only, small fixed test budget, one ad per problem to the same signup page. Compare ads to each other, not to industry benchmarks.
- Small numbers: early on we're dealing with tens of signups, not thousands. Don't recommend tests or attribution models that need more volume than we have; say so when results aren't significant.
