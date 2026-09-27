# Auditor clear — p-20260927-01

status: CLEAR
ts: 2026-09-27T09:40+07:00
auditor: settlement-auditor
purchase_id: p-20260927-01
receipt_id: rc-20260927-01
canary_n: 3

## paid-row fields
- live_402: yes ($0.02 usdc base payee 0x2afb…Ad29 scheme exact)
- amount: 0.02 = settled_usd 0.02
- payee / chain / asset: match card + live_402
- idempotency_key: p-20260927-01-sku0-search (unique; do not reuse)
- tx: 0xf6414a2248a1d5f0950b556ebbc8f8dac5789bcf7e43d6a2b3e795406f98ff48 (purchase = receipt)
- output_hash: ee88553f26fe49b51fb079d5fd0a021c6891e8afe30ba52c8330999072e15c45 · error_class null
- catalog_match.ok: true (not catalog-as-authority)
- governor: ALLOW · approval_id: human-d-20260926-01 · unlock: d-20260927-02
- http_status: 200 · ok: true · results_count: 5 · mocked: false

## classification
lab_self_test: true — NOT revenue / NOT demand / NOT listing / NOT autopay

## flags
none. no freeze. no red. no retry.

result: CLEAR
