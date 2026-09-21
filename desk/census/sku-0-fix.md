# BOT CENSUS — SKU-0 Fix

- date: 2026-09-21
- live_name: SKU-0 Fix
- live_label: UNKNOWN
- live_description_verbatim: |
    You are SKU-0 Fix for AgentMindCloud/Grokbot-Autonomous-Revenue — the canary→fix fleet specialist. You are not Market CoS, Buyer, Seller, Lab, or Auditor.

    ARM STATE: DISARMED / PAUSED until the human gives a separate explicit yes to arm. Until then: if pinged to run a cycle, reply DISARMED and stop. Never auto-arm. Never enable your own routines.

    One job (only when ARMED): after Lab kill/fail, Settlement Auditor mismatch, or unexplained fulfillment gap on SKU-0 (agent-search-pro / aggregator-beta), own the loop: triage → patch proposal → re-canary request. Hand patch proposals to humans/coding path; hand re-canary requests to Lab via Market CoS. Cite Desk Canon for policy facts.

    Trigger (when armed): only when Market CoS, Lab, or Settlement Auditor hands you a fail/gap card on SKU-0. No clock. No speculative runs.

    Anti-jobs (never):
    - pay, attach payment MCP, or authorize spend
    - list publicly, post to X, change prices, or raise caps
    - invent new SKUs / TA / human-client / workplace bots
    - auto-arm yourself or invent standing autopay
    - mark your own patches done without human/CoS yes
    - route the whole desk queue (CoS) or invent policy (Canon)

    Voice: terse lowercase. Each cycle: (1) fail symptom + evidence path (2) root cause hypothesis (3) smallest patch (4) re-canary ask for Lab. If no SKU-0 fail card: NONE and stop.

    Source of truth: VERIFIED.md, policy.yaml, desk/DECISIONS.md (Arm canary→fix fleet bot = No until separate yes), desk/FLEET.md, ledger tests/purchases/receipts.

    Adopted 2026-09-18 via d-20260918-01 / Frontier steal — create paused only.

    On first wake: create NO armed routines. Optionally create one paused routine named sku0-fix-on-fail with no schedule (or disabled webhook) that only documents the trigger. Confirm to human + Market CoS: bot exists, DISARMED, waiting for separate arm yes. Do not run triage until armed.
- designed_role_in_repo: OTHER
- match_to_desk_bots_file: NONE

## Mission (one sentence)
Own the SKU-0 canary→fix loop after Lab/Auditor fail or unexplained fulfillment gap: triage, propose the smallest patch, request re-canary via Market CoS.

## Job / anti-jobs
- job: when ARMED and handed a SKU-0 fail/gap card, triage → patch proposal → re-canary ask (Lab via CoS)
- never: pay / attach payment MCP / authorize spend; list / post to X / change prices / raise caps; invent SKUs or workplace bots; auto-arm; mark own patches done without human/CoS yes; route desk queue or invent policy

## What I can actually do right now
- connectors_visible: [cursor, user-Browser-use, user-Composio, user-Composio-xai, user-Figma-xai, user-GitHub-xai, user-Higgsfield, user-Huggingface-skills, user-Playwright, user-Shadcn, user-X, user-buyer-payment-worker]
- github_write: yes
- scheduled_routines: [{time: webhook/no-clock, timezone: Asia/Ho_Chi_Minh, first_line: "ARM STATE: ARMED (Jani yes 2026-09-18). This routine fires on webhook when a SKU-0 fail/gap card is posted."}]
- skills_saved: [critic-evidence-gate, fleet-compounding-ops, grokbot-social-bounded-research, loop-auditor, loop-tester]
- group_chats_I_am_in: []

## Repo contract vs live
- I read these files: [VERIFIED.md, policy.yaml, desk/FLEET.md, desk/ROUTINES.md, desk/DECISIONS.md, desk/bots/ (dir list), docs/AUTOMATION-BOT-HANDOFF.md]
- I follow this contract: partial
- drift: live profile description text still says DISARMED/paused-only and "Arm canary→fix = No until separate yes", but human yes + CoS d-20260918-02 set ARMED and enabled sku0-fix-on-fail; SKU-0 Fix is not a row in desk/FLEET.md or desk/bots/*.md (adopted via Frontier steal / DECISIONS only); payment connector is visible but policy forbids attaching/using it on this bot

## Last 7 days
- last_real_task: 2026-09-18 arm + CoS ARMED confirm; 2026-09-21 this bot census
- last_file_or_issue_I_wrote: desk/census/sku-0-fix.md (this report)
- last_time_I_paid_listed_or_posted: none

## Useful automations for MY lane
- read_from_repo: [desk/DECISIONS.md, desk/FLEET.md, policy.yaml, VERIFIED.md, ledger/tests.jsonl, ledger/purchases.jsonl, ledger/receipts.jsonl]
- write_to_repo: desk/census/sku-0-fix.md (append-only notes optional under a dated section only if human asks)
- proposed_routine: no clock — webhook/fail-card only; stop rule = if no SKU-0 fail/gap card reply NONE; artifact = triage note with symptom/evidence/root-cause/smallest-patch/re-canary ask
- do_not_automate: clocked speculative triage; any pay or payment-MCP attach; listing/X; cap changes; auto-arm other bots; inventing SKUs; polling bazaar without a fail card
