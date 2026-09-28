# Purchase Card p-20260928-02 — UNLOCKED (external tick/symbols one-shot)

status: unlocked
approval: payee-accepted d-20260925-08 (tick) + EXTERNAL_ONE_SHOT d-20260928-03 + unlock d-20260928-05
pay: true
lab_self_test: false
standing_autopay: false
external_one_shot: true
source: desk/cards/2026-09-27-demand-radar.md

sku: tick/symbols
endpoint: https://tick.hugen.tokyo
method: GET https://tick.hugen.tokyo/tick/symbols
expected_catalog_usd: 0.005
max_usd: 0.005
chain: base
asset: USDC
payee: 0x29322Ea7EcB34aA6164cb2ddeB9CE650902E4f60
asset_token: 0x833589fCD6eDb6E08f4c7C32D4f71b54bdA02913
idempotency_key: p-20260928-02-tick-symbols
approval_id: d-20260928-03
unlock_decision_id: d-20260928-05

## live_402 inspect (no-pay GET 2026-09-28T20:44+07:00) — MATCH
- http_status: 402
- x402Version: 2
- resource_url: https://tick.hugen.tokyo/tick/symbols
- scheme: exact
- network: eip155:8453 (Base) — Solana accept present; **desk uses Base only**
- amount_atomic: 5000 (= $0.005)
- asset: 0x833589fCD6eDb6E08f4c7C32D4f71b54bdA02913 (USD Coin)
- payTo: 0x29322Ea7EcB34aA6164cb2ddeB9CE650902E4f60
- catalog_match: amount $0.005 / Base USDC / payTo == accepted tick payee d-20260925-08 and tick/all d-20260927-24 → ok
- paymentFlow: authorization (x402 v2 payment-required header)
- source: demand-radar 2026-09-27 rank 3 (accepted / refresh) plus this no-pay GET
- note: GET only. Sample body returned with 402 notice. This file is not a payment.

## rules
- UNLOCK_PAY d-20260928-05. Buyer pays once after Governor ALLOW. This file is not a payment.
- Verify payTo on fresh live 402 vs 0x29322Ea7EcB34aA6164cb2ddeB9CE650902E4f60 before any pay.
- Stop on mismatch (amount/asset/chain/payee).
- Not novel payee (accepted d-20260925-08). Not listing. Not X. Not SKU-0 densify pack. NOT autopay. NOT lab_self_test.
- Do not use Solana accept. Day cap $10.
- On pay (after unlock+ALLOW only): SCHEMA-aligned purchases/receipts rows (id/paid/live_402{}/settled_usd).

Buyer Desk (UNLOCK_PAY active — pay once after Governor ALLOW):
1. Re-fetch live 402. Stop if payee/chain/asset/amount != this card.
2. Ask Spend Governor ALLOW.
3. Pay once with idempotency_key above. Never retry success.
4. Append SCHEMA-aligned purchases.jsonl + receipts.jsonl. Hand Auditor + Lab.
5. Stop.
