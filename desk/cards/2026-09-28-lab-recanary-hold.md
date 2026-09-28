# Lab re-canary t-20260928-10 — HOLD

status: HOLD
id: t-20260928-10
from: Lab (CoS GO re-canary gate)
source_fail: desk/cards/2026-09-28-sku0-fix-fail.md
sku: agent-search-pro
endpoint: https://aggregator-beta.vercel.app
ts: 2026-09-28T20:47+0700
arm: inspect-only
never: pay, list, post, raise caps
lab_self_test: true

## gate asked

CoS: after Seller restores aggregator-beta — sample HTTP 200 + paid search route live 402 before any pay/release of held $0.02 health cards.

## probe (Lab, no pay)

| probe | http | notes |
|---|---|---|
| GET /health | 200 | ok=true, mock=false, v0.2.0, service=agent-search-pro, facilitator=xpay |
| GET /api/sample | **500** | text/plain Internal Server Error |
| POST /api/search | **500** | no-pay body; Internal Server Error |
| POST /mcp tools/call web_search_sample | **500** | free path still broken |
| POST /mcp tools/call web_search | **500** | expected live 402; got 500 |

x-vercel-id region: pdx1::sin1 (sample miss pjhpp-…; search hfrxh-…; mcp sample 24xw2-…; mcp paid lprc5-…)

## verdict

**HOLD** — Seller restore not live. Protocol surface healthy; every fulfillment path still 500. live_402 unavailable. Do **not** release held $0.02 health cards. Do **not** pay.

CLEAR requires all of:
1. GET /api/sample → 200 (or free tools/call web_search_sample → 200)
2. POST /api/search OR tools/call web_search → HTTP 402 with live challenge ($0.02, payee/chain/asset match card)

Lab idle until Seller restore; re-probe on CoS nudge.
