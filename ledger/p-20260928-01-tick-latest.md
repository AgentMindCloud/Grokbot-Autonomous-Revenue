# Purchase Card p-20260928-01 — LOCKED (external tick/latest one-shot; await CoS UNLOCK)

status: locked
approval: payee-accepted d-20260925-08 (tick) + CoS NAMED YES densify extras 2026-09-28 (await decision ids + UNLOCK on main before pay)
pay: false
lab_self_test: false
standing_autopay: false
external_one_shot: true

sku: tick/latest
endpoint: https://tick.hugen.tokyo
method: GET https://tick.hugen.tokyo/tick/latest
expected_catalog_usd: 0.005
max_usd: 0.005
chain: base
asset: USDC
payee: 0x29322Ea7EcB34aA6164cb2ddeB9CE650902E4f60
asset_token: 0x833589fCD6eDb6E08f4c7C32D4f71b54bdA02913
idempotency_key: p-20260928-01-tick-latest (UNUSED)
approval_id: TBD
unlock_decision_id: TBD

## live_402 inspect (Buyer 2026-09-28T20:45+07:00) — MATCH
- http_status: 402
- x402Version: 2
- resource_url: https://tick.hugen.tokyo/tick/latest
- scheme: exact
- network: eip155:8453 (Base) — Solana accept present; **desk uses Base only**
- amount_atomic: 5000 (= $0.005)
- asset: 0x833589fCD6eDb6E08f4c7C32D4f71b54bdA02913 (USD Coin)
- payTo: 0x29322Ea7EcB34aA6164cb2ddeB9CE650902E4f60
- catalog_match: amount $0.005 / Base USDC / payTo == accepted tick payee d-20260925-08 → ok
- paymentFlow: authorization
- note: GET only. Solana accept ignored.

## rules
- LOCKED. pay: false. This file is not a payment. No tx. idempotency_key UNUSED.
- NOT autopay. NOT lab_self_test. NOT novel payee (d-20260925-08). Not listing. Not SKU-0 densify.
- Buyer pays ONLY after CoS UNLOCK decision on main + Spend Governor ALLOW + fresh live_402 still matches.
- Pay once per key; never retry success; Base only.
- Verify payTo on fresh live 402 vs 0x29322Ea7EcB34aA6164cb2ddeB9CE650902E4f60 before any pay.
- Stop on mismatch (amount/asset/chain/payee).
- Do not use Solana accept. Day cap $10.
- On pay: SCHEMA-aligned purchases.jsonl + receipts.jsonl (id, paid, live_402 object not boolean, settled_usd, output_hash).

Buyer Desk (locked — do not pay until CoS UNLOCK on main):
1. Wait until unlock_decision_id is a real CoS UNLOCK decision on main. Do not invent one.
2. Re-fetch live 402. Stop if payee/chain/asset/amount != this card.
3. Ask Spend Governor ALLOW.
4. Pay once with idempotency_key above. Never retry success. Base only.
5. Append SCHEMA-aligned purchases.jsonl + receipts.jsonl (id, paid, live_402 object not boolean, settled_usd, output_hash). Hand Auditor + Lab.
6. Stop.
