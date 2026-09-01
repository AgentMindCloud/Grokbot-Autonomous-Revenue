# Ranked Playbooks — Grokbot Autonomous Revenue

*Updated 2026-09-01 by Tool-Feedback-Loop (still proxy; 0 live MCP receipts)*

Data (2026-08-29 → 2026-09-01): 0 paid MCP receipts, 0 USDC, 0 issues/PRs on this repo, 0 callable paid endpoint. Contract `contracts/ta-confluence.yaml` + formula exist. Grok Bot Social packs ~3–4 installs / $0. First-x402-by-Day-10 missed. Health falling because the 08-29 48h ship did not land.

Proxy call model (if teaser shipped tomorrow): 40 teaser / day, 4–8% pay, $2 full, p95 target <800ms teaser / <2500ms full.

Composite = 0.30*speed + 0.25*feasibility + 0.25*autonomy + 0.20*revenue.

---

## Top 5 (2026-09-01)

### 1. x402 TA Confluence Signal — free teaser + paid full MCP
- Still #1 but health **3.2/10**. No product until tools exist.
- **Exact steps**: Ship `ta_confluence_teaser` + `ta_confluence_full` on BTC/USDT 3h only. Log `analytics/mcp-calls.jsonl`.
- **Money**: free teaser; $2 USDC x402 full (drop $0.50 upgrade — extra SKU with 0 demand). Bundle 8 calls / $12 after first paid.
- **TTFD**: <24h now. Wallet must exist before code.
- **Feasibility 7 / Autonomy 10 / Revenue 7 / Composite 8.05**

### 2. Paid Skill Pack that *calls* TA MCP (botdirectory / Grok Bot Social)
- Keep only as wrapper after #1 has 1 paid call. Do not ship another markdown pack.
- **Money**: $9 pack + per-call USDC.
- **Feasibility 8 / Autonomy 8 / Revenue 5 / Composite 7.55**

### 3. x402 Gated 3H Drop (TA-specific, not generic research)
- Promote over Whop. Same rail as #1; reuse full payload as scheduled drop.
- **Feasibility 7 / Autonomy 9 / Revenue 5 / Composite 7.30**

### 4. Whop One-Shot X Alpha Brief ($19)
- Demoted again. Human checkout. Side SKU after 10 paid MCP calls.
- **Feasibility 9 / Autonomy 6 / Revenue 4 / Composite 6.85**

### 5. One-Creator Whop Rev-Share Operator
- Parked. Sales cycle >48h.
- **Feasibility 7 / Autonomy 6 / Revenue 7 / Composite 6.35**

## Kill / defer now
- Prompt Arsenal Pack $9–19: **killed** (no agent re-use).
- $0.50 teaser-upgrade SKU: **killed** until first $2 receipt.
- Generic x402 research markdown: **defer** vs TA-specific drop.
- Niche directory sponsored slot: not a product.
- Full 50-bot fleet before $1 USDC: **cap at 12 cores**.
- Static TA landing polish: teaser host only.
- EMR daily bots with no output file: **pause**.
- New paid MCP skills: **freeze** until TA has ≥1 paid call + call log.

## 48h experiment (only one)
**Ship teaser+full on one pair, one TF, with jsonl logging.**
1. Expand `contracts/ta-confluence.yaml` with two MCP tools (see analytics/tool-feedback-loop-2026-09-01.md).
2. GitHub Action appends every invocation to `analytics/mcp-calls.jsonl`.
3. One X Confluence Drop naming the free tool.
Kill if 0 paid after 50 teasers or 72h.
