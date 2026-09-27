# Demand Radar — 2026-09-27

- **ts:** 2026-09-27 10:27 +07 (Asia/Ho_Chi_Minh)
- **source:** CDP Bazaar `https://api.cdp.coinbase.com/platform/v2/x402/discovery/resources` (paged ≤2k for host filter) + prior demand-radar hits
- **method:** live HTTP 402 via `estimate_payment` + curl — **no pay**; Base USDC only; `live_402_usd ≤ 0.25`; rank by `l30DaysUniquePayers` desc then `l30DaysTotalCalls`; prefer accepted payees (desk/DECISIONS.md)
- **note:** tick/all $0.005 one-shot is **Buyer-queued** — Demand Radar does **not** pay
- **classification:** listing-unlock evidence · **not pays** · novel SKUs stay HOLD unless ACCEPT_PAYEE

## Ranked unlock cards (accepted payees)

| rank | endpoint | payee | live_402_usd | fills_seen | unique_payers_30d | class | why unlocks | payTo_verify |
|---:|---|---|---:|---:|---:|---|---|---|
| 1 | `https://tick.hugen.tokyo/tick/latest` | `0x29322Ea7EcB34aA6164cb2ddeB9CE650902E4f60` | 0.005 | 353 | 172 | accepted / refresh | Highest unique-payer density on accepted tick payee; live 402 Base USDC $0.005 confirmed | ok |
| 2 | `https://tick.hugen.tokyo/tick/all` | `0x29322Ea7EcB34aA6164cb2ddeB9CE650902E4f60` | 0.005 | 171 | 139 | accepted / Buyer-queued | Prior card still valid; all-pairs FX BBO; **Buyer-queued one-shot — DR does not pay** | ok |
| 3 | `https://tick.hugen.tokyo/tick/symbols` | `0x29322Ea7EcB34aA6164cb2ddeB9CE650902E4f60` | 0.005 | 132 | 116 | accepted / refresh | Prior card still valid; symbol discovery before tick subscribe | ok |
| 4 | `https://blockrun.ai/api/v1/pm/polymarket/events` | `0x6E007731870EDe419CfB31889Cd5C4493CEcb04c` | 0.0085 | 64 | 48 | accepted / refresh | Prior card still valid; Polymarket events list; live 402 $0.0085 Base USDC | ok |
| 5 | `https://api.nansen.ai/api/v1/profiler/address/current-balance` | `0x93053f1e7A5eFEDa532Fe69CbbE43cBEc3A0F13f` | 0.01 | 1427 | 34 | accepted / refresh | Prior card still valid; highest fills_seen among accepted set; live 402 $0.01 | ok |
| 6 | `https://google-trends.use.x402atlas.com/trend` | `0x9AACeabAD8E1858b72fcEA1665381B168841b2fa` | 0.05 | 1119 | 8 | accepted / refresh | Prior card still valid; SEO/demand series; **payTo MATCH** r-20260924-e05 | ok |

## x402atlas payTo verification (r-20260924-e05)

| field | value |
|---|---|
| endpoint | `https://google-trends.use.x402atlas.com/trend` |
| accepted payTo | `0x9AACeabAD8E1858b72fcEA1665381B168841b2fa` |
| live Base payTo (HTTP 402 + estimate_payment) | `0x9AACeabAD8E1858b72fcEA1665381B168841b2fa` |
| live amount | `50000` atomic = **$0.05** USDC on `eip155:8453` / asset `0x833589fCD6eDb6E08f4c7C32D4f71b54bdA02913` |
| **result** | **MATCH** |
| related | `/related-queries` live payTo same address, $0.03 (amt 30000) — also MATCH |

Probe ts: 2026-09-27 10:27 +07. Methods: curl HTTP/2 402 body `accepts[0].payTo` + `estimate_payment` recipient. No payment made.

## Skips / holds

| item | reason |
|---|---|
| SKU-0 `0x2afbBE0F1D4F2c721B7e535E695f72e88997Ad29` | self-canary — skip (not unlock card) |
| glim `0xC751344Ee09B5159160173F77D4a1169bCd386A1` | HOLD (d-20260925-04) Solana/new_chain |
| svm402 | HOLD (d-20260925-11) Solana/new_chain |

## Novel payees held (not ranked as unlock cards)

Flag only — do not unlock without ACCEPT_PAYEE:

| unique_30d | fills | usd | payTo | endpoint (sample) |
|---:|---:|---:|---|---|
| 29 | 45 | 0.02 | `0x36038e1d712c5e39f35952164ec58ec2b96caee7` | kronossignals liquidations/btc |
| 23 | 1723 | 0.011 | `0xe9030014F5DAe217d0A152f02A043567b16c1aBf` | blockrun **exa** (≠ accepted blockrun PM payee `0x6E007731…`) |
| 23 | 255 | 0.002 | `0x38C063312719220c676E988f0DEE14B4ec0e44C8` | vibesprings btc-usd |
| 22 | 204 | 0.01 | `0xF752eEB75d3Bea24AA867ad93bfd8EF5a2F431B9` | x402atlas websearch (≠ accepted atlas `0x9AAC…`) |
| 21 | 28 | 0.005 | `0xA55B06462A2e48661bAdF22f5841F95aE654b716` | x402atlas hyperliquid-predict |
| 19 | 492 | 0.006 | `0x51D577C8CBB8b3fB1BA0CE31c7923cC27a07F78B` | x402atlas twitter/search |

## Ops note

Demand Radar **never pays**. tick/all $0.005 one-shot remains **Buyer-queued** under existing Buyer/CoS/Governor rail — not DR action.
