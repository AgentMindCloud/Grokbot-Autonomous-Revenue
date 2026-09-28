# Auditor clear — p-20260928-01

status: CLEAR
ts: 2026-09-28T20:57+07:00
auditor: settlement-auditor
purchase_id: p-20260928-01
receipt_id: rc-20260928-01
rail: external tick/latest one-shot
sku: tick/latest

## paid-row fields
- live_402: challenge object ($0.005 usdc base payee 0x29322…4f60 scheme exact; catalog_match.ok)
- amount: max_usd 0.005 = live_402.amount_usd 0.005 = settled_usd 0.005 (atomic 5000)
- payee / chain / asset: match card + live_402.payTo (base / USDC 0x833589…2913)
- idempotency_key: p-20260928-01-tick-latest (unique; spent; do not reuse)
- tx: 0x34bafe23879144057f00cb799448f12442f039cd3f98b26e1f864fff195c7bb3 (purchase = receipt)
- output_hash: c982f1184fe0d9df52e8ad4c975051a73121a716f259319673bb1bb073cfe00f · error_class null
- schema: id/paid/live_402{}/settled_usd present (SCHEMA.md parity)
- governor: ALLOW · approval_id: d-20260928-02 · unlock: d-20260928-04 · artifact: g-20260928-01-allow.md
- http_status: 200 · ok: true · results_count: 1 · mocked: false

## classification
lab_self_test: false · external_one_shot: true · standing_autopay: false
NOT densify sku0 · NOT listing · NOT autopay

## flags
none. no freeze. no red. no retry.

result: CLEAR
