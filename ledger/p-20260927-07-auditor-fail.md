# Auditor FAIL — p-20260927-07

status: FAIL
ts: 2026-09-27T10:00+07:00
auditor: settlement-auditor
purchase_id: p-20260927-07
receipt_id: rc-20260927-07
canary_n: 9

## claim vs ledger
- tx: 0x7865c5d2643674011cd1aabcb7e1e145329cea0ad39b20bbca2a9fdfb5ef1962 (purchase = receipt; matches CoS claim)
- amount_usd: 0.02 = receipt amount_usd 0.02
- payee / chain / asset: present; match claim
- idempotency_key: p-20260927-07-sku0-search (unique)
- output_hash: 56c1a13e6942bd7f9f5c75d7f13f8a396fce4516f9162110e218fe1ec65715dd present

## mismatches (hard)
- live_402: boolean `true` — not challenge object (need amount/payTo/network/asset/catalog_match). cannot prove live_402 ≡ settled
- schema:purchase missing `id` / `paid` / structured `live_402{}` (SCHEMA.md + prior paid rows)
- schema:receipt missing `id` / `settled_usd` (has receipt_id / amount_usd)

## classification
lab_self_test: true — NOT revenue / NOT demand
do not retry pay. do not unlock #10 (CoS owns unlock).

## action
RED to Market CoS. request Spend Governor freeze SKU agent-search-pro until row schema restored + live_402 challenge object filed (amend/append — never edit past line? append amend row).

result: FAIL
