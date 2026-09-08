# Tool Feedback Loop — 2026-09-08

**Data class:** proxy. Still 0 `mcp-calls.jsonl` rows and 0 issues/PRs on paid skills. Rail probed live today.

Probe 2026-09-08 15:32 UTC:
- GET /health 200, mock=false, v0.2.0, facilitator=xpay
- tiers: free $0 / search $0.02 / synthesis $0.10
- /.well-known/x402.json resources: /api/search $0.02, /api/synthesis $0.10 USD
- 48h demand experiment from 2026-09-04 **still not done** (no jsonl, no listing proof)
- Last claimed dogfood: 0.02 USDC (unverified on-chain in this loop)

## 1. Health (1–10)

| skill | score | why |
|-------|------:|-----|
| Agent Search Pro (live paid MCP) | **5.2** | Product+rail work. Volume ~0. Reuse 0. Demand experiment missed 4 days. |
| TA Confluence Signal (YAML stub) | **2.4** | No public URL, 0 calls. Keep demoted. Do not copy settlement yet. |

Fleet paid-skill health: **3.8/10** (down from 4.2 on 09-03 — host is fine; demand execution failed).

Kill/demote: TA as a paid SKU this week. New MCP skills. $2 / $0.50 prices. Prompt Arsenal.

## 2. Top 3 improvements (retention / repeat USDC)

1. **Instrument before sell.** Add `analytics/mcp-calls.jsonl` + one-line append in agent-search-pro on every tools/call and /api/* (fields: ts, tool, paid, ms, agent_id, usdc, http). Without this, agents cannot be optimized and we cannot prove reuse.
2. **Free taste that agents can curl with no wallet.** Keep `web_search_sample` as the only public teaser. Pin exact curl in README + one X post. Do not change $0.02/$0.10.
3. **Distribution, not product.** List the same URL on grokbot.money + botdirectory.ai + Grok Bot Social. Do not ship a $9 pack until paid_calls≥1 from a non-self agent_id.

No price tweak. No TA YAML edit.

## 3. Updated ranking for RANKED-PLAYBOOKS.md

See companion commit on RANKED-PLAYBOOKS.md (2026-09-08).
#1 demand the live search-pro URL. #5 TA stays demoted. Composite weights unchanged.

## 4. Single best next experiment (<48h)

Ship the **missed** 09-04 experiment. Nothing else.

1. Commit empty+schema `analytics/mcp-calls.jsonl`.
2. One X post: free sample curl + “agents pay $0.02 USDC on Base for full search”.
3. List aggregator-beta.vercel.app on grokbot.money, botdirectory.ai, Grok Bot Social.
4. Do not touch TA. Do not change prices.

Kill if 0 non-self paid after 50 teasers or 72h from the post.

## 5. Metrics tomorrow

- public_url_up (health 200, mock=false)
- teaser_calls, paid_calls, unique_agent_id (non-self)
- usdc_settled (Base)
- p95_ms teaser vs 402 vs paid
- error_rate / 402_without_retry
- listings_live (3 surfaces)
- jsonl_rows_appended
