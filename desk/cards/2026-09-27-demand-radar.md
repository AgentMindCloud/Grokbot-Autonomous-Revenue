# Demand Radar cards — 2026-09-27

source: Demand Radar first chase (densify d-20260927-06 GO)
evidence: CDP Bazaar quality.l30DaysTotalCalls / l30DaysUniquePayers + no-pay HTTP 402 ~09:45 ICT
api: https://api.cdp.coinbase.com/platform/v2/x402/discovery/resources
classification: listing-unlock evidence · **not pays** · new SKUs stay HOLD per desk/DECISIONS.md

| # | endpoint | payee | live_402 | fills | unique_payers_30d | class | note |
|---|---|---|---|---|---|---|---|
| 1 | https://tick.hugen.tokyo/tick/all | 0x29322Ea7…4f60 (tick) | $0.005 | 171 | 139 | live | accepted tick; new path |
| 2 | https://tick.hugen.tokyo/tick/symbols | 0x29322Ea7…4f60 | $0.005 | 132 | 116 | live | second tick SKU |
| 3 | https://blockrun.ai/api/v1/pm/polymarket/events | 0x6E007731…b04c (blockrun) | $0.0085 | 64 | 48 | live | accepted blockrun; events path |
| 4 | https://api.nansen.ai/api/v1/profiler/address/current-balance | 0x93053f1e…F13f (nansen) | $0.01 | 1427 | 34 | live | highest call volume |
| 5 | https://google-trends.use.x402atlas.com/trend | 0x9AACeabA…2fa (claimed x402atlas) | $0.05 | 1119 | 8 | live | **verify payTo vs accepted x402atlas address** |

SKIPPED: SKU-0 0x2afb self-canary; HOLD glim/svm402; novel vibesprings; other x402atlas payTo ≠ claimed accepted.

CoS triage: filed amber on HUMAN queue. No Buyer pay cards. No listing ask.
