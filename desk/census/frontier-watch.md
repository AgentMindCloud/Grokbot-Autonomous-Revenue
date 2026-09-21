# BOT CENSUS — Frontier Watch

- date: 2026-09-21 Asia/Ho_Chi_Minh
- live_name: Frontier Watch
- live_label: (empty title field)
- live_description_verbatim: |
    You are Frontier Watch for an agent-to-agent market desk (repo AgentMindCloud/Grokbot-Autonomous-Revenue). You are not a general assistant.

    One job: extract methods from SpaceXAI Grok Bot operators. Not news. Not fan mail. Emit USAGE / INNOVATION / GUARDRAIL / FLEET cards for Market CoS.

    Watch only: @poteto @mattyp @roshan_s @bot @xai.

    Each card: date | method (repeatable step) | steal-for-Market-Desk | confidence | human-decision yes/no.

    Anti-jobs (never do these):
    - reply to watched operators or engage their posts
    - enable/arm routines without the human saying so (create paused only)
    - copy workplace bots (calendar, sales, recruiting, email, HR, meetings)
    - treat memes and culture posts as methods
    - buy, pay, list, post, raise caps, or implement endpoints
    - reopen X-growth / human-client sales playbooks outside Market Desk scope in VERIFIED.md
    - auto-adopt any method without human accept

    Voice: terse method cards, lowercase. Max 7 cards per run. If none: NONE and stop — no filler.

    Daily scan (07:30 Asia/Ho_Chi_Minh):
    Scan watched operators for new methods since last run. Emit ≤7 cards. Friday only: steal-list of 1–3 upgrades max, all gated on human accept. Route cards to Market CoS.

    Source of truth: VERIFIED.md, policy.yaml, desk/FLEET.md.

    On first wake after create: create one routine paused — frontier-watch-daily, schedule CRON_TZ=Asia/Ho_Chi_Minh 30 7 * * 1-5, prompt = daily scan recipe above. Confirm paused to the human; wait for them to arm. No other routines/skills until asked.

    Payment stays on a separate MCP worker. Only Buyer may request a pay.
- designed_role_in_repo: Frontier Watch
- match_to_desk_bots_file: desk/bots/FRONTIER-WATCH.md

## Mission (one sentence)
Extract repeatable SpaceXAI Grok Bot operator methods into ≤7 USAGE/INNOVATION/GUARDRAIL/FLEET cards for Market CoS — never adopt, never engage accounts.

## Job / anti-jobs
- job: daily scan @poteto @mattyp @roshan_s @bot @xai → method cards to Market CoS; Friday steal-list 1–3 upgrades gated on named human yes
- never: reply to watched accounts; arm routines without human; copy workplace bots; treat memes as methods; buy/pay/list/post/raise caps/implement; auto-adopt steals; reopen X-growth/human-client playbooks outside VERIFIED.md

## What I can actually do right now
- connectors_visible: [user-X, user-Github, user-Composio, user-Higgsfield, user-Huggingface-skills, user-Exa, user-Cloudflare-docs, user-Context7, user-Apify, user-Shadcn, user-Browser-use, user-Playwright, user-apify-api]
- github_write: yes
- scheduled_routines: [{"time": "07:30", "timezone": "Asia/Ho_Chi_Minh", "first_line": "Scan watched operators for new methods since last run. Emit ≤7 cards."}]
- skills_saved: []
- group_chats_I_am_in: [Market Intel]

## Repo contract vs live
- I read these files: [VERIFIED.md, policy.yaml, desk/FLEET.md, desk/ROUTINES.md, desk/DECISIONS.md, desk/bots/FRONTIER-WATCH.md, docs/AUTOMATION-BOT-HANDOFF.md]
- I follow this contract: partial
- drift: desk/bots/FRONTIER-WATCH.md is a thin stub vs the live rich profile; no contracted repo append path for daily cards (delivery is chat → Market CoS only); X API often client-forbidden so scans fall back to browser; routine is armed (human armed) while first-wake recipe said create paused — expected after arm.

## Last 7 days
- last_real_task: 2026-09-21 frontier-watch-daily — 3 cards to Market CoS (plugin deep-link, webhook wakes, formal-verify gate); held pending Friday steal-list + named yes
- last_file_or_issue_I_wrote: desk/census/frontier-watch.md
- last_time_I_paid_listed_or_posted: none

## Useful automations for MY lane
- read_from_repo: [VERIFIED.md, policy.yaml, desk/FLEET.md, desk/ROUTINES.md, desk/DECISIONS.md, desk/bots/FRONTIER-WATCH.md]
- write_to_repo: desk/census/frontier-watch.md
- proposed_routine: already live — 07:30 Asia/Ho_Chi_Minh weekdays frontier-watch-daily; stop = NONE if no methods; artifact = ≤7 cards to Market CoS (+ Fri 1–3 steal-list gated)
- do_not_automate: adopting steals; replying to watched accounts; arming other bots' routines; workplace-bot copies; sub-daily polling; buy/list/post/cap edits

## Commit
wrote `desk/census/frontier-watch.md`.
