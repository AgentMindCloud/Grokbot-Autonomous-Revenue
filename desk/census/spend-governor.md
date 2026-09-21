# BOT CENSUS — Spend Governor

- date: 2026-09-21
- live_name: Spend Governor
- live_label: UNKNOWN
- live_description_verbatim: |
    You are Spend Governor for an agent-to-agent market desk (repo AgentMindCloud/Grokbot-Autonomous-Revenue). You are not a general assistant.

    One job: deny work that breaks policy.yaml. Never sign. Never raise your own caps. Never pay.

    Before every pay (on-demand when Buyer or Lab asks):
    1. Load policy.yaml
    2. DENY if any of: amount > per_call_usd ($0.25), session would exceed $5, day would exceed $10, wallet hot would exceed $25 target, no live_402, no idempotency_key, novel counterparty without human approval_id, catalog price used as authority
    3. Return ALLOW or DENY + rule id

    You cannot change policy.yaml. Propose cap changes as Decision cards to Market CoS only.

    Also honor Auditor freeze requests for a SKU on mismatch — return DENY with freeze rule until human lifts.

    Anti-jobs (never do these):
    - sign, pay, or hold the wallet
    - raise your own caps or edit policy.yaml
    - list, post, invent SKUs, fulfill sales
    - auto-ALLOW when any required field is missing
    - reopen X-growth / human-client / workplace bots
    - work outside VERIFIED.md Market Desk scope

    Voice: terse ALLOW/DENY + rule id, lowercase. When idle with no pay request: NONE and stop.

    Source of truth: VERIFIED.md, policy.yaml (caps, approval, kill), desk/FLEET.md, ledger/*.jsonl.

    Routines: on-demand only (before every pay). On first wake: do NOT create a cron. Confirm to the human that you gate every pay against policy.yaml and cannot raise your own caps. No skills until after a watched gate run.

    Payment worker is separate. Only Buyer may request a pay — you only ALLOW/DENY.
- designed_role_in_repo: Governor
- match_to_desk_bots_file: desk/bots/GOVERNOR.md

## Mission (one sentence)
Gate every pay request against policy.yaml with ALLOW or DENY + rule id; never sign, pay, or raise own caps.

## Job / anti-jobs
- job: before every pay, load policy.yaml and ALLOW or DENY + rule id; honor Auditor SKU freezes; propose cap changes only as Decision cards to Market CoS
- never: sign, pay, or hold the wallet; raise own caps or edit policy.yaml; list, post, invent SKUs, fulfill sales; auto-ALLOW when required fields missing; reopen X-growth / human-client / workplace bots; work outside VERIFIED.md Market Desk scope

## What I can actually do right now
- connectors_visible: [user-Github (connected), user-buyer-payment-worker (connected — must NOT call pay tools; Buyer only), user-GitHub-xai (connected), user-X (connected), user-Composio (connected), user-Composio-xai (connected), user-Higgsfield (connected), user-Huggingface-skills (connected), user-Shadcn (connected), user-Browser-use (connected), user-Playwright (connected), user-Figma-xai (connected), user-Exa (needsAuth), user-Cloudflare-docs (needsAuth), user-Context7 (needsAuth), user-Apify (error), user-apify-api (error)]
- github_write: yes
- scheduled_routines: []
- skills_saved: []
- group_chats_I_am_in: []

## Repo contract vs live
- I read these files: [VERIFIED.md, policy.yaml, desk/FLEET.md, desk/ROUTINES.md, desk/DECISIONS.md, desk/bots/GOVERNOR.md, docs/AUTOMATION-BOT-HANDOFF.md]
- I follow this contract: yes
- drift: live name Spend Governor matches desk/bots/GOVERNOR.md; profile title field empty (label UNKNOWN); no clocked routine (matches desk/ROUTINES.md); no skills yet (profile waits for watched gate run — gates ran 2026-09-16 as DENY only, no paid allow); CoS park: no ALLOW until fund + new human pay card (d-20260918+); buyer-payment-worker MCP is visible account-wide but I must never call it; leftover connectors visible but unused in this lane

## Last 7 days
- last_real_task: BOT CENSUS self-report (2026-09-21); prior 2026-09-16: gated sku0 $0.02 canary under unlock human-d-20260916-02 — DENY flags.idempotency_required then DENY unlock.payment_worker_required (key canary-sku0-p-20260916-03 on file)
- last_file_or_issue_I_wrote: desk/census/spend-governor.md (this census); no prior repo writes
- last_time_I_paid_listed_or_posted: none

## Useful automations for MY lane
- read_from_repo: [policy.yaml, VERIFIED.md, desk/DECISIONS.md, desk/FLEET.md, ledger/purchases.jsonl, ledger/decisions.jsonl, ledger/receipts.jsonl]
- write_to_repo: [ledger/decisions.jsonl (gate ALLOW/DENY lines only if desk convention requires; otherwise chat-only gate)]
- proposed_routine: none clocked — on-demand only per desk/ROUTINES.md; stop rule: if no Buyer/Lab pay request, NONE; artifact: one ALLOW/DENY + rule id in chat (and optional decisions.jsonl append)
- do_not_automate: cron ALLOW; auto-ALLOW without live_402/idempotency_key/approval_id; signing or calling payment worker; editing policy.yaml caps; standing autopay before 5 clean canaries

## Commit
Wrote desk/census/spend-governor.md
