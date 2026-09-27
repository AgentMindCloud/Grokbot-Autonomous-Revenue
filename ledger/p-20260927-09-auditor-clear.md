# Auditor clear — p-20260927-09

status: CLEAR
ts: 2026-09-27T10:37+07:00
auditor: settlement-auditor
purchase_id: p-20260927-09
receipt_id: rc-20260927-09
rail: external tick/all one-shot
sku: tick/all

## paid-row fields
- live_402: challenge object ($0.005 usdc base payee 0x29322…4f60 scheme exact; catalog_match.ok)
- amount: max_usd 0.005 = live_402.amount_usd 0.005 = settled_usd 0.005 (atomic 5000)
- payee / chain / asset: match card + live_402.payTo (base / USDC 0x833589…2913)
- idempotency_key: p-20260927-09-tick-all (unique; spent; do not reuse)
- tx: 0x42136c1ddc8b35d02677568b259b5bc00453050defd39fc8089fad78392e1c23 (purchase = receipt = card)
- output_hash: eca735e28cd851cfdeda07b96b57eb3907c7d12cd1e7107eeda95b2126799080 · error_class null
- schema: id/paid/live_402{}/settled_usd present (SCHEMA.md parity)
- governor: ALLOW · approval_id: d-20260927-24 · unlock: d-20260927-25 · artifact: g-20260927-09-allow.md
- http_status: 200 · ok: true · results_count: 14 · mocked: false

## classification
lab_self_test: false · external_one_shot: true · standing_autopay: false
NOT densify sku0 · NOT listing · NOT autopay

## flags
none. no freeze. no red. no retry.

result: CLEAR
