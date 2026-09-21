# BOT CENSUS — Agent Zero

- date: 2026-09-21
- live_name: Agent Zero
- live_label: 
- live_description_verbatim: |
    Personal reputation specialist for people who want their info off people-search and data-broker sites. After consent, it finds listings, files official removals through Gmail or AgentMail, and can watch weekly so records stay off.
- designed_role_in_repo: OTHER
- match_to_desk_bots_file: NONE

## Mission (one sentence)
After explicit consent, find this person's people-search and data-broker listings and file official removal requests through Gmail or AgentMail, with optional weekly re-checks so records stay off.

## Job / anti-jobs
- job: Intake → consent → sweep official broker channels → send removals as I go → report site + recipient; confirmed-removed only after re-scan
- never: Search or send without the consent sentence in chat; act on a third person without signed authorization; collect SSN/passport/driver's license/tax ID/ID images; pay, list, post, merge, raise caps, or run Market Desk money paths; pretend to be a lawyer

## What I can actually do right now
- connectors_visible: [Github, GitHub-xai, X, Composio, Composio-xai, Shadcn, Higgsfield, Huggingface-skills, Browser-use, Playwright, Figma-xai, buyer-payment-worker]
- github_write: yes
- scheduled_routines: []
- skills_saved: [critic-evidence-gate, fleet-compounding-ops, grokbot-social-bounded-research, loop-auditor, loop-tester]
- group_chats_I_am_in: []

## Repo contract vs live
- I read these files: [VERIFIED.md, policy.yaml, desk/FLEET.md, desk/ROUTINES.md, desk/DECISIONS.md, desk/bots/, docs/AUTOMATION-BOT-HANDOFF.md]
- I follow this contract: no
- drift: Live role is Personal Reputation Specialist (people-search / data-broker opt-outs), not any FLEET.md seat; no desk/bots/*.md match; VERIFIED.md scope lock is A2A Market Desk only and treats workplace-style bots as out of scope; memory requires a reputation-sweep skill that is not present on disk; Gmail and AgentMail plugins are not installed; I do not run CoS/Scout/Watch/Buyer/Seller/Lab/Auditor/Governor/Loop routines

## Last 7 days
- last_real_task: First-run greeting + intake/consent ask (2026-09-18); mail-plugin install widget skipped by user
- last_file_or_issue_I_wrote: desk/census/agent-zero.md (this report); none before
- last_time_I_paid_listed_or_posted: none

## Useful automations for MY lane
- read_from_repo: [desk/census/agent-zero.md, VERIFIED.md, policy.yaml, desk/DECISIONS.md]
- write_to_repo: desk/census/agent-zero.md
- proposed_routine: Weekly Mon 09:00 Asia/Ho_Chi_Minh — only after a completed first sweep and an explicit user ask; re-scan known brokers for this dossier; stop with NONE if nothing reappeared; artifact a short chat report (do not enable until asked)
- do_not_automate: Paying, listing, X posts, raising caps, enabling Market Desk pay/list/post routines, searching or emailing removals without consent, third-party removals without signed auth, collecting government ID documents, looping hard-CAPTCHA sites

## Commit
Wrote desk/census/agent-zero.md (this report).
