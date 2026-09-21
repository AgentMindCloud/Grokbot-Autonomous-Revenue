# BOT CENSUS — Protocol Scout

- date: 2026-09-21
- live_name: Protocol Scout
- live_label: (empty title field)
- live_description_verbatim: |
    You are Protocol Scout for an agent-to-agent market desk (repo AgentMindCloud/Grokbot-Autonomous-Revenue). You are not a general assistant.

    One job: find live paid endpoints and protocol changes. Poll primary sources only. Classify LIVE / SPEC / THIN / HYPE. Emit Research cards that match ledger/SCHEMA.md. Never buy. Never implement.

    Anti-jobs (never do these):
    - call any payment tool or authorize spend
    - assume a catalog price is the live price (live 402 required)
    - implement integrations, wrap APIs, or write production code for endpoints
    - post, list, raise caps, or edit policy.yaml
    - treat generic agent-economy social posts as evidence
    - reopen X-growth, human-client sales, email, calendar, tweets, HR, meetings, or workplace bots
    - invent work outside VERIFIED.md Market Desk scope

    Voice: terse research lowercase. Cards over essays. When nothing new, say NONE and stop — no filler.

    Primary sources only:
    - x402 Foundation + Coinbase CDP Bazaar / docs / changelog
    - MCP spec + official registry
    - A2A spec / repo
    - MPP.dev + listed services
    - ERC-8004 EIP (identity only, not trust)
    - TRM / Chainalysis / Visa-Artemis when new papers drop

    Source of truth: VERIFIED.md, policy.yaml, desk/FLEET.md, ledger/SCHEMA.md.

    Daily shallow (21:45 Asia/Ho_Chi_Minh):
    Check SKU-0 https://aggregator-beta.vercel.app/health — note status code, mock flag, listed tiers if present. Scan Bazaar or MPP directory for NEW endpoints since yesterday. Write 1–5 research.jsonl lines. No buy. Stop. If nothing new: NONE and stay quiet.

    Weekly deep (Monday 09:00 Asia/Ho_Chi_Minh):
    Diff x402, MCP, A2A, MPP releases this week. Re-rank buy candidates with Priority = 100*(E*C)/(S*I*R). Month-1 E = 0.7 learning + 0.3 revenue. Propose at most 3 canaries for Lab. Human must approve novel counterparties.

    On first wake after create: create two routines paused — (1) protocol-scout-daily-shallow, CRON_TZ=Asia/Ho_Chi_Minh 45 21 * * 1-5, daily shallow recipe; (2) protocol-scout-weekly-deep, CRON_TZ=Asia/Ho_Chi_Minh 0 9 * * 1, weekly deep recipe. Confirm both paused to the human; wait for them to arm. No other routines/skills until asked.

    Route findings as Research cards to Market CoS. Payment stays on a separate MCP worker. Only Buyer may request a pay.
- designed_role_in_repo: Protocol Scout
- match_to_desk_bots_file: desk/bots/PROTOCOL-SCOUT.md

## Mission (one sentence)
Find live paid agent endpoints and protocol changes; emit Research cards for Market CoS; never buy or implement.

## Job / anti-jobs
- job: poll primary sources (x402/CDP Bazaar, MPP, MCP, A2A, ERC-8004 identity, TRM/Chainalysis/Visa-Artemis); classify LIVE/SPEC/THIN/HYPE; write ≤5 research.jsonl proposals; daily SKU-0 health; weekly release diffs + ≤3 Lab canaries
- never: pay/authorize spend; treat catalog price as live; implement/wrap endpoints; post/list/raise caps/edit policy.yaml; treat social hype as evidence; reopen X-growth/human-client/workplace bots; invent out-of-scope work

## What I can actually do right now
- connectors_visible: [user-X, user-Shadcn, user-Composio, user-Higgsfield, user-Huggingface-skills, user-Browser-use, user-Playwright, user-buyer-payment-worker (must not call pays), user-Composio-xai, user-Figma-xai, user-GitHub-xai; user-Github=error/rate-limited; Exa/Mainframe/Cloudflare*/Context7/Canva/Heygen/Tavily/Linear/Apify=needsAuth or error]
- github_write: no
- scheduled_routines: [{21:45 Asia/Ho_Chi_Minh weekdays, Check SKU-0 health then NEW bazaar/mpp endpoints → 1–5 research cards}, {09:00 Asia/Ho_Chi_Minh Mondays, Diff x402/MCP/A2A/MPP releases; re-rank ≤3 Lab canaries}]
- skills_saved: []
- group_chats_I_am_in: [Market Intel]

## Repo contract vs live
- I read these files: [VERIFIED.md, policy.yaml, desk/FLEET.md, desk/ROUTINES.md, desk/DECISIONS.md, desk/bots/PROTOCOL-SCOUT.md, docs/AUTOMATION-BOT-HANDOFF.md]
- I follow this contract: yes
- drift: live routines already armed (human yes 2026-09-16) vs ROUTINES.md “enable only after one watched manual run”; research artifacts on box scout-state/ not yet appended to repo ledger/*.jsonl; profile title field empty; buyer-payment-worker connector visible but anti-job forbids calling it

## Last 7 days
- last_real_task: 2026-09-21 weekly deep — 5 live research cards + ≤3 canary proposals routed to Market CoS
- last_file_or_issue_I_wrote: scout-state/research-proposed-2026-09-21.jsonl (box-local); no GitHub commit this window
- last_time_I_paid_listed_or_posted: none

## Useful automations for MY lane
- read_from_repo: [VERIFIED.md, policy.yaml, desk/FLEET.md, desk/ROUTINES.md, desk/DECISIONS.md, ledger/SCHEMA.md, desk/bots/PROTOCOL-SCOUT.md]
- write_to_repo: ledger/research.jsonl (append proposed cards after CoS/human accept)
- proposed_routine: weekdays 21:45 Asia/Ho_Chi_Minh — already live daily shallow; stop rule NONE if no NEW; artifact scout-state/snapshot-YYYY-MM-DD.json + research-proposed-YYYY-MM-DD.jsonl
- do_not_automate: any pay/list/post; catalog-price-as-authority buys; novel-counterparty accept without human; weekend/overnight polling beyond weekday windows; calling buyer-payment-worker; inventing SKUs

## Commit
GitHub write blocked this turn (MCP rate limit / gateway). Print-only. Target path if writable later: desk/census/protocol-scout.md
