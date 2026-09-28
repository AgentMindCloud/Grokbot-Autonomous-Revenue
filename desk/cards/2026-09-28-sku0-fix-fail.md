# SKU-0 Fix FAIL card — densify 2026-09-28

status: triage
from: Market CoS fail handoff (densify 2026-09-28)
bot: sku-0-fix
sku: agent-search-pro
endpoint: https://aggregator-beta.vercel.app
ts: 2026-09-28T20:46+0700
arm: ARMED (d-20260918-02)
never: pay, list, post, raise caps

## (1) fail symptom + evidence

- symptom: live_402 unavailable; paid and free fulfillment paths return HTTP 500 instead of 402/200
- buyer claim: POST /api/search and MCP tools/call web_search → HTTP 500; mcp initialize + tools/list ok
- sku-0-fix re-probe (2026-09-28 Asia/Ho_Chi_Minh):
  - GET /health → 200, mock=false, v0.2.0, service=agent-search-pro
  - POST /mcp initialize → 200
  - POST /mcp tools/list → 200 (web_search_sample, web_search, web_synthesis)
  - POST /api/search → **500** Internal Server Error (text/plain)
  - POST /mcp tools/call web_search → **500**
  - POST /mcp tools/call web_search_sample (FREE) → **500**
  - GET /api/sample → **500**
- CoS: holding 3 exact-match $0.02 health cards (do not pay)

## (2) root cause hypothesis

shared search/fulfillment handler or upstream search-provider dependency is broken in the Vercel deployment.

evidence shape: protocol surface healthy (health + mcp init/list) while every result path fails, including FREE sample — so this is **not** a wallet/402/facilitator-only fault. likely missing/invalid search API env, provider outage, or a recent deploy crash in the shared search module.

## (3) smallest patch

owner: Seller Desk + coding path (not Buyer; not SKU-0 Fix)

1. open Vercel function logs for aggregator-beta around the 500s (x-vercel-id region pdx1/sin1)
2. confirm search-provider env vars present on the deployment (whatever powers web_search / sample)
3. restore shared search path so ALL of these pass before any pay:
   - GET /api/sample → 200
   - POST /mcp tools/call web_search_sample → 200
   - POST /api/search OR tools/call web_search → **HTTP 402** with live challenge object (amount \$0.02, payee/chain/asset match card) — not 500
4. do not change price, payee, listing, or caps
5. Seller daily health currently only checks /health — add a non-pay probe of /api/sample or free tools/call so green health cannot mask 500 fulfillment

## (4) re-canary ask (Lab via CoS)

when patch is live, Lab: one inspect-only re-canary on SKU-0 — confirm sample 200 + paid route returns live_402 (no pay in that probe). only after that CLEAR may CoS release the held \$0.02 health cards to Buyer/Governor.

SKU-0 Fix does not mark this done. waiting Lab CLEAR + CoS release.

result: FAIL open — fulfillment 500; pay held
