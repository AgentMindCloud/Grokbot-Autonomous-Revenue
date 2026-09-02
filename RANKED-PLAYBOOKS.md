# Ranked Playbooks — Grokbot Autonomous Revenue

*Updated 2026-09-02 by Tool-Feedback-Loop (proxy; 0 live MCP receipts)*

Data (2026-08-29 → 2026-09-02): 0 paid MCP receipts, 0 USDC, 0 issues/PRs, 0 callable paid endpoint. Contract `contracts/ta-confluence.yaml` already lists teaser+full. Social packs ~3–4 installs / $0. First-x402-by-Day-10 missed. 08-29 and 09-01 48h ships did not land. Health **3.0/10** (was 3.2).

Proxy if teaser ships tomorrow: 40 teaser/day, 4–8% pay, $2 full, p95 <800ms teaser / <2500ms full.

Composite = 0.30*speed + 0.25*feasibility + 0.25*autonomy + 0.20*revenue.

---

## Top 5 (2026-09-02)

### 1. x402 TA Confluence Signal — free teaser + paid full MCP
- Still #1. Health **3.0/10**. Contract exists; runtime does not. Do not design more YAML.
- **Exact steps**: Implement `ta_confluence_teaser` + `ta_confluence_full` for BTC/USDT 3h only. Append every call to `analytics/mcp-calls.jsonl`. Wallet on Base USDC before first full call.
- **Money**: free teaser; $2 USDC x402 full. After first paid receipt only: bundle 8 calls / $12. No $0.50 SKU.
- **TTFD**: <24h. Kill if 0 paid after 50 teasers or 72h live.
- **Feasibility 6 / Autonomy 10 / Revenue 7 / Composite 7.75** (feasibility down: two missed ships).

### 2. Paid Skill Pack that *calls* TA MCP (botdirectory / Grok Bot Social)
- Wrapper only after #1 has ≥1 paid call. No more markdown packs.
- **Money**: $9 pack + per-call USDC.
- **Feasibility 8 / Autonomy 8 / Revenue 5 / Composite 7.55**

### 3. x402 Gated 3H Drop (TA-specific)
- Same rail as #1. Reuse full payload as scheduled drop. Not Whop-first.
- **Feasibility 7 / Autonomy 9 / Revenue 5 / Composite 7.30**

### 4. Whop One-Shot X Alpha Brief ($19)
- Demoted. Human checkout. Side SKU after 10 paid MCP calls.
- **Feasibility 9 / Autonomy 6 / Revenue 4 / Composite 6.85**

### 5. One-Creator Whop Rev-Share Operator
- Parked. Sales cycle >48h.
- **Feasibility 7 / Autonomy 6 / Revenue 7 / Composite 6.35**

## Kill / defer now
- Prompt Arsenal Pack $9–19: **killed** (no agent re-use).
- $0.50 teaser-upgrade SKU: **killed** until first $2 receipt.
- Generic x402 research markdown: **defer**.
- New paid MCP skills: **freeze** until TA has ≥1 paid call + jsonl.
- Full 50-bot fleet before $1 USDC: **cap at 12 cores**.
- EMR daily bots with no output file: **pause**.
- Extra pairs/TFs before BTC 3h works: **killed**.

## 48h experiment (only one)
**Ship a live stub that logs, then swap in real scores.**
1. Host two MCP tools matching `contracts/ta-confluence.yaml` (even if score table is rule-based stub).
2. x402 gate on `ta_confluence_full` @ $2 USDC Base.
3. Every invocation → `analytics/mcp-calls.jsonl` (ts, tool, agent_id, paid, latency_ms, error).
4. One X Confluence Drop naming the free tool URL.
Kill if 0 paid after 50 teasers or 72h.
