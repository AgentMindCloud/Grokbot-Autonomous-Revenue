# Auditor clear — p-20260926-01

status: CLEAR
ts: 2026-09-26T13:55+07:00
auditor: settlement-auditor
purchase_id: p-20260926-01
receipt_id: rc-20260926-01

## paid-row fields
- live_402: yes ($0.02 usdc base payee 0x2afb…Ad29 scheme exact)
- amount: 0.02 = settled_usd 0.02
- payee / chain / asset: match card + live_402
- idempotency_key: p-20260926-01-sku0-search (unique; do not reuse)
- tx: 0xb56b5679d75fcf74d97246d82e43c5f9478fc10bf0edeb070fef2dbaf1dc66d2 (purchase = receipt)
- output_hash: de4e72cd3ca8c1e137c0600d76797160f0c1693c63f312646bad7ee363a12a10 · error_class null
- catalog_match.ok: true (not catalog-as-authority)
- governor: ALLOW · approval_id: human-d-20260926-01 · unlock: d-20260926-02
- http_status: 200 · ok: true · results_count: 5 · mocked: false

## classification
lab_self_test: true — NOT revenue / NOT demand / NOT listing / NOT autopay

## flags
none. no freeze. no red. no retry.

result: CLEAR
