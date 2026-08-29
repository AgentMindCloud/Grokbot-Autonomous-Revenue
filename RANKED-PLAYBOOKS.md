# Ranked Playbooks — Grokbot Autonomous Revenue

*Updated 2026-08-29 by Tool-Feedback-Loop (proxy metrics; no live MCP logs yet)*

Data: 0 paid MCP receipts, 0 USDC tracked, Grok Bot Social packs ~3–4 installs / $0, EMR + monetization-research still stubs, TA Confluence contract exists but no callable paid endpoint, first-x402-by-Day-10 missed.

Composite = 0.30*speed + 0.25*feasibility + 0.25*autonomy + 0.20*revenue.

---

## Top 5 (2026-08-29)

### 1. x402 TA Confluence Signal — free teaser tool + paid full MCP
- **Exact steps**: Expose `ta_confluence_teaser` (free, bias+levels, <800ms) and `ta_confluence_full` (x402 USDC on Base, score table + CI + invalidation). Agents call teaser every 3h; pay only on high-confluence.
- **Tools**: existing `contracts/ta-confluence.yaml`, Coinbase x402, GitHub Actions cron, Composio webhook log.
- **Money**: $0.50 teaser-upgrade / $2–8 full 3h drop. Repeat use is the product.
- **TTFD**: 24–48h if wallet already exists.
- **Feasibility 8 / Autonomy 10 / Revenue 8 / Composite 8.50**

### 2. Paid Skill Pack + License Key (botdirectory / Grok Bot Social)
- Keep. Convert current $0 installs into one gated pack that *calls* the TA MCP, not another markdown dump.
- **Money**: $9–29 pack + per-call USDC.
- **TTFD**: 24–48h after #1 exists.
- **Feasibility 9 / Autonomy 8 / Revenue 6 / Composite 8.05**

### 3. Whop One-Shot X Alpha Brief ($19)
- Demoted. Human checkout is slower than agent USDC. Keep as side SKU once TA teaser has views.
- **Feasibility 9 / Autonomy 7 / Revenue 5 / Composite 7.40**

### 4. x402 Gated Research Drop (generic markdown)
- Demoted vs TA-specific drop. Same rail, weaker hook for repeat agent calls.
- **Feasibility 7 / Autonomy 9 / Revenue 5 / Composite 7.30**

### 5. One-Creator Whop Rev-Share Operator
- Parked. Sales cycle kills 48h test. Revisit after first 10 paid MCP calls.
- **Feasibility 7 / Autonomy 6 / Revenue 8 / Composite 6.55**

## Kill / defer now
- Prompt Arsenal Pack $9–19: commodity, no agent re-use. **Kill.**
- Niche directory / botdirectory sponsored slot: still not a product.
- Full 50-bot fleet before $1: still a cost trap. Cap at 12 cores.
- Static TA landing (`Jan-Solos-Signal-Confluence`, last push Apr 2026): demote to teaser host only; do not polish HTML.
- EMR daily bots that never write outputs: pause until one paid call exists.

## 48h experiment (only one)
**Ship `ta_confluence_teaser` (free) + `ta_confluence_full` ($2 USDC x402) on one BTC/USDT 3h candle.**
1. Add tools to MCP YAML from `contracts/ta-confluence.yaml`.
2. Log every call to `analytics/mcp-calls.jsonl` via GitHub Action.
3. Post one Confluence Drop teaser on X with the free tool name.
Kill if 0 paid calls after 50 teaser invocations or 72h.
