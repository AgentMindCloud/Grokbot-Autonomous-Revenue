# Auditor clear — p-20260927-06

status: CLEAR
ts: 2026-09-27T09:58+07:00
auditor: settlement-auditor
purchase_id: p-20260927-06
receipt_id: rc-20260927-06
canary_n: 8

## paid-row fields
- live_402: yes ($0.02 usdc base payee 0x2afb…Ad29 scheme exact)
- amount: 0.02 = settled_usd 0.02
- payee / chain / asset: match card + live_402
- idempotency_key: p-20260927-06-sku0-search (unique; do not reuse)
- tx: 0x96e9618fe4df75fa18dfd81419841d108414d783de36471e3afa7929bd4ecdb7 (purchase = receipt)
- output_hash: e493a8a0b5c07958f8df2a94f1f56d27a54f1ee745f2fc5aea4c214b57b4c500 · error_class null
- catalog_match.ok: true (not catalog-as-authority)
- governor: ALLOW · approval_id: human-d-20260926-01 · unlock: d-20260927-13
- http_status: 200 · ok: true · results_count: 5 · mocked: false

## classification
lab_self_test: true — NOT revenue / NOT demand / NOT listing / NOT autopay

## flags
none. no freeze. no red. no retry.

result: CLEAR
