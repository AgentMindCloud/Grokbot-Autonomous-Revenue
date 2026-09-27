# Auditor clear — p-20260927-04

status: CLEAR
ts: 2026-09-27T09:52+07:00
auditor: settlement-auditor
purchase_id: p-20260927-04
receipt_id: rc-20260927-04
canary_n: 6

## paid-row fields
- live_402: yes ($0.02 usdc base payee 0x2afb…Ad29 scheme exact)
- amount: 0.02 = settled_usd 0.02
- payee / chain / asset: match card + live_402
- idempotency_key: p-20260927-04-sku0-search (unique; do not reuse)
- tx: 0x0b4d2fb755d8903ab19a38e248766983322c0e28deec1db8e82b05ed83e212b4 (purchase = receipt)
- output_hash: 5c09059d0c678e1ea66c26694eb7584f77df1fcc1c22cd2fdbc23a2c455b99b6 · error_class null
- catalog_match.ok: true (not catalog-as-authority)
- governor: ALLOW · approval_id: human-d-20260926-01 · unlock: d-20260927-09
- http_status: 200 · ok: true · results_count: 5 · mocked: false

## classification
lab_self_test: true — NOT revenue / NOT demand / NOT listing / NOT autopay

## flags
none. no freeze. no red. no retry.

result: CLEAR
