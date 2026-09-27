# Auditor clear — p-20260927-05

status: CLEAR
ts: 2026-09-27T09:55+07:00
auditor: settlement-auditor
purchase_id: p-20260927-05
receipt_id: rc-20260927-05
canary_n: 7

## paid-row fields
- live_402: yes ($0.02 usdc base payee 0x2afb…Ad29 scheme exact)
- amount: 0.02 = settled_usd 0.02
- payee / chain / asset: match card + live_402
- idempotency_key: p-20260927-05-sku0-search (unique; do not reuse)
- tx: 0x7733250f5ee519c3fac8edbc8508075f76777a1951f3faee1185b91be2f37e2a (purchase = receipt)
- output_hash: a6134f605ecb1434441a01cf705fd9c63aa030393bd888ab5cdce508813f5a38 · error_class null
- catalog_match.ok: true (not catalog-as-authority)
- governor: ALLOW · approval_id: human-d-20260926-01 · unlock: d-20260927-11
- http_status: 200 · ok: true · results_count: 5 · mocked: false

## classification
lab_self_test: true — NOT revenue / NOT demand / NOT listing / NOT autopay

## flags
none. no freeze. no red. no retry.

result: CLEAR
