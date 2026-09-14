# Automation → Bot Handoff

Automations research. The Loop Tester Bot tests. The sink is a GitHub LOOP-TEST issue in this repo.

There is no native Grok Automation → Grok Bot pipe. This contract is the pipe.

## Who writes tickets
Only **one** automation per day should open a Rank=1 issue:
- `Master-Synthesis-Daily` (primary)
- `Tool-Feedback-Loop-Daily` may open a ticket **only if** Master-Synthesis did not, and only for a skill-health experiment

All other dailies (Pricing, Market-Validation, API-Innovation, Competitive-Analysis, Simulations-Loops, Revenue-Models, AI Daily, Crypto_3H) stay research-only. They must **not** open LOOP-TEST issues.

## Append this block to Master-Synthesis-Daily (end of prompt)

```
HARD CONTRACT — last action every run:
1. Do not execute anything. Do not post to X. Do not change production.
2. Choose exactly ONE 48h experiment (Rank=1). If yesterday's LOOP-TEST issue is still open and READY/in-test, do not open a new one. Comment on the existing issue instead.
3. Create a GitHub issue in AgentMindCloud/Grokbot-Autonomous-Revenue using template .github/ISSUE_TEMPLATE/loop-test.md
   Title: LOOP-TEST: <method name>
   Labels: loop-test, ready-to-test
4. Fill every field. Smallest test must be ≤30 min and falsifiable.
5. Also write analytics/master-synthesis-YYYY-MM-DD.md as usual.
6. If GitHub issue create is unavailable, paste the full filled template in the run output under heading LOOP-TEST ISSUE BODY so a human or Bot can file it.
```

## Append this block to Tool-Feedback-Loop-Daily (end of prompt)

```
HARD CONTRACT:
Research + scoring only. Open a LOOP-TEST issue only if:
- Master-Synthesis has no open Rank=1 ticket today, AND
- the experiment is a skill-health probe (jsonl, latency, price, listing check) that can finish in 30 min.
Otherwise: update RANKED-PLAYBOOKS.md and analytics/tool-feedback-loop-YYYY-MM-DD.md only.
Never execute, post, pay, or deploy.
```

## Bot routine (paste into Loop Tester)

```
Every day at 22:30 Asia/Ho_Chi_Minh, run the Loop Tester skill against AgentMindCloud/Grokbot-Autonomous-Revenue.
Search is:open label:loop-test label:ready-to-test.
Test only the newest Rank=1 ticket.
Write PASS / FAIL / BLOCKED + evidence on the issue.
Append analytics/loop-test-log.md.
Do not merge, post, pay, or change production without my approval.
If no READY ticket exists, say NONE and stop.
Timezone: Asia/Ho_Chi_Minh.
```

## Labels
- loop-test — this contract
- ready-to-test — Bot may pick it up
- in-test — Bot started
- pass / fail / blocked — result

## First human steps
1. Create Grok Bot named Loop Tester. Paste skills/loop-tester.md as a saved skill.
2. Paste the routine block above.
3. Confirm SuperGrok Plus/Heavy or Cursor plan + Bot desktop app.
4. Apply the two automation prompt appends (or ask Grok chat to update those automations).
5. Keep specialist research automations unchanged except they must not file tickets.
