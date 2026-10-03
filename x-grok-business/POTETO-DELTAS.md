# Poteto Scout deltas — @poteto (2026-09-15)
Source: Poteto Scout (e47d1339…). NEW vs Scout baseline. Research only. Wedge B HOLD.

## Monetize / marketplace / retainers
**NULL from @poteto primary posts.** No Lauren quote on selling bots, retainers, paid share links, or paid bot marketplace.
Closest packaging (not sell-side):
- pstack on Cursor marketplace as skill/plugin (promo: “like hiring me but free”)
- Dr Eggbot shareable template that creates other bots
Do NOT invent a sell model from her. Monetize evidence must come from other actors (Ken, templatebot, 88 Labs, Grokati, outside-canon PRIMARY).

## Mechanism deltas (HOW-THEY-WORKED fuel)

### 1. Fleet — Bots as coordinators, not workers
- Source PRIMARY: Complete Guide to pstack Pt.1, 2026-09-01, post 2094457600259842065
- Mechanism: Grok Bot spawns Cursor cloud agents; bot keeps context clean; cloud agents build/verify on own machines. Prefer cloud agents over local worktrees (“worktrees are dead”).
- Steal: persistent Bot = supervisor; cloud agents = workers; one project per workstream.

### 2. Guardrail — /swarm verification as merge confidence gate
- Sources: same guide + post 2087977008253071816
- Mechanism: /swarm fans cloud agents to run verification skill / fuzz PR stacks; gate for merge-while-sleep.
- Outcome: her PR-volume trajectory claims (1000→~2000/mo) — **not Critic evidence bar** without independent corroboration.

### 3. Product direction — verification as infra + Feature Map
- Source: 2094457600259842065, 2026-09-01
- /create-verification-skill → agent-friendly CLI (“Build the Lever”) + Feature Map as materialized memory; daily /maintain-verification-skill; pin /poteto-mode.
- Shipping direction: shortest path = correct path; verification = critical infra.

### 4. Outer loop factory (X + Slack)
- Source: 2090141955695198633 ~2026-08-31
- Routines farm Slack bugs + **X complaints** + feature ideas → human prioritizes → Full Autopilot = /goal+/loop+/swarm on cloud agents.
- Alias: /lauren-mode == /poteto-mode.

### 5. pstack 0.15.0 packaging
- Source: 2097380152703615396, 2026-09-08
- 3–11% token savings; new principles under /poteto-mode; ships as Cursor marketplace plugin (auto-updates). Skill/plugin packaging ≠ bot-for-sale marketplace.

### 6. Dr Eggbot v0.1→v0.2 (strongest template signal)
- Sources: 2093392701005946931 (v0.1), 2094967827019243547 (v0.2 ~2026-09-02)
- Shareable Bot that creates high-quality bots (coding→pstack); ask Eggbot → engineer bot → verification skill + daily maintain; v0.2 weekly routine health; daily friction skim (“not what i meant”) → suggest skills/bots/routines.
- Reinstall to upgrade; copy state to new bot.
- Creation + fleet hygiene packaging — **not pricing**.

### 7. Live demo pending
- Galaxy Sep 15–17 2026 with @mattyp @roshan_s: blank-slate company in 3 days, Grok Bot only. luma.com/3ifrgttw.
- As of 2026-09-15 morning: Day 1 not demonstrated; ~70k signups = scale only. Recording promised, unposted.
- Ping Poteto Scout after Day 1+ for live bot-split / refuse-to-automate updates.

## Baseline (not new)
pstack for hard tasks; Dune agent-first; /loop+/goal; 20+ agents + CoS; one project/workstream; merge own PRs when confident; CI bans; pstack-everywhere burns tokens.

## Galaxy Day 1+ (2026-09-16 Scout)
See POTETO-GALAXY-DAY1.md — VOD holds method; no text operating-rule deltas yet. Day 2 8:30 AM PT.

---

# Poteto Scout ESCALATE — 2026-09-24 (Asia/Saigon)
Source: Poteto Scout → Super Intel. Owner lock: follow @poteto, no critique. Critic opinions-only. Monetize still NULL.

**Top steal (fleet):** Give each bot a JD that names what it **refuses**, then hand off between seats — not one mega-bot.

## 8) GUIDE — Galaxy game-studio recap publish pattern
- Source PRIMARY: https://x.com/poteto/status/2102835770784694385 (2026-09-23)
- Points to: x.ai/galaxy · thursdayarena.com · x.ai/bot/guides (marketing / dev / GTM)
- Mechanism: After a live build, publish a short recap that links standing playbooks + the shipped product.
- Steal: Recap → playbooks → product links as the closeout artifact (not a long postmortem).
- Confidence: high
- Evidence tag: MOTION-ONLY (method demonstrated/pointed; not a money outcome)

## 9) FLEET — Rank’em six-seat JD / refuse / handoff
- Source: Lauren recap pointer → x.ai/bot/guides/grok-bot-for-mobile-app-development (Rank’em guide, author Ryan Perry; Lauren co-signed via recap)
- Seats (each own computer / todos / overnight): Mobile Orchestrator · Analytics · Creatives · Rank’em Engineer · GCS · Bug fix
- Handoffs without human routing; record-button skills for UI when APIs blocked
- Refuse table (copy this shape):
  - Analytics never writes creative / never touches app code; only Analytics declares a finding
  - Creatives never buys media; human before spend
  - Bug fix fixes obvious + escalates the rest
  - Nothing to players without GCS
- Steal: Rewrite fleet prompts as **owns X / refuses Y / hands off to Z**; spend + merge-to-players behind named gate or human
- Confidence: high for her pointer; medium-high that Rank’em refuse table is the method to copy
- Evidence tag: SURVIVES as mechanism (PRIMARY pointer + detailed guide); OUTCOME UNKNOWN on product metrics

## 10) INNOVATION — pstack 0.15.3 Autopilot-full ops
- Source: cursor/plugins#414 (merged by poteto) → pstack 0.15.3
- Mechanism: Autopilot-full verifies in rounds from code-ready head; children.tsv subagent tracking; tick posts only on tracked change; defaults Opus 5.5 + Grok 4.7; cut skill prose models no longer need
- Steal: children.tsv (or equiv) + delta-only pings; A/B-cut redundant skill text per model tier
- Confidence: high
- Evidence tag: SURVIVES as shipped mechanism in pstack

## 11) GUARDRAIL — pstack 0.15.5 owner vs babysitter + append-only audit
- Source: cursor/plugins#419 + #422 → pstack 0.15.5
- Mechanism: More A/B instruction cuts; standalone babysit still bans rebase/force-push; Autopilot-full/stack **owner** may rebase own branch and `git push --force-with-lease` after `ls-remote`; show-me-your-work is append-only (supersede, never delete)
- Steal: Explicit owner vs babysitter push rules; never delete audit rows — supersede
- Confidence: high
- Evidence tag: SURVIVES as shipped guardrail

## Compound next (draft-only until owner go where needed)
1. Codify seat JD template: owns / refuses / hands off to — apply to Super Intel + Compound pair first
2. Add children.tsv-style workstream tracker + quiet-unless-delta for Scout→Intel→Compound
3. Lock append-only audit for playbook files (supersede rows, no silent delete)
4. Do **not** invent monetize / sell from Galaxy recap or Rank’em

---

# Poteto Scout NEW — 2026-09-25 (Asia/Saigon)
Source: Poteto Scout → Super Intel. File only. Do not adopt. Do not create bots. Monetize still NULL.

## 12) FLEET | USAGE — Many concurrent Cursor Projects + pstack
- Source PRIMARY: https://x.com/poteto/status/2103252563999232092 (2026-09-24 22:37 UTC / ~05:37 ICT 2026-09-25)
- Points to: https://cursor.com/blog/projects (coordinator / shared context / subscriptions; cloud-by-default)
- Mechanism: Cursor Projects + pstack at parallel scale. Routinely **≥10 Projects concurrently** (perf, tech debt, Bend2/rust experiments, user-feedback fixes, dashboards, games).
- Vs baseline: Extends “one project per workstream” + Grok Bot outer-loop → **many concurrent Cursor Project coordinators**, each with pstack.
- Steal (file only; do not adopt): Keep existing Market Desk roles; **no new specialist bots**. Parallel lanes = separate Cursor Projects with pstack — playbook delta for Compound / HOW-THEY-WORKED.
- Confidence: high
- Evidence tag: MOTION-ONLY (method claim + product link; not independent outcome ledger)
- Human: Frontier Friday ACCEPT `d-20260925-06` already on HUMAN.md — do not re-ask.
- Skipped by Scout: “rewrite it in bend”; Galaxy+Rank’em+pstack 0.15.5 already baseline.

---

# Poteto Scout ESCALATE — 2026-09-28 (Asia/Saigon)
Source: Poteto Scout → Super Intel. File only. Do not adopt. Do not create bots. Never pay. Monetize still NULL.

**Top steals:** (1) Matcha = orchestration-only eng lead. (2) Trust ladder watch→correct→skill→one-shot→routine. (3) Land-before-read only after ladder. (4) Design: human first ~5% keyframe → Figma-MCP scale-out.

## 13) GUIDE — Behind the Craft “14 bots” (Lauren + Peng)
- Source PRIMARY: https://x.com/poteto/status/2104260894004039831 (~2026-09-27 17:15Z) quoting Peter Yang; YouTube https://youtu.be/xZ5TEaleUdg; creatoreconomy.so writeup (partial free)
- Mechanism: Co-signed public walkthrough of personal+team bot roster + trust ladder — fills refuse-to-automate / org bot-split writeup gap vs Compile baseline.
- Steal: Treat as HOW-THEY-WORKED primary; do **not** spawn bots from the roster list.
- Confidence: high
- Evidence tag: SURVIVES as mechanism primary (talk/guide); OUTCOME UNKNOWN on desk metrics

## 14) FLEET — Matcha eng-lead orchestration-only + Dr. Eggbot audit
- Mechanism: Big projects → **Matcha** (does not execute; decomposes/routes to eng bots) → eng bots spawn cloud coding agents (“massive agent swarms”). Cross-room PM+design+eng. Dr. Eggbot designs **and audits** other bots.
- Vs baseline: Extends coordinator→cloud agents + Projects≥10 with a **named non-executing lead**.
- Steal: Coordinator ≠ worker; lead seats stay orchestration-only. Meta design/audit seat = fleet hygiene (**file only** — CreateAgent still Needs-go).
- Confidence: high (public takeaways)
- Evidence tag: SURVIVES as mechanism

## 15) USAGE — Design first-5% keyframe + Figma MCP; self-test before merge
- Design bot (Peng): Figma MCP + layout/token skill; human does first ~5% (system + one keyframe); bot extends full flow.
- Self-test before merge restated as bot-owned gate (aligns verification / Autopilot rounds).
- Life/ops bots noted (CoS supplies; trip booking) — **not** desk adopt; never pay from this seat.
- Steal: Keyframe-then-scale design pattern; keep self-test before merge in playbook.
- Confidence: high for public takeaways; medium unpaid full transcript
- Evidence tag: MOTION-ONLY

## 16) GUARDRAIL — Trust ladder + land-before-read
- Trust ladder (quoted): watch → correct → skill → one-shot → routine.
- Autonomy signal: sometimes land PR before human reads — only after trust ladder earned (stronger than Galaxy “Land merges”).
- Steal: Skill→routine promotion gate; **do not** loosen merge/land-before-read without one-shot reliability.
- Michelin kitchen restated = Compile baseline (not NEW alone).
- Confidence: high
- Evidence tag: SURVIVES as policy signal


---

# Poteto Scout ESCALATE — 2026-09-29 (Asia/Saigon)
Source: Poteto Scout → Super Intel. File only. Do not adopt. Do not create bots. Never pay. Monetize still NULL.

**Top steals:** (1) Team Bots = first-party shared role-bot + Slack + cloud-agent spawn. (2) Restatement prompt before swarm/execute.

## 17) FLEET | INNOVATION | GUARDRAIL — Team Bots multiplayer
- Source PRIMARY: Lauren https://x.com/poteto/status/2104664283808428165 (2026-09-28 20:07Z) quoting @bot https://x.com/bot/status/2104661562715967548; docs: cursor.com/docs/grok-bot + /teams
- Mechanism: Personal bots → **shared Team Bot** for a role; plugins/skills/credentials on the bot; members chat in Grok Bot or Slack (one-click); Lauren pattern = chat + fire cloud agents. Docs: member 1:1 chat → usually that member’s computer; Slack/group → Team Bot’s own computer; owner secrets available to all teammates; Auto-review off in Slack/teammate chats unless Enterprise Enforce Auto-review.
- Vs baseline: Extends Matcha orchestration-only / Grok-Bots-as-coordinators / Projects≥10 with a **first-party shared-bot / multiplayer primitive**.
- Steal (file only; densify: do not adopt / do not create bots): Org fleet unit = shared role-bot + Slack surface + cloud-agent spawn; scope credentials/skills to role; note credential blast radius + Auto-review gap.
- Confidence: high
- Evidence tag: SURVIVES as mechanism (Lauren + @bot + docs); OUTCOME UNKNOWN on desk metrics
- Skipped by Scout: 1.3T tokens vanity; Finance connector promo; Peter Yang 14-bots (already 2026-09-28); Compile pin; pstack still 0.15.5

## 18) USAGE — Goal/problem restatement prompt
- Source PRIMARY: https://x.com/poteto/status/2104744961904394699 (2026-09-29 01:27Z)
- Mechanism: Most-used prompt: “restate in your own words what you think my goals are and what the problem i'm trying to solve is”
- Vs baseline: Complements trust-ladder watch→correct and Control Glass / Feature Map alignment — cheap pre-work clarification before agents execute.
- Steal (file only): Restatement as mandatory first turn / skill step before swarm or cloud-agent spawn.
- Confidence: high
- Evidence tag: MOTION-ONLY (usage tip; no independent outcome ledger)


---

# Poteto Scout ESCALATE — 2026-10-01 (Asia/Saigon)
Source: Poteto Scout → Super Intel. File only. Do not adopt. Do not create bots. Never pay. Monetize still NULL.

**Top steals:** (1) Team engineer bot = Slack manager → @ for coding → create Projects / cloud agents (bot stays manager). (2) GUIDE watch: Matt Pocock live Fri 2026-10-02 9AM PT.

## 19) FLEET | USAGE | INNOVATION — Team engineer as Slack manager → Projects
- Source PRIMARY: Lauren https://x.com/poteto/status/2105377066942349794 (2026-09-30 19:19Z) quoting @bot https://x.com/bot/status/2105373767568621895
- Mechanism (Lauren recipe): (1) Create new **team engineer bot** + Slack; (2) `@` bot for coding work; (3) Tell it to **create new Projects** (group related agents into one conversation). Cloud agents: any Cursor model; each has own computer → bot is **manager**, not coder. Product also: hand off coding to Cursor; manage PRs with GitHub + Origin plugins; share video demos.
- Vs baseline: Extends Team Bots multiplayer (L17) + Matcha orchestration (L14) + Projects≥10 (L12) with explicit **manager split recipe** and Slack `@` as default intake.
- Steal (file only; densify: do not adopt / do not create bots): Role Team Bot on Slack → @ for work → spawn Projects/cloud agents; keep bot managerial.
- Confidence: high
- Evidence tag: SURVIVES as mechanism (Lauren + @bot); OUTCOME UNKNOWN on desk metrics
- Skipped by Scout: burnout personal post; pstack still 0.15.5

## 20) GUIDE — Matt Pocock live (watch/file when live)
- Source: Lauren https://x.com/poteto/status/2105324768186777634 → Matt https://x.com/mattpocockuk/status/2105239236178018636 → https://youtube.com/live/MN9dGgmLyso
- Mechanism: Cosigned live YouTube Fri 2026-10-02 9AM PT (~23:00 ICT) — skills, high-velocity software factories, SOTA agent shipping.
- Steal (file only): Watch/file when live; **do not invent content before air**.
- Confidence: high for schedule/cosign; content pending
- Evidence tag: MOTION-ONLY until VOD/transcript filed
