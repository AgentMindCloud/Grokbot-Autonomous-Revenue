# Auditor clear — p-20260927-02

status: CLEAR
ts: 2026-09-27T09:45+07:00
auditor: settlement-auditor
purchase_id: p-20260927-02
receipt_id: rc-20260927-02
canary_n: 4

## paid-row fields
- live_402: yes ($0.02 usdc base payee 0x2afb…Ad29 scheme exact)
- amount: 0.02 = settled_usd 0.02
- payee / chain / asset: match card + live_402
- idempotency_key: p-20260927-02-sku0-search (unique; do not reuse)
- tx: 0x4353b306f818e050cc5fc18bf797091efe8126164cd904469a8eba006c5b58d9 (purchase = receipt)
- output_hash: 26e4b6ea7f6864da4392913453e0b3d324d321af7f72031854ed32c705d50198 · error_class null
- catalog_match.ok: true (not catalog-as-authority)
- governor: ALLOW · approval_id: human-d-20260926-01 · unlock: d-20260927-04
- http_status: 200 · ok: true · results_count: 5 · mocked: false

## classification
lab_self_test: true — NOT revenue / NOT demand / NOT listing / NOT autopay

## flags
none. no freeze. no red. no retry.

result: CLEAR
