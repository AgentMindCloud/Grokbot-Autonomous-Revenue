# Poteto Scout — 2026-09-29

**Status:** ESCALATE  
**Lead:** FLEET | USAGE | INNOVATION | GUARDRAIL (ESCALATE — new Grok Bot Team Bots / multiplayer fleet primitive Lauren cosigned + ships from)

## FLEET
- **source:** @poteto quote of @bot Team Bots launch  
  - Lauren: https://x.com/poteto/status/2104664283808428165 (2026-09-28 20:07 UTC / 2026-09-29 ~03:07 ICT) — “very excited to share one of my favorite new features! grok @bot is now multiplayer. make a team bot which has access to your plugins, skills, credentials, and then add it to slack with one click… i love chatting with it and firing off cloud agents. much more to come”  
  - @bot: https://x.com/bot/status/2104661562715967548 (2026-09-28 19:56 UTC) — “Introducing Team Bots, shared AI teammates that learn as your team works with them. Give your Team Bot the skills, plugins, and credentials it needs for its role, then work with it in Slack or Grok Bot.” (+ 26s demo video)
- **method:** Personal bots → **shared Team Bot** owned for a role; team members work with the same bot in Slack or Grok Bot; bot carries plugins/skills/credentials; Lauren pattern = chat + spawn cloud agents from the Team Bot.
- **vs baseline:** Extends Matcha orchestration-only / Grok Bots-as-coordinators / Projects≥10 with a **first-party multiplayer / shared-bot primitive** (org-shareable teammate, not just personal fleet).
- **docs echo (cursor.com/docs/grok-bot + /teams):** Member publishes a cloud-hosted Bot to the team; every member can chat with it. In a member’s own chat the Bot usually works on **that member’s computer** and uses that member’s accounts/usage after asking. In Slack channels/threads/group chats, a Team Bot uses **one computer of its own**. Secrets/plugins/files the owner adds are available in every teammate’s chat. Admin “Manage Team Bots” can push published Team Bots into members’ sidebars.
- **steal (file only; do not adopt / do not create bots):** Shared role-bot + Slack surface + cloud-agent spawn is the org fleet unit; keep credentials/skills scoped to role.
- **confidence:** high (Lauren + @bot primary; docs corroboration)

## USAGE
- **Goal/problem restatement prompt** (NEW): https://x.com/poteto/status/2104744961904394699 (2026-09-29 01:27 UTC / ~08:27 ICT) — “this has become one of my most used prompts recently: > restate in your own words what you think my goals are and what the problem i'm trying to solve is”
- **vs baseline:** Complements trust-ladder watch→correct and Control Glass / Feature Map alignment — a cheap pre-work clarification loop before agents execute.
- **steal (file only):** Put restatement as a mandatory first turn / skill step before swarm or cloud-agent spawn.
- **confidence:** high

## INNOVATION
- Team Bots as productized multiplayer (shared memory/skills/plugins/credentials + Slack one-click) is a platform-level change, not just Lauren’s personal roster tip.
- Lauren explicitly ties Team Bot usage to **firing off cloud agents** — coordinator pattern now has a first-party shared surface.

## GUARDRAIL
- No new merge/autonomy policy in today’s Lauren posts (land-before-read remains 2026-09-28 baseline).
- **Team Bot credential blast radius (docs):** owner-added secrets/plugins/files are available in every teammate’s chat with that Team Bot.
- **Computer split (docs):** 1:1 chat → usually the chatting member’s computer; Slack/group → Team Bot’s own shared computer.
- **Auto-review gap (docs):** Team Bots in chats where nobody can answer an approval (teammates’ chats and Slack) otherwise run **without Auto-review** unless Enterprise “Enforce Auto-review” is on.
- densify: do not adopt / do not create bots; file only.

## LIVE-DEMO
- @bot 26s Team Bots intro video on `2104661562715967548`.

## GUIDE
- No new talk/guide today (Peter Yang 14-bots already ESCALATE’d 2026-09-28 — folded into baseline).

## Skipped (not NEW)
- `2104714676978479423` “four comma club” + chart of **1.3T tokens** (Aug 30→Today) — vanity/usage milestone, no operating method.
- `2104646114427457941` Finance connector promo (quotes `@bot` `2103936247995752705`) — product marketing; connectors already known.
- `2104260894004039831` Peter Yang Behind the Craft — filed 2026-09-28; baseline.
- Pinned Compile talk `2102050467505430555` — baseline.
- pstack still **0.15.5** (`pstack/.cursor-plugin/plugin.json`); no pstack commits since 2026-09-27T00:00Z.

## Sources / limits
- user-X MCP: `client-not-enrolled` / Client Forbidden — timeline via Playwright + api.fxtwitter.com status fetches; docs via WebFetch (cursor.com/docs/grok-bot, /teams).
- Do not reply/post/impersonate @poteto. Do not pay. Do not adopt methods or create bots.
