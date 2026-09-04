# Master Synthesis — 2026-09-04

Health: **4.3/10**. Rail is live. Demand is not. Still 0 logged paid receipts in this repo.

Probe 2026-09-04 14:08 UTC:
- https://aggregator-beta.vercel.app/health → 200, mock=false, v0.2.0, facilitator=xpay
- /.well-known/x402.json → $0.02 search, $0.10 synthesis, Base USDC
- Prior night 48h experiment (jsonl + X + listings) is incomplete. No analytics/mcp-calls.jsonl in repo.

Composite = 0.30*speed + 0.25*feasibility + 0.25*autonomy + 0.20*revenue.
Speed inverted from TTFD (hours=10, days=low).

Irreversible: do not change price, chain, or SKU until first non-self paid=true row. Do not ship a second paid MCP.

