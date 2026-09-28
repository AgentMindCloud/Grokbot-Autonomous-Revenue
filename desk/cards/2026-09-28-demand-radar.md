# Demand Radar — 2026-09-28

- **ts:** 2026-09-28 20:47 +07 (Asia/Ho_Chi_Minh)
- **source:** CDP Bazaar `https://api.cdp.coinbase.com/platform/v2/x402/discovery/resources` (paged ~18.8k; quality.l30DaysTotalCalls / l30DaysUniquePayers) + desk/DECISIONS.md + ledger/decisions.jsonl ACCEPT_PAYEE + prior `desk/cards/2026-09-27-demand-radar.md`
- **method:** live HTTP 402 via `estimate_payment` (user-buyer-payment-worker) + curl decode of `PAYMENT-REQUIRED` — **no pay**; Base USDC only (`eip155:8453` / `0x833589fCD6eDb6E08f4c7C32D4f71b54bdA02913`); prefer `live_402_usd ≤ 0.25`; rank by `unique_payers_30d` desc then `fills_seen`; accepted payees only
- **classification:** listing-unlock evidence · **not pays** · novel SKUs stay HOLD unless ACCEPT_PAYEE
- **ops:** Demand Radar **never pays** · never `make_x402_request` / `get_my_wallet` · never messages agents

## Ranked unlock cards (accepted payees)

| rank | endpoint | payee | live_402_usd | fills_seen | unique_payers_30d | class | why unlocks | payTo_verify |
|---:|---|---|---:|---:|---:|---|---|---|
| 1 | `https://tick.hugen.tokyo/tick/latest` | `0x29322Ea7EcB34aA6164cb2ddeB9CE650902E4f60` | 0.005 | 339 | 175 | live | Highest unique-payer density on accepted tick (d-20260925-08); live 402 Base USDC $0.005 reconfirmed | ok |
| 2 | `https://tick.hugen.tokyo/tick/all` | `0x29322Ea7EcB34aA6164cb2ddeB9CE650902E4f60` | 0.005 | 167 | 135 | live | All-pairs FX BBO; EXTERNAL_ONE_SHOT rail was Buyer-side (d-20260927-24/25) — **DR does not pay** | ok |
| 3 | `https://tick.hugen.tokyo/tick/symbols` | `0x29322Ea7EcB34aA6164cb2ddeB9CE650902E4f60` | 0.005 | 128 | 114 | live | Symbol discovery before tick subscribe; live 402 $0.005 reconfirmed (curl + estimate_payment) | ok |
| 4 | `https://blockrun.ai/api/v1/pm/polymarket/events` | `0x6E007731870EDe419CfB31889Cd5C4493CEcb04c` | 0.0085 | 64 | 48 | live | Accepted blockrun PM payee (d-20260925-03); live 402 $0.0085 Base USDC | ok |
| 5 | `https://api.nansen.ai/api/v1/profiler/address/current-balance` | `0x93053f1e7A5eFEDa532Fe69CbbE43cBEc3A0F13f` | 0.01 | 1383 | 35 | live | Highest fills_seen in prior set; accepted nansen (d-20260924-08); live 402 $0.01 | ok |
| 6 | `https://kronossignals.com/api/v1/liquidations/btc` | `0x36038e1d712c5e39f35952164ec58ec2b96caee7` | 0.02 | 45 | 28 | live | Accepted kronos (d-20260924-05); was under-ranked as “novel held” on 09-27 — corrected; live 402 $0.02 | ok |
| 7 | `https://x402.glassnode.com/v1/metadata/metrics` | `0x1f81da453901D15296c1710af83e0Bc0371D39f1` | 0.01 | 29 | 15 | live | Accepted glassnode (d-20260924-12); strongest unique among non-prior siblings today; live 402 $0.01 | ok |
| 8 | `https://api.oblique.markets/api/v1/paid/base-gas-price` | `0x970007590aCC5C938cd51345B17AF51B1B40D3Ab` | 0.002 | 20 | 15 | live | Accepted oblique (d-20260921-01); cheap Base gas probe; live 402 $0.002 | ok |
| 9 | `https://google-trends.use.x402atlas.com/trend` | `0x9AACeabAD8E1858b72fcEA1665381B168841b2fa` | 0.05 | 1146 | 9 | live | Accepted x402atlas (d-20260925-12); high fills / concentrated payers; **payTo MATCH** | MATCH |
| 10 | `https://base-gas-x402-production.up.railway.app/gas` | `0x0D083590c048A243e24a75E3a7C968145DE25B44` | 0.005 | 682 | 8 | live | Accepted base-gas railway (d-20260925-10); strong fills_seen; live 402 $0.005 payTo match `0x0D0835…` | ok |
| 11 | `https://api.agentservices.to/v1/fx` | `0x9863aB6242663FCc84c33632741711dB78f8Fd15` | 0.003 | 54 | 8 | thin | Accepted agentservices (d-20260924-11); live 402 $0.003; thinner unique vs tick/blockrun | ok |

### Accepted scanned but not ranked (weak unique / CF / thin)

| operator | sample endpoint | unique_30d | fills | note |
|---|---|---:|---:|---|
| omniterminal | `/api/x402/v1/news` | 11 | 15 | bazaar stats; live probe HTTP 403 CF from box — no fresh payTo body |
| lionx402 | `/api/x402/wallet-screen-json` | 10 | 22 | bazaar stats; live probe HTTP 403 CF |
| ozmium | `/v1/loan/markets` | 8 | 24 | bazaar stats; live probe HTTP 403 CF |
| lonestar | `options…/flow` etc. | ≤7 | — | below strong-unique bar |
| voidfeed / celerapi / anchor / agent-commerce-factory / aiagentoracle / agentmercantile / geoprimitives | various | ≤6 (geo timezone=4) | — | accepted but not strong unique today |

## x402atlas payTo verification (r-20260924-e05 / d-20260925-12)

| field | value |
|---|---|
| endpoint | `https://google-trends.use.x402atlas.com/trend` |
| accepted payTo | `0x9AACeabAD8E1858b72fcEA1665381B168841b2fa` |
| live Base payTo (HTTP 402 + estimate_payment) | `0x9AACeabAD8E1858b72fcEA1665381B168841b2fa` |
| live amount | `50000` atomic = **$0.05** USDC on `eip155:8453` / asset `0x833589fCD6eDb6E08f4c7C32D4f71b54bdA02913` |
| CDP quality | fills_seen **1146** · unique_payers_30d **9** |
| **result** | **MATCH** |
| related | `/related-queries` live payTo same address, $0.03 (amt 30000), unique 10 / fills 397 — also MATCH |

Probe ts: 2026-09-28 20:47 +07. Methods: curl HTTP/2 402 `accepts[0].payTo` + `estimate_payment` recipient. No payment made.

## Skips / holds

| item | reason |
|---|---|
| SKU-0 `0x2afbBE0F1D4F2c721B7e535E695f72e88997Ad29` | self-canary — skip (not unlock card) |
| glim `0xC751344Ee09B5159160173F77D4a1169bCd386A1` | HOLD (d-20260925-04) Solana/new_chain |
| svm402 | HOLD (d-20260925-11) Solana/new_chain |

## Novel payees held (not ranked as unlock cards)

Flag only — do not unlock without ACCEPT_PAYEE (or wrong payTo on accepted host):

| unique_30d | fills | usd | payTo | endpoint (sample) |
|---:|---:|---:|---|---|
| 192 | 189449 | 0.002 | `0xe9030014F5DAe217d0A152f02A043567b16c1aBf` | blockrun **chat/completions** (≠ accepted blockrun PM `0x6E007731…`) |
| 23 | 1727 | 0.011 | `0xe9030014F5DAe217d0A152f02A043567b16c1aBf` | blockrun **exa/search** (≠ accepted PM payee) |
| 22 | 204 | 0.01 | `0xF752eEB75d3Bea24AA867ad93bfd8EF5a2F431B9` | x402atlas websearch (≠ accepted atlas `0x9AAC…`) |
| 22 | 24 | 0.001 | `0x38C063312719220c676E988f0DEE14B4ec0e44C8` | vibesprings base-gas (≠ accepted base-gas railway `0x0D0835…`) |
| 20 | 26 | 0.005 | `0xA55B06462A2e48661bAdF22f5841F95aE654b716` | x402atlas hyperliquid-predict |
| 19 | 492 | 0.006 | `0x51D577C8CBB8b3fB1BA0CE31c7923cC27a07F78B` | x402atlas twitter/search |

## Ops note

Demand Radar **never pays**. Prior tick/all one-shot remains Buyer/CoS/Governor rail only — not DR action. No `make_x402_request`, no wallet reads, no agent messages this run.
