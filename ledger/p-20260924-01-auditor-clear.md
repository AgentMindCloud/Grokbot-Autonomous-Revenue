# Auditor clear — p-20260924-01

status: CLEAR
ts: 2026-09-24T20:15+07:00
auditor: settlement-auditor
purchase_id: p-20260924-01
receipt_id: rc-20260924-01

## paid-row fields
- live_402: yes ($0.02 usdc base payee 0x2afb…Ad29 scheme exact)
- amount: 0.02 = settled_usd 0.02
- payee / chain / asset: match card + live_402
- idempotency_key: p-20260924-01-sku0-search (unique; do not reuse)
- tx: 0x126454b6fdbd9691bf62cc6b7578ceee72882024b8aaf5283818b025da933d71 (purchase = receipt)
- output_hash: e2b9c6a2514cba457f42ff34cf51424ad1ef69af71488ef80dc4d5a6b0c8a5ee · error_class null
- catalog_match.ok: true (not catalog-as-authority)
- governor: ALLOW · approval_id: human-d-20260924-06
- http_status: 200 · ok: true · results_count: 5 · mocked: false

## classification
lab_self_test: true — NOT revenue / NOT demand / NOT listing / NOT autopay

## flags
none. no freeze. no red. no retry.

result: CLEAR
