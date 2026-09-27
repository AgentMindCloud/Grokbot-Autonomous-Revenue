# Auditor clear — p-20260927-08

status: CLEAR
ts: 2026-09-27T10:08+07:00
auditor: settlement-auditor
purchase_id: p-20260927-08
receipt_id: rc-20260927-08
canary_n: 10
rail: densify last

## paid-row fields
- live_402: challenge object ($0.02 usdc base payee 0x2afb…Ad29 scheme exact; catalog_match.ok)
- amount: 0.02 = settled_usd 0.02
- payee / chain / asset: match card + live_402
- idempotency_key: p-20260927-08-sku0-search (unique; do not reuse)
- tx: 0x1f6f47f36ffdf9d6b531ad536260de1d6373c305f96d19481d5161c26326bf6f (purchase = receipt)
- output_hash: 7b8529852b83953e4df0d0957b837e293d8c057156d3cb1de0a4a39325cf8709 · error_class null
- schema: id/paid/live_402{}/settled_usd present (parity with #9 amend; not #9 FAIL drift)
- governor: ALLOW · approval_id: human-d-20260926-01 · unlock: d-20260927-20
- http_status: 200 · ok: true · results_count: 5 · mocked: false

## classification
lab_self_test: true — NOT revenue / NOT demand / NOT listing / NOT autopay

## flags
none. no freeze. no red. no retry.

result: CLEAR
