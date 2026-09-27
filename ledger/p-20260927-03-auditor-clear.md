# Auditor clear — p-20260927-03

status: CLEAR
ts: 2026-09-27T09:48+07:00
auditor: settlement-auditor
purchase_id: p-20260927-03
receipt_id: rc-20260927-03
canary_n: 5

## paid-row fields
- live_402: yes ($0.02 usdc base payee 0x2afb…Ad29 scheme exact)
- amount: 0.02 = settled_usd 0.02
- payee / chain / asset: match card + live_402
- idempotency_key: p-20260927-03-sku0-search (unique; do not reuse)
- tx: 0x58ba9ee0b3088a0ac42dba481ea3a3b2c1167ce1facb1db2c8d0b3e77f9c9778 (purchase = receipt)
- output_hash: dfb553fcd072f2f6e974348b610b2fe2fb6ab6035a5fb24fb54a858b9d6e8654 · error_class null
- catalog_match.ok: true (not catalog-as-authority)
- governor: ALLOW · approval_id: human-d-20260926-01 · unlock: d-20260927-07
- http_status: 200 · ok: true · results_count: 5 · mocked: false

## classification
lab_self_test: true — NOT revenue / NOT demand / NOT listing / NOT autopay

## flags
none. no freeze. no red. no retry.

result: CLEAR
