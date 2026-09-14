# Skill: Loop Tester

**Owner Bot:** Loop Tester  
**When to use:** Daily routine, or when a new issue labeled `loop-test` + `ready-to-test` appears in AgentMindCloud/Grokbot-Autonomous-Revenue.

## Purpose
Turn one research ticket into a real PASS / FAIL / BLOCKED with evidence. Do not generate more research.

## Required inputs
- Repo: `AgentMindCloud/Grokbot-Autonomous-Revenue`
- Issue search: `is:open label:loop-test label:ready-to-test`
- Fallback if no issue: newest `analytics/master-synthesis-*.md` → section "48h experiment"
- Approval matrix: `50-bot-system/security/APPROVAL-MATRIX.md`

## Sequence
1. Pick **one** ticket. Prefer Rank=1, then oldest READY. Ignore drafts and tickets missing Pass/Fail criteria.
2. Comment `TEST START <ISO-8601>` and remove `ready-to-test` (add `in-test` if the label exists).
3. Run **only** the Smallest test. Cap 30 minutes. Prefer: HTTP probe, file exists, jsonl append, dry-run command, staging URL.
4. Write evidence on the issue (command, status code, snippet, file path). No novel theory.
5. Set result:
   - PASS → label `pass`. List the next human-gated step. Stop.
   - FAIL → label `fail`. One-line reason. Do not invent a replacement product.
   - BLOCKED → label `blocked`. Name the missing secret, login, or approval.
6. Append one line to `analytics/loop-test-log.md`:
   `YYYY-MM-DD | ISSUE# | PASS/FAIL/BLOCKED | 1-line evidence`
7. Stop. Do not open a second ticket the same run.

## Validate
- Evidence is reproducible (URL + status, or path + snippet).
- No production mutation happened.
- Only one experiment touched.

## Return
Short comment on the issue + the log line. If PASS and next step is human-gated, say exactly what the human must click/approve.

## Approvals (hard stop)
Never without explicit human yes in this conversation:
- Post to X
- Spend or move money / x402 live charge beyond a single self-probe if already approved in-repo
- Change DNS, Hostinger, production env, or merge to main
- Contact customers or create public listings

If the ticket asks for those, mark BLOCKED and quote the gate.

## Failure handling
- Repo or issue API down → report failure, do not use stale tickets.
- Ticket incomplete → comment what field is missing, leave OPEN, do not guess steps.
- Test would take >30 min → BLOCKED: scope too big. Ask human to shrink.
