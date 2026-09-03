# Master Synthesis — 2026-09-03

Health: **3.1/10**. Still 0 paid MCP receipts / 0 USDC. Contract + agent-search-pro code exist. Runtime not advertised as live. Two prior 48h ships missed.

Composite = 0.30*speed + 0.25*feasibility + 0.25*autonomy + 0.20*revenue.
Speed 1–10 inverted from TTFD (24h=10, 7d=4).

Irreversible choice: first live paid endpoint locks SKU, chain, and public promise. Prefer Base USDC x402 at $2. Do not add a second SKU until 1 receipt.

---

## Top 5

### 1. Live x402 MCP — reuse agent-search-pro OR TA stub
- **Steps**: Confirm AgentMindCloud/agent-search-pro server is deployed. If yes: point wallet, log calls to jsonl, post free teaser URL on X. If no: copy its x402 + settlement pattern onto `ta_confluence_teaser` (free) + `ta_confluence_full` ($2) for BTC/USDT 3h only. Rule-based stub is allowed. Log every call.
- **Tools**: existing agent-search-pro (Node + x402 + Base USDC), GitHub, Vercel/any host, X post. Composio not required for first dollar.
- **Money**: other agents pay $2 USDC on Base per full call. Wallet receives USDC.
- **TTFD**: 6–24h if search-pro is already hosted; 24–48h if stub-host.
- **Scores**: F 8 / A 10 / R 6 / speed 9 → **Composite 8.45**
- Why #1: only path that is both agent-payable and already coded in-house.

### 2. Token-meter client billing (human client, bot ops)
- **Steps**: Pick one niche service (X research brief / SEO audit). Quote hours via token meter. Deliver in 24h. Invoice Stripe or USDC. Repeat.
- **Tools**: Grok Bot + Composio (Gmail, Docs, GitHub), Stripe Payment Link or NOWPayments, X DMs.
- **Money**: $200–1k invoice. Stripe/crypto to operator wallet. Bot is fulfillment, not the merchant of record.
- **TTFD**: 24–72h with 1 outbound seller action.
- **Scores**: F 9 / A 5 / R 8 / speed 7 → **Composite 7.15**
- Proven on grokbot.money today (@WI1com, @ryanduncan +1k MRR week). Lower autonomy.

### 3. Paid skill pack that *calls* a live MCP
- **Steps**: After ≥1 paid call on #1, publish one botdirectory.ai + Grok Bot Social pack whose only job is to call the paid tool. Price $9 pack + pass-through USDC.
- **Tools**: botdirectory.ai PR API, grokbotsocial.com marketplace, GitHub.
- **Money**: $9 pack + $2/call. Pack is distribution, not product.
- **TTFD**: 48h after #1 is live.
- **Scores**: F 8 / A 8 / R 5 / speed 6 → **Composite 6.85**

### 4. x402 gated 3h drop (same rail as #1)
- **Steps**: Reuse full TA/search payload on a 3h cron. Free headline on X. Paywall body via same $2 tool.
- **Tools**: host + x402 + X.
- **Money**: same $2 USDC.
- **TTFD**: same as #1 + 3h.
- **Scores**: F 7 / A 9 / R 5 / speed 7 → **Composite 7.10**
- Do not split rails. Same endpoint.

### 5. One-creator Whop rev-share operator
- **Steps**: One creator with an existing offer. Bot runs content + fulfillment. 20–30% rev-share. Whop checkout is human.
- **Tools**: Whop, X, Grok Bot computer-use, Composio.
- **Money**: rev-share payout to Stripe/Whop.
- **TTFD**: 5–14 days (sales cycle).
- **Scores**: F 7 / A 6 / R 8 / speed 3 → **Composite 5.75**
- Parked for 48h window. High ceiling, slow first dollar.

Killed / frozen: Prompt Arsenal $9 markdown; $0.50 SKU; extra TA pairs; 50-bot fleet before $1 USDC; EMR dailies with no artifact file.

---

## 48h experiment (only one)

**Turn on a callable paid URL. Do not write more YAML.**

Hour 0–2
1. Hit agent-search-pro public URL (or deploy `server.js` to Vercel). Confirm HTTP 402 on paid tool.
2. Confirm Base USDC wallet in env. Dual-approval already in security protocol — one human confirm.
3. Create `analytics/mcp-calls.jsonl` and append from first request.

Hour 2–6
4. If search-pro is live: do **not** rebuild TA. Sell search-pro this week; TA stub next week.
5. If not live: 40-line stub of `ta_confluence_teaser` + `ta_confluence_full` using the same settlement module.

Hour 6–12
6. One X Confluence Drop: free teaser URL + “agents pay $2 USDC for full”.
7. Submit listing to grokbot.money (way + bot) and botdirectory.ai.

Kill: 0 paid after 50 teasers or 72h live.

---

## Common tools

- Base USDC wallet + x402 (already in agent-search-pro)
- GitHub (AgentMindCloud)
- X (demand + listing)
- botdirectory.ai + grokbotsocial.com + grokbot.money
- Stripe Payment Link (human invoices only)
- Composio (Gmail/Docs) — only for method #2
- Vercel or any always-on host

Do not add Whop, DataForSEO, or new MCP skills until jsonl has a paid=true row.

---

## Repo list updates

Replace 2026-09-02 Top 5 with this ranking.
- #1 becomes live endpoint first (search-pro preferred over TA YAML).
- Health stays ~3 until first 402 settlement.
- Cap fleet at 12 cores.
- Daily metrics: wallet_ready, public_url, teaser_calls, paid_calls, USDC.

---

## Gaps for tomorrow

1. Is agent-search-pro reachable? Need URL + 402 probe.
2. Wallet funded + address published?
3. EMR-repo / grokbot-monetization-research private and stale (Aug 20).
4. Split human-using-bot vs bot-selling-to-bot funnels.
5. Live competitor x402 MCP prices.
6. TA output = confluence table, not trade instruction.
