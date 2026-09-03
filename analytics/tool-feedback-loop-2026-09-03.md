# Tool Feedback Loop — 2026-09-03 (night probe)

Probe 15:59 UTC: `https://aggregator-beta.vercel.app` is live.
- GET /health 200, mock=false, v0.2.0, xpay facilitator
- GET /.well-known/x402.json 200 ($0.02 search, $0.10 synthesis, Base USDC)
- MCP tools/list 200: web_search_sample / web_search / web_synthesis
- tools/call web_search_sample 200 in ~2.2s
- unpaid web_search → HTTP 402 + PAYMENT-REQUIRED (eip155:8453, amount 20000 = $0.02 USDC, payTo 0x2afbBE0F…)

No `mcp-calls.jsonl` in this repo. No issues/PRs. Social packs ~3–4 / $0. README claims one dogfood 0.02 USDC tx (not independently verified on-chain here).

## Health (1–10)

| skill | score | why |
|-------|------:|-----|
| Agent Search Pro (live paid MCP) | **5.6** | Product 4/4 + rail 2/3 (works, volume ~0) + reuse 0/2 + demand proxy 1.6 |
| TA Confluence Signal (YAML only) | **2.8** | Contract exists, no URL, 0 calls. Demote until search-pro has paid_calls ≥ 1 |

Fleet health: **4.2/10** (was 3.1 this morning — lift is host confirmation, not revenue).

## Metrics
| metric | search-pro | TA |
|--------|------------|-----|
| public_url | aggregator-beta.vercel.app | none |
| teaser_calls (logged) | 0 in GAR jsonl (probe sample succeeded) | 0 |
| paid_calls | 0 logged (1 claimed dogfood) | 0 |
| USDC | ~0.02 claimed | 0 |
| p95_ms | teaser ~2200, 402 ~560 | n/a |
| error_rate | n/a (no log) | n/a |
| wallet_ready | payTo present in 402 | n/a |

Kill: new TA pairs/TFs, $2 TA SKU this week, Prompt Arsenal, $0.50 SKU, extra paid MCP skills, 50-bot expand.
