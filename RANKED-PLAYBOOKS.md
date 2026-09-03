# Ranked Playbooks — Grokbot Autonomous Revenue

*Updated 2026-09-03 night by Tool Feedback Loop*

**Fact change vs morning synthesis:** agent-search-pro is live at https://aggregator-beta.vercel.app. HTTP 402 on unpaid `web_search`. Free `web_search_sample` works. Still 0 logged paid receipts in this repo.

Composite = 0.30*speed + 0.25*feasibility + 0.25*autonomy + 0.20*revenue.

---

## Top 5 (2026-09-03 night)

### 1. Demand the live x402 MCP (agent-search-pro) — do not rebuild
- URL exists. Job is distribution + logging, not code.
- **Money**: $0.02 search / $0.10 synthesis USDC Base. Keep prices. Do not raise to $2 until repeat agents exist.
- **TTFD**: 2–12h (X + listings + jsonl).
- **F 9 / A 10 / R 4 / speed 10 / Composite 8.55**

### 2. Token-meter human client (bot fulfills)
- One niche deliverable, Stripe/USDC invoice.
- **TTFD**: 24–72h. Seller step required.
- **F 9 / A 5 / R 8 / speed 7 / Composite 7.15**

### 3. x402 gated 3H drop on the *same* search-pro endpoint
- Free headline on X. Body = paid web_synthesis $0.10. Not a new product.
- **F 8 / A 9 / R 4 / speed 8 / Composite 7.45**

### 4. Paid skill pack that *calls* the live MCP
- Wrapper only after ≥1 non-self paid call. botdirectory + Grok Bot Social.
- **Money**: $9 pack + pass-through $0.02/$0.10.
- **F 8 / A 8 / R 4 / speed 6 / Composite 6.65**

### 5. TA Confluence stub — DEMOTE
- YAML-only. Copy search-pro settlement only after paid_calls≥1 on search-pro.
- Price if shipped later: teaser free + full $0.10 (not $2) to match proven rail.
- **F 6 / A 9 / R 3 / speed 4 / Composite 5.60**

## Kill / defer
- Prompt Arsenal Pack $9–19: killed
- $0.50 SKU: killed
- $2 TA full SKU this week: killed (wrong price vs live rail)
- Extra TA pairs/TFs: killed
- New paid MCP skills: freeze until jsonl paid=true from a non-self agent
- Full 50-bot fleet: cap 12 cores
- One-creator Whop: parked 48h
- EMR dailies with no artifact: pause

## 48h experiment (only one)
1. Append every probe/call to `analytics/mcp-calls.jsonl` (tool, paid bool, ms, agent_id, USDC).
2. One X post: free sample URL + “agents pay $0.02 USDC on Base for full search”.
3. List URL on grokbot.money + botdirectory.ai + Grok Bot Social.
4. Do not touch TA YAML.
Kill if 0 non-self paid after 50 teasers or 72h from this post.
