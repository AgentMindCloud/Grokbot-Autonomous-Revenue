# Auditor clear — p-20260928-02

status: CLEAR
ts: 2026-09-28T20:57+07:00
auditor: settlement-auditor
purchase_id: p-20260928-02
receipt_id: rc-20260928-02
rail: external tick/symbols one-shot
sku: tick/symbols

## paid-row fields
- live_402: challenge object ($0.005 usdc base payee 0x29322…4f60 scheme exact; catalog_match.ok)
- amount: max_usd 0.005 = live_402.amount_usd 0.005 = settled_usd 0.005 (atomic 5000)
- payee / chain / asset: match card + live_402.payTo (base / USDC 0x833589…2913)
- idempotency_key: p-20260928-02-tick-symbols (unique; spent; do not reuse)
- tx: 0x31e539d34fa51d78cb3a48de9a3345961d0f7f0b6cbfa970ef8b9a96c4a26d46 (purchase = receipt)
- output_hash: 00c6194135596c97570e917360e5b73d7e804e702580dd60bd06af0598414973 · error_class null
- schema: id/paid/live_402{}/settled_usd present (SCHEMA.md parity)
- governor: ALLOW · approval_id: d-20260928-03 · unlock: d-20260928-05 · artifact: g-20260928-02-allow.md
- http_status: 200 · ok: true · results_count: 14 · mocked: false

## classification
lab_self_test: false · external_one_shot: true · standing_autopay: false
NOT densify sku0 · NOT listing · NOT autopay

## flags
none. no freeze. no red. no retry.

result: CLEAR
