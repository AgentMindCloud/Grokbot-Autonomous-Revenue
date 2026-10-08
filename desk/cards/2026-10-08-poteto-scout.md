# Poteto Scout — 2026-10-08

**Status:** NEW  
**Lead:** INNOVATION | GUIDE | USAGE — Lauren floats "time to (fully automated, hands-off) rewrite" (TTR) as a thought-experiment heuristic for how agent-ready a codebase is; posts a first-timer onboarding guide (connect apps first, do everything with one bot before adding more); and closes the product loop with Grok Bot's new native X monitoring (X feedback → issue tracker / Cursor cloud agent).

## INNOVATION — "time to rewrite" (TTR)
- **source:** https://x.com/poteto/status/2107913381751730352 (2026-10-07 19:18 UTC / 02:18 ICT Oct 8). Primary Lauren post, explicitly "a thought experiment and rough heuristic, not a real number that can be compared"; "not a fully formed idea yet".
- **the question:** if you decided to rewrite your code in a different language/framework/architecture, how long would it take a single engineer, fully automated and hands off? The number matters less than the questions it raises about making the codebase more legible and productive for agents.
- **probes she lists:**
  - If TTR feels high because you wouldn't trust the result (agents can't verify and prove identical user-visible behavior), that gap is likely slowing you and your agents today too.
  - Rewrite quality: is perf better, same, or regressed? Is the code easy to delete and extend? Will it hold quality as PRs flow in?
- **reply extensions (via /2/conversation):**
  - Token efficiency framing: agents that can't verify their work cause bugs and rework, which cost more tokens (and unhappy customers). Ways to lower TTR deterministically include a high-quality test suite and libraries like XState or Effect to enforce business-logic invariants; "your codebase is a form of memory" (2107922229711585334).
  - Possible measures: % of agent-written code that gets merged, revert/rework rate, and # of human messages per accepted PR, lower is better (2107923381001781362).
  - Working backwards: imagining a rewrite is a way to find improvements to existing legacy code; good engineering still matters (2107920188494709220, 2107925381340905809).
- **vs baseline:** baseline has the verification skill as infra, swarm as merge gate, and constraints-as-agent-management (2026-10-05). NEW is the TTR lens itself plus the three candidate agent-readiness measures.

## GUIDE — first-time onboarding
- **source:** https://x.com/poteto/status/2107830403549831186 (2026-10-07 13:48 UTC / 20:48 ICT).
- **steps:**
  1. First connect the apps you use regularly (calendar, Slack, issue tracker, CRM, Google Drive) so the bot has context and tools.
  2. Don't rush into multiple bots. The primary bot is very capable alone; she recommends doing everything with one bot first.
  3. Add bots later for specialization and organization. One bot does the work you'd normally do; several bots are like a team you design around how you work. GTM examples: one bot per customer, or specialists for one slice of the workflow such as an Outreach bot.
  4. When ready, use the bot marketplace (https://x.ai/bot/marketplace) or her bot designer Dr Eggbot (https://x.ai/bot/_jOdbfkB16zxu7MRcmReE).
- **vs baseline:** first-mile/last-mile guide (2026-10-07) already had "connect apps first" and Dr Eggbot. NEW is the explicit one-bot-first sequencing and the per-customer vs specialist team-design examples.

## USAGE — X monitoring closes the loop
- **source:** https://x.com/poteto/status/2107963437154435182 (2026-10-07 22:37 UTC / 05:37 ICT Oct 8), quoting @bot "Grok Bot can now search, read, and monitor X" (RT 2107949161878606089).
- **pattern:** ask your bot to monitor X for user feedback on your products; send feature requests to your issue tracker and bug reports to a Cursor cloud agent or Project to triage and fix. "the loop is complete."
- **note:** available to all users with no X connector setup (2107963575105192357).
- **vs baseline:** "Grok Bot routines farm Slack/X into an outer loop" and the Slack→Linear→cloud agent daily loop are known. NEW is native X monitoring as the feedback intake, with no connector.

## FLEET (community, context only)
- RT @vinvan "merged 145 prs so far today", calling it the @poteto playbook: lots of tokens; one Project (orchestrator) per workstream and only talk to those; projects spawn cloud agents in poteto mode; verify with cross-model reviews (2107995483981361243). Project-per-workstream is baseline; cross-model review as the verify step is a community framing she amplified.

## Product context (RTs)
- @ericzakariasson Grok Bot 0.68.1: slide decks (PowerPoint / Google Slides), formatted email from draft cards, bot color in 1:1 chat, faster computer use on 1920x1200 (2107887770937283028).
- @mattyp "What's new in Grok Bot" video: Main @Bot, engineering updates, knowledge work + Google connectors, Team Bots in Slack, Team Bot voice calls/status lines, plugin search with Cmd-K (2107886668892057614).
- @elonmusk model routing: simple requests to small fast models (a fast Grok 4.8 when it ships), complex ones to large models (2107849623364895151, 2107894231922876510).
- @AlexFinn update video (dedicated email address, Opus in Grok, Cursor integration, Main bot; 2107993702144851992); @zachdavis "Cringe Bot" team QA bot running 3x/week with up to 5 screenshot findings (2107882019367821400).

## LIVE-DEMO
- None in this window. @parkersmith's Thursday Oct 8 workshop is already known; she isn't presenting.

## Skipped (not NEW)
- Already covered by 10-07 galaxy-pulse: "Grok Bot is getting an upgrade!" quote of the Elon backend-model note, parkersmith screenshot call.
- @theo / @peterpme token-cost debate about her public Cursor profile (RT, community), @liam_fallen follow list, hiring RT, sentiment RTs (unclebobmartin, iruletheworldmo, liam_fallen, Jason).

## Limits / owner lock
- Window: 2026-10-07 ~02:40Z → 2026-10-08 ~02:40Z via api.fxtwitter.com profile statuses (2 pages, curl UA) + /2/conversation for the TTR post. user-X MCP not used.
- Follow @poteto patterns; do not critique. Do not adopt methods. Do not create bots. Never pay. File-only; no CoS / Compound / SI / human messages.
