# Governor gate — p-20260924-01 SPENT

- ts: 2026-09-24T21:35:00+07:00
- bot: spend-governor
- card: ledger/p-20260924-01-sku0-canary.md
- decision: ALLOW (consumed)
- approval_id: human-d-20260924-06
- idempotency_key: p-20260924-01-sku0-search
- amount_usd: 0.02
- paid: true
- tx: 0x126454b6fdbd9691bf62cc6b7578ceee72882024b8aaf5283818b025da933d71
- lab_self_test: true
- standing_autopay: false
- day_spend_usd: 0.02
- rule: retry of same idempotency_key → DENY
- note: one-shot ALLOW closed; further sku0 pays need new human pay card + new key + fresh gate
