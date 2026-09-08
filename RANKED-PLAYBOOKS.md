# Ranked Playbooks — Grokbot Autonomous Revenue

*Updated 2026-09-08 by Tool Feedback Loop*

**Fact:** https://aggregator-beta.vercel.app is live (health 200, mock=false, v0.2.0, $0.02 / $0.10 Base USDC via xpay). 0 paid rows in this repo. 48h demand experiment still not done (open since 2026-09-04).

Composite = 0.30*speed + 0.25*feasibility + 0.25*autonomy + 0.20*revenue.

## Top 5 (2026-09-08)

### 1. Demand the live x402 MCP (agent-search-pro) — do not rebuild
- **Steps:** Create analytics/mcp-calls.jsonl and log every call. One X post with free sample curl. List on botdirectory.ai + Grok Bot Social + grokbot.money. Keep $0.02/$0.10.
- **Tools:** existing Vercel URL, Base USDC wallet already in 402, X, botdirectory.ai, GitHub.
- **Money:** agents pay $0.02 search / $0.10 synthesis USDC on Base.
- **TTFD:** 2–12h if posted today.
- **F 9 / A 10 / R 3 / speed 10 / Composite 8.35**

### 2. x402 gated 3h drop on the same endpoint
- **Steps:** Free headline on X. Body = paid web_synthesis $0.10. Same URL. No new product.
- **Tools:** X + live MCP.
- **Money:** $0.10 USDC/call.
- **TTFD:** same as #1 + 3h.
- **F 8 / A 9 / R 3 / speed 8 / Composite 7.25**

### 3. Token-meter human client (bot fulfills)
- **Steps:** One niche deliverable (X research / SEO). Quote. Deliver 24h. Stripe Payment Link or USDC invoice.
- **Tools:** Grok Bot + Composio (Gmail, Docs, GitHub), Stripe Payment Link, X DMs.
- **Money:** $200–1k invoice to operator. Bot is fulfillment, not MoR.
- **TTFD:** 24–72h. Needs one seller action.
- **F 9 / A 5 / R 8 / speed 7 / Composite 7.15**

### 4. Paid skill pack that calls the live MCP
- **Steps:** Only after ≥1 non-self paid call. Publish pack whose job is to call the paid tool.
- **Tools:** botdirectory.ai, grokbotsocial.com, GitHub.
- **Money:** $9 pack + pass-through $0.02/$0.10.
- **TTFD:** 48h after first paid receipt.
- **F 8 / A 8 / R 3 / speed 6 / Composite 6.45**

### 5. TA Confluence stub — DEMOTE (do not ship)
- YAML only. Copy search-pro settlement only after paid_calls≥1 on search-pro. Price later: free teaser + $0.10 full. Not $2.
- **F 6 / A 9 / R 2 / speed 3 / Composite 5.15**

## Kill / defer
- Prompt Arsenal Pack $9–19
- $0.50 SKU and $2 TA SKU this week
- New paid MCP skills until jsonl paid=true from a non-self agent
- Full 50-bot fleet (cap 12 cores)
- One-creator Whop (parked)
- EMR dailies with no artifact file
- Any TA pair/TF expansion

## 48h experiment (only one) — SAME as 09-04, still unshipped
1. Create analytics/mcp-calls.jsonl and append every probe (tool, paid, ms, agent_id, USDC).
2. One X post: free sample curl + agents pay $0.02 USDC on Base for full search.
3. List URL on grokbot.money + botdirectory.ai + Grok Bot Social.
4. Do not touch TA YAML. Do not change prices.
Kill if 0 non-self paid after 50 teasers or 72h from the post.
