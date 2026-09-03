# Ranked Playbooks — Grokbot Autonomous Revenue

*Updated 2026-09-03 by Master-Synthesizer*

Data (2026-08-29 → 2026-09-03): 0 paid MCP receipts, 0 USDC, 0 issues/PRs. `contracts/ta-confluence.yaml` exists. `AgentMindCloud/agent-search-pro` has a full x402 Node server (unconfirmed public host). Social packs ~3–4 installs / $0. First-x402-by-Day-10 missed. Health **3.1/10**.

Composite = 0.30*speed + 0.25*feasibility + 0.25*autonomy + 0.20*revenue.

---

## Top 5 (2026-09-03)

### 1. Live x402 MCP — agent-search-pro first, TA stub second
- Stop designing YAML. Turn on a URL that returns HTTP 402.
- **Money**: $2 USDC Base per full call. Bundle 8/$12 only after first receipt.
- **TTFD**: 6–24h if search-pro is hosted; else 24–48h stub.
- **Feasibility 8 / Autonomy 10 / Revenue 6 / speed 9 / Composite 8.45**

### 2. Token-meter client billing
- One niche deliverable, Stripe/USDC invoice, bot does the work.
- **TTFD**: 24–72h. Human seller step required.
- **Feasibility 9 / Autonomy 5 / Revenue 8 / speed 7 / Composite 7.15**

### 3. x402 gated 3H drop (same endpoint as #1)
- Reuse payload. Not a new product.
- **Feasibility 7 / Autonomy 9 / Revenue 5 / speed 7 / Composite 7.10**

### 4. Paid skill pack that *calls* the live MCP
- Wrapper only after ≥1 paid call. botdirectory + Grok Bot Social.
- **Money**: $9 pack + per-call USDC.
- **Feasibility 8 / Autonomy 8 / Revenue 5 / speed 6 / Composite 6.85**

### 5. One-creator Whop rev-share
- Parked for 48h. Sales cycle too long for first dollar.
- **Feasibility 7 / Autonomy 6 / Revenue 8 / speed 3 / Composite 5.75**

## Kill / defer
- Prompt Arsenal Pack $9–19: killed
- $0.50 SKU: killed until first $2 receipt
- Extra TA pairs/TFs: killed
- Full 50-bot fleet before $1 USDC: cap at 12 cores
- EMR dailies with no output file: pause
- New paid MCP skills: freeze until jsonl has paid=true

## 48h experiment (only one)
1. Probe or deploy agent-search-pro. Confirm 402.
2. Wallet on Base USDC. Log `analytics/mcp-calls.jsonl`.
3. One X post with free teaser URL.
4. List on grokbot.money + botdirectory.ai.
Kill if 0 paid after 50 teasers or 72h live.
