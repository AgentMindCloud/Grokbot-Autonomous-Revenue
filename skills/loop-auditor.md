# Skill: Loop Auditor

**Owner Bot:** Loop Auditor  
**When to use:** Daily after Loop Tester, or when an issue is labeled `loop-test` plus `pass` / `fail` / `blocked` and has no `audited` label.

## Purpose
Check that Loop Tester's result is true. Do not invent a new experiment. Do not re-run a different test.

## Required inputs
- Repo: `AgentMindCloud/Grokbot-Autonomous-Revenue`
- Issue search: `is:open label:loop-test label:pass,fail,blocked -label:audited`
- Fallback: newest comment on the latest `loop-test` issue from today
- Tester skill contract: `skills/loop-tester.md`

## Sequence
1. Pick the newest unaudited result. One issue per run.
2. Comment `AUDIT START <ISO-8601>`.
3. Re-do **only** the probes the Tester claimed (same URLs/commands). Cap 15 minutes.
4. Compare:
   - Did status codes match the comment?
   - Was the smallest-test scope respected (<30 min, no production mutation)?
   - Did labels match the evidence (`pass` only if pass criteria were met)?
   - Did they stop at human gates (no X/pay/DNS/merge)?
5. Verdict:
   - CONFIRMED → add label `audited`. One-line agreement.
   - REJECTED → remove `pass`/`fail`/`blocked` if wrong; add `ready-to-test` only if the original smallest test was never actually run. Add `audit-fail`. State which claim was false.
   - BLOCKED → cannot reproduce (auth, outage). Leave Tester labels. Say why.
6. Append `analytics/loop-test-log.md`:
   `YYYY-MM-DD | ISSUE# | AUDIT CONFIRMED/REJECTED/BLOCKED | 1-line`
7. Stop. Never open a new LOOP-TEST issue. Never post, pay, or deploy.

## Validate
- You touched only evidence the Tester already cited, plus label hygiene.
- You did not expand scope (no extra products, no TA rebuild, no second experiment).

## Approvals (hard stop)
Same as Loop Tester. Auditor has **no** extra privileges.

## Failure handling
- No unaudited result → reply NONE and stop.
- Tester comment missing evidence → REJECTED, send back to `ready-to-test`.
