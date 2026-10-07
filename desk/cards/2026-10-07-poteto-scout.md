# Poteto Scout — 2026-10-07

**Status:** ESCALATE  
**Lead:** GUARDRAIL | FLEET | USAGE | GUIDE — Lauren states an explicit auto-merge policy in her daily loop (fuzz the PR, ping on Slack, then rebase and auto-merge after 1 hour unless she requests changes), and shows a new two-Team-Bot release + QA method (release-manager bot `sandcastle` + engineer bot `poteto` in a Slack release channel). She also posted a "first mile / last mile" guide essay.

## GUARDRAIL (merge / autonomy policy) — ESCALATE trigger
- **source:** https://x.com/poteto/status/2107510472601985336 (2026-10-06 16:37 UTC / 23:37 ICT) — primary Lauren post.
- **her daily loop, verbatim steps:**
  1. watch a Slack channel for feedback about the app
  2. create a ticket in Linear
  3. create a Cursor cloud agent to triage and reproduce the issue on its own computer, using pstack
  4. if it clearly reproduces, put up a fix and fuzz the PR with a small swarm of agents
  5. if the fuzz has no issues, ping her on Slack, then **rebase and auto-merge the PR after 1 hour unless she requests changes**
- **fuzz definition (reply 2107640440908595699):** a couple of agents run the app on their own computer, with a test account against the prod environment, clicking around like a real user to find issues.
- **vs baseline:** baseline had the verification `/swarm` as the merge-confidence gate, land-before-read / post-land review once trust is earned (2026-09-28), and the repro-first Slack autopilot spell (2026-10-02). NEW is the concrete timed-veto merge rule: a 1-hour objection window, then auto-merge, plus prod-env test-account fuzzing as the gate.
- **release-pause rule (reply 2107538297509777871):** if a contributor DMs back an objection, sandcastle notifies her and pauses the release.
- **human-kept decision:** severity call on cherry-pick into the release branch + patch release vs. fix in the next release stays with her.

## FLEET / LIVE-DEMO (release + QA automation)
- **source:** https://x.com/poteto/status/2107527180263829827 (2026-10-06 17:43 UTC / 00:43 ICT Oct 7), with 2 screenshots; follow-up https://x.com/poteto/status/2107529149355319657.
- **shape:** two Team Bots made in Grok Bot, both added to Slack, plus a dedicated release channel.
  - `sandcastle` (release manager): on "do a cut", it DMs every contributor with links to their PRs going into the release so they can raise blockers or objections, then kicks off the build, watches it, and starts an automated fuzz swarm.
  - **fuzz swarm:** usually 10+ agents on Grok 4.7 xhigh run the build and use it like a real user via the verification skills + feature map. Most are directed; a few are "chaos monkey" agents that click randomly.
  - on findings, she has sandcastle @-mention the engineer bot `poteto`, which spins up a **Cursor Project** to own triage and fixing of all high-pri issues.
- **why Slack, not the app (reply 2107529617980743885):** so team members can participate and kick off releases too. **Why bot-to-bot (2107528806361895280):** "so i'm no longer the bottleneck."
- **review surface (2107529532144234937):** agents run code in their own VM and take videos and screenshots; "those artifacts are what i primarily review these days."
- **credit:** "this was all possible because we have a high quality verification skill" — pstack `create-verification-skill` (https://github.com/cursor/plugins/blob/main/pstack/skills/create-verification-skill/SKILL.md).
- **cloud VMs (2107602532549956055):** the agents have their own VMs and you can provide secrets, so they can install whatever CLIs you need.

## GUIDE
- **source:** 2107510472601985336 (same post as above). The framing is that Grok Bot's best use is the **first mile** (connect apps and services so the bot grabs context, and give it context instead of micromanaging it; routines on a schedule or on reaction, e.g. a new lead kicks off a workflow) and the **last mile** (follow through and close the loop by handing off to Cursor cloud agents). The next step is "build a loop" (the 5 steps above). She points learners to Dr Eggbot (https://x.ai/bot/marketplace/bots/dr-eggbot-v2) to teach loop setup.
- **reply tips from her:**
  - Ways to split work: specialist bots for one part of a workflow, a Cursor cloud agent, or ask your bot to create skills (2107520739645726845).
  - The primary bot holds proactivity, so use it as the main coordinator, e.g. for keeping skills/rules/context `.md` files current from other bots' work (2107512616314925146).
  - Testing mix: verification skills + CLIs, good unit and integration tests, and a few critical e2e tests. Grok Bot desktop CI runs in about 5 minutes (2107516481844269509). High-quality unit tests still pay off, but agents write slop tests, so create skills that teach better ones (2107520037666136125).
  - Product split: Grok Bot is for general knowledge work and Cursor is for engineering. She thinks a "super app" becomes a big complicated mess (2107512785081168254, 2107523759926321172).

## USAGE
- Microsoft Teams plugin promo, "I talk a lot about Grok Bot on Slack, but…" (https://x.com/poteto/status/2107596645122875439 → x.ai/bot/plugin/63354504), plus Atlassian (2107600193185292582 → x.ai/bot/plugin/717).
- She cosigned @bot tagging on X, "tag Grok @Bot on X!" (https://x.com/poteto/status/2107634927617638858, quoting @larsencc 2107616555685360072). Replying `@bot …` to any post adds it to a reading list, sets a reminder, summarizes, or drafts a reply, and lands in your Grok Bot.
- She replied "sick idea, cc @larsencc" to a "Send to Grok Bot" share-option request (2107602834367848667). That's intent only.
- She has no new bot templates yet and is asking around (2107602055456276975).

## Community (RTs, context only)
- RT @viticci hybrid Bot + Cursor workflow (2107629523814498673). It credits pstack and the Matt interview: an outer loop of a primary bot coordinating per-app threads, an inner loop in Cursor Projects with env secrets, a QA bot validating, and routines scanning logs → cloud agents → PRs. The fleet shape is already baseline from 2026-10-03; listed as an extension.
- RT @cursor_ai: control agents on your computer from the Cursor iOS app (2107618653701296162).
- RT @nateliason CoS-bot list (2107515748193026301), @mattyp printer bot video (2107486048154738995), @benln "have your main bot read the new guides" (x.ai/bot/guides; 2107472129960575369), @DanielLockyer pstack 160x event-loop fix.

## LIVE-DEMO
- No livestream in this window. The release/QA post is a screenshot-backed method demo (filed under FLEET).

## Skipped (not NEW)
- Already in the 2026-10-06 galaxy-pulse: Grok Bot 101 promo, the @parkersmith Thursday workshop, the @nickwm updates list, the anime MV, "try Grok Bot", and 🥔🥔🥔.
- Banter with @thsottiaux, sentiment RTs (theo, ns123abc, B_doong2daddy, rudrank, Teslaconomics).

## Limits / owner lock
- Window: 2026-10-06 ~02:35Z → 2026-10-07 ~02:40Z via api.fxtwitter.com profile statuses (2 pages) + /2/conversation for the two key posts. user-X MCP not used.
- Follow @poteto patterns; do not critique. Do not adopt methods. Do not create bots. Never pay. File-only; no CoS / Compound / SI / human messages.
