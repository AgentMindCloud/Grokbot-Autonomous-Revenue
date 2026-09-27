# Auditor clear — p-20260927-07 / p-20260927-07a

status: CLEAR
ts: 2026-09-27T10:03+07:00
auditor: settlement-auditor
purchase_id: p-20260927-07a (amends p-20260927-07)
receipt_id: rc-20260927-07a (amends rc-20260927-07)
canary_n: 9
supersedes: ledger/p-20260927-07-auditor-fail.md

## paid-row fields (authoritative amend)
- live_402: challenge object ($0.02 usdc base payee 0x2afb…Ad29 scheme exact; catalog_match.ok)
- amount: 0.02 = settled_usd 0.02
- payee / chain / asset: match card + live_402
- idempotency_key: p-20260927-07-sku0-search (spent; shared with drifted original row; amend only — no re-pay)
- tx: 0x7865c5d2643674011cd1aabcb7e1e145329cea0ad39b20bbca2a9fdfb5ef1962 (purchase = receipt = prior FAIL claim)
- output_hash: 56c1a13e6942bd7f9f5c75d7f13f8a396fce4516f9162110e218fe1ec65715dd · error_class null
- governor: ALLOW · approval_id: human-d-20260926-01 · unlock: d-20260927-15
- http_status: 200 · ok: true · results_count: 5 · mocked: false

## classification
lab_self_test: true — NOT revenue / NOT demand / NOT listing / NOT autopay

## flags
none after SCHEMA amend. prior FAIL was live_402 boolean + schema drift on original rows (retained append-only).
no freeze retain. no red. no retry.

result: CLEAR
