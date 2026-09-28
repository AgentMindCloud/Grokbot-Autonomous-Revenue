# Seller Desk — SKU-0 restore BLOCKED

- date: 2026-09-28 20:49 Asia/Ho_Chi_Minh
- from: Market CoS GO on desk/cards/2026-09-28-sku0-fix-fail.md
- goal: restore sample 200 + paid route live_402 (never pay, never list)
- repro confirmed (box only): GET /health 200 mock=false v0.2.0; POST /api/search 500; MCP tools/call web_search_sample 500; GET /api/sample 500
- blocker: no source repo visible to Seller Desk
  - AgentMindCloud/agent-search-pro → 404
  - AgentMindCloud/aggregator-beta → 404
  - CloudAgent repositories search aggregat|agent-search|sku → 0
  - no vercel CLI / VERCEL_* on Seller Desk box
  - historical cloud agent PR pointed at AgentMindCloud/agent-search-pro/pull/1 but repo not readable now
- not used: user KitchenPC (local tools Never; wrong surface anyway)
- need (one of): github URL for live aggregator-beta source with write+deploy, OR vercel project access + search-provider env fix
- no price/payee/list/X change attempted