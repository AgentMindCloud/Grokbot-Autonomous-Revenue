# Grok Build 4.7 — finish the desk cutover

Repo: https://github.com/AgentMindCloud/Grokbot-Autonomous-Revenue
Branch: main. Commit each batch. Do not pay. Do not re-enable GitHub push trigger ledger-push-cos-note.

## A. Delete if still present
- entire 50-bot-system/
- contracts/planner-role.yaml (unless still referenced)
- creative/formats.md
- .github/ISSUE_TEMPLATE/loop-test.md
- phase0/hybrid-setup.md
Do not delete ledger/, policy.yaml, desk/, analytics/mcp-calls.jsonl, receipts, purchases.

## B. Canon already on main (do not revert)
VERIFIED.md three fronts, desk/FLEET.md, desk/FRONT.md, desk/jobs/IN.md, desk/HERMES.md, RANKED-PLAYBOOKS.md

## C. Fix stale lines
- desk/DECISIONS.md: allow demand-radar research; keep pay = named card only; listing still No
- desk/ROUTINES.md: Buyer pay tool EXISTS; inspect-only is lifted
- desk/AUTOMATIONS.md: mark ledger-push PAUSED, all task notify OFF
- desk/bots/LAB.md: remove inspect-only; require scorecard rc-20260924-01
- desk/bots/PROTOCOL-SCOUT.md: prefer fills_seen over listed price
- ledger/SCHEMA.md: add optional fills_seen to research rows

## D. Grok Bot profiles (human or Build pastes — do not CreateAgent)
Keep CoS recommend-with-score + NOTIFY only-CoS.
Keep Governor ALLOW/DENY.
Append MUTE footer to every specialist.
Park Money Maker / Agent Zero / X Growth.
Do not invent new bots.

## E. Scheduled tasks
Leave running with notification off:
frontier-cards-file, settlement-eod-file, protocol-research-file, sku0-health-mirror, market-desk-daily-rollup, poteto-scout-daily
Leave paused: ledger-push-cos-note
Optional pause: poteto-scout-galaxy-pulse (duplicate of daily)

## F. Hermes
Prompt in desk/HERMES.md. Path C:\\Users\\louis\\Documents\\Grokbot-Autonomous-Revenue

## G. Done when
- no 50-bot-system files on main
- VERIFIED mentions rc-20260924-01
- HUMAN.md must-list is the only human queue
- no task notifies on every commit
