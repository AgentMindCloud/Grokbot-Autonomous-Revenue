# BOT CENSUS — dr eggbot

- date: 2026-09-21
- live_name: dr eggbot
- live_label: (none / empty title)
- live_description_verbatim: |
    Designs high-quality Grok Bots. Asks a few preference questions, then creates them with CreateAgent. Coding bots get the poteto-mode bar (one job, unslopped, verified). Non-coding bots get the same tightness: one job, one voice, explicit anti-jobs, no leftover tools. Casual, a little mad-scientist, short lowercase. Bias to act once the job is clear. Does not default to shareable templates.
- designed_role_in_repo: dr eggbot
- match_to_desk_bots_file: NONE (role named in desk/FLEET.md only; no desk/bots/DR-EGGBOT.md)

## Mission (one sentence)
Design and repair Market Desk Grok Bots, then run a weekly fleet routine healthcheck — never pay, list, or run lab.

## Job / anti-jobs
- job: Design/repair desk bots (CreateAgent/UpdateAgent); weekly routine waste + light transcript friction audit; wire buyer_payment_worker when human-authorized
- never: pay; list; post; run lab; raise caps; merge without approval; enable other bots' routines without human yes; contact people outside the fleet unless asked

## What I can actually do right now
- connectors_visible: [X, Shadcn, Composio, Higgsfield, Huggingface-skills, Browser-use, Playwright, buyer-payment-worker (Buyer-only instructions), Composio-xai, Figma-xai, GitHub-xai; Github plugin error; Apify error; several needsAuth]
- github_write: yes
- scheduled_routines: [{time: "08:49 Mondays", timezone: "Asia/Saigon (CRON_TZ=Asia/Saigon 49 8 * * 1)", first_line: "Weekly Market Desk + fleet healthcheck (Mondays)."}, {time: "08:44 weekdays PAUSED", timezone: "Asia/Saigon (CRON_TZ=Asia/Saigon 44 8 * * 1-5)", first_line: "transcript-healthcheck (paused; weekly-only mode)"}]
- skills_saved: [critic-evidence-gate, fleet-compounding-ops, grokbot-social-bounded-research, loop-auditor, loop-tester, plus pstack plugin skills, plus Cursor managed skills]
- group_chats_I_am_in: []

## Repo contract vs live
- I read these files: [VERIFIED.md, policy.yaml, desk/FLEET.md, desk/ROUTINES.md, desk/DECISIONS.md, docs/AUTOMATION-BOT-HANDOFF.md, desk/bots/ listing]
- I follow this contract: partial
- drift: Live profile is generic bot-designer; FLEET pins weekly healthcheck + design/repair and forbids pay/list/run lab (observed). Live also attached buyer-payment-worker account-wide (gated Buyer-only by instructions) and created SKU-0 Fix / Desk Canon / market desk bots — within designer lane. Did not invent a Market Desk operator role for myself.

## Last 7 days
- last_real_task: 2026-09-21 weekly-healthcheck parent relay (Seller Desk weekend cron flag); prior 2026-09-18 payment-worker rebind + hot wallet; 2026-09-18 SKU-0 Fix create/arm notes
- last_file_or_issue_I_wrote: desk/census/dr-eggbot.md (this census); local connector-secrets/buyer-x402-hot.json (private key file on box, not repo)
- last_time_I_paid_listed_or_posted: none

## Useful automations for MY lane
- read_from_repo: [desk/FLEET.md, desk/DECISIONS.md, desk/ROUTINES.md, desk/bots/*.md, policy.yaml, VERIFIED.md, ledger/*.jsonl]
- write_to_repo: [desk/census/dr-eggbot.md]
- proposed_routine: Monday 08:49 Asia/Ho_Chi_Minh weekly-healthcheck — stop/quiet when no waste or friction; artifact = short proposal list to human only
- do_not_automate: auto-attaching payment MCP; enabling desk routines without yes; CreateAgent fan-out; any pay/list/post; running Lab; weekday transcript-healthcheck (intentionally paused)

## Commit
Written to desk/census/dr-eggbot.md