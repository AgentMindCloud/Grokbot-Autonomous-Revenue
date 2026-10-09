# Poteto Scout — 2026-10-09

**Status:** ESCALATE  
**Lead:** GUARDRAIL | INNOVATION | USAGE | FLEET | GUIDE — Lauren names **agentic code review** that risk-scores every PR and lets low–medium risk merge without human review (plus bugbot; "agentic forge" still cooking), shows a concrete **X→Slack dual-bot** relay (mention/monitor bot → Slack report; Slack bot runs pstack triage/repro/fix), and posts a longform **"volume does matter"** guide for the software-factory / Michelin-kitchen job.

## GUARDRAIL | INNOVATION — agentic code review / agentic forge
- **source:** https://x.com/poteto/status/2108283057581195413 (2026-10-08 19:47 UTC / 02:47 ICT Oct 9), reply to @emilkowalski asking whether human review is required for her parallel PR volume.
- **pattern:** "we have agentic code review, so every PR gets assessed for risk. low-medium risk ones don't require a review so you just merge it. also bugbot of course"
- **forward look:** "there's many more interesting ideas we have for the agentic forge that we've been discussing cc @jacobgold"
- **aspiration echo:** https://x.com/poteto/status/2108329348600381660 — "figure out how to make human code review obsolete" (reply to someone saying human CR is the bottleneck).
- **vs baseline:** 2026-10-07 had Slack→Linear→cloud agent→fuzz→Slack ping→**rebase + auto-merge after 1h unless changes requested**. NEW is an explicit **risk-tier gate**: agentic CR decides whether a human review is required at all; low–medium risk merges without it. "Agentic forge" is named as the research umbrella.
- **ESCALATE reason:** merge / autonomy policy change.

## USAGE | FLEET — X→Slack dual-bot + live digest prompt
- **architecture (explicit):** https://x.com/poteto/status/2108253488451100877 (2026-10-08 17:49 UTC) — "i set it up so my bot that responds to my X mentions just sends the report to slack, where i have another bot (that is added to slack) uses pstack to do the triage/repro and fix" (screenshot attached in thread).
- **live prompt template:** https://x.com/poteto/status/2108232222163812795 (2026-10-08 16:25 UTC) — `@bot look out for interesting things people are doing with Grok Bot on X and slack me a daily digest at 9am. if there's anything relevant, pick the coolest ideas and suggest how I can use it to improve my workflow`
- **live @bot ops on X:** multiple `@bot repro this` / `triage/repro this` / `@bot @bot repro on windows` tags in-thread (e.g. 2108236736384159941, 2108263247766016205, 2108266733895295377, 2108352509555405251).
- **how-to for tagging:** https://x.com/poteto/status/2108232974672224484 — sign into grok.com with the Grok Bot email and link X before `@bot` tags work.
- **vs baseline:** 2026-10-08 USAGE had native X monitoring → issue tracker / cloud agent ("loop is complete"). NEW is the **two-bot relay** (X-facing bot → Slack handoff → Slack bot + pstack) plus a **copyable daily digest prompt**.

## GUIDE — "volume does matter" / software factory
- **source:** https://x.com/poteto/status/2108290818746528017 (2026-10-08 20:17 UTC), long note_tweet quoting @emilkowalski's "why 100s of PRs/day?" question.
- **core claims she ships in this post:**
  - Pre-agent volume mattered only at the tails (struggling vs "coding machine"); agents make the coding-machine archetype available to everyone, so flat PR volume vs pre-agent baseline is a signal to pause.
  - Trust (links Compile talk 2102050467505430555) is the prerequisite to scale; without it you cannot raise throughput.
  - Cost framing = **cost per intelligence** (tokens expensive now, likely cheaper; one engineer + agents vs hiring tens/hundreds).
  - Job change: not merely produce software — **build the machine that writes the software**; she calls this a **software factory** or **Michelin kitchen**, still a research topic she shares to show what rigor at agent scale unlocks.
- **related replies in-thread:**
  - Parallel portfolio that "adds up" under pstack (perf, user-bug fixes, agent-friendly refactors, skills, features, UI polish, harness, release/o11y, side projects) — https://x.com/poteto/status/2108279582088671583 + pstack plugin link.
  - "you design the machine and the conveyor belts" — https://x.com/poteto/status/2108295872052359290
  - Prioritization unchanged: (1) user experience, (2) anything that helps the team move faster; now everything can run in parallel — https://x.com/poteto/status/2108300758605320594
  - "ask your agent" for visualizations/diagrams when stuck understanding — https://x.com/poteto/status/2108297694561394852
  - Re-points skeptics at her Compile talk (~6 months + lots of refactoring to go from human-sized PR volume to current) — https://x.com/poteto/status/2108320890333388854
- **vs baseline:** Ship Company / coding-machine / software-factory themes and the Compile talk are known. NEW is the full **volume essay**, the **Michelin kitchen** name, cost-per-intelligence, and the concrete parallel workstream list.

## Product / community context (not NEW ops)
- Cosign RT Elon: "You could build an entire company made of Grok Bots!" (2108348616306008532 quoting 2108298090755031284) — product/Galaxy-adjacent; no live company-build method from her.
- Shopify + Grok Bot connector promo + plugin link (2108234315096330255, 2108338959386554546) — product.
- Omarchy feedback call + community PR to bump packaged Grok Bot (2108261735199371451) — community/product.
- RT rowancheung native-X routine pack; RT @bot Shopify help — already-known native X monitoring surface.
- "you should be more ambitious / way more ambitious" (2108299315764777171) — meme, not an operating pattern.
- @parkersmith workshop re-promo (2108161535990517941) — already known; she isn't presenting.

## LIVE-DEMO
- None by Lauren in this window (no Galaxy livestream / live company-build table). Workshop was @parkersmith.

## Skipped (not NEW)
- Galaxy-pulse 2026-10-08 already noted vanity bot email joke (tibo@mail.grokbot.com).
- Sentiment / celebration RTs; Omarchy Mac install aside; short congrats.

## Limits / owner lock
- Window: 2026-10-08 ~02:40Z → 2026-10-09 ~02:40Z via X `get_users_posts` (paginated) + `get_posts_by_ids` for long notes.
- Follow @poteto patterns; do not critique. Do not adopt methods. Do not create bots. Never pay. File-only; no CoS / Compound / SI / human messages.
