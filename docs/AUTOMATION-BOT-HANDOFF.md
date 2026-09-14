# Automation → Bot Handoff

Automations research. Loop Tester tests. Loop Auditor verifies evidence. Sink = GitHub LOOP-TEST issue in this repo.

There is no native Grok Automation → Grok Bot pipe. This contract is the pipe.

## Who writes tickets
Only **one** automation per day should open a Rank=1 issue:
- `Master-Synthesis-Daily` (primary)
- `Tool-Feedback-Loop-Daily` may open a ticket **only if** Master-Synthesis did not, and only for a skill-health experiment

All other dailies stay research-only. They must **not** open LOOP-TEST issues.

## Bots (cap = 2)
| Bot | When | Job |
|---|---|---|
| Loop Tester | 22:30 Asia/Ho_Chi_Minh | Run smallest test on `ready-to-test` |
| Loop Auditor | 23:00 Asia/Ho_Chi_Minh | Re-check Tester evidence. No new test. |

Desktop can be off. Routines run on the Bot cloud computer. Phone is for review.

## Bot routine — Loop Tester

```
Every day at 22:30 Asia/Ho_Chi_Minh, run the Loop Tester skill against AgentMindCloud/Grokbot-Autonomous-Revenue.
Search is:open label:loop-test label:ready-to-test.
Test only the newest Rank=1 ticket.
Write PASS / FAIL / BLOCKED + evidence on the issue.
Append analytics/loop-test-log.md.
Do not merge, post, pay, or change production without my approval.
If no READY ticket exists, say NONE and stop.
```

## Bot routine — Loop Auditor

```
Every day at 23:00 Asia/Ho_Chi_Minh, run the Loop Auditor skill against AgentMindCloud/Grokbot-Autonomous-Revenue.
Search is:open label:loop-test label:pass,fail,blocked -label:audited.
Re-run only the probes the Tester cited. Confirm or reject the result.
Do not open new issues. Do not post, pay, or deploy.
If none, say NONE and stop.
```

## Labels
- loop-test, ready-to-test, in-test, pass, fail, blocked
- audited — Auditor confirmed
- audit-fail — Tester result was wrong

## First human steps
1. Create Loop Tester. Paste skills/loop-tester.md + Tester routine.
2. Create Loop Auditor. Paste skills/loop-auditor.md + Auditor routine.
3. Keep specialist research automations from filing tickets.
