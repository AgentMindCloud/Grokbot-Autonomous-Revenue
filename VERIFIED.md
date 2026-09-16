# VERIFIED — Market Desk freeze point

Date: 2026-09-16
Source: repo state + Master Synthesis 2026-09-15 + LOOP-TEST log
Rule: only facts below are treated as true. Ranked playbooks are hypotheses.

## Live seller

- URL: https://aggregator-beta.vercel.app
- Health: 200, mock=false, v0.2.0 (confirmed 2026-09-14 and 2026-09-15)
- Tiers: $0.02 search / $0.10 synthesis, Base USDC
- Probe: POST /mcp web_search returns HTTP 402
- Sample: GET /api/sample 200 (2026-09-14)

## Not true yet

- `analytics/mcp-calls.jsonl` did not exist as of 2026-09-15
- 0 paid rows recorded in this repo
- No listing on botdirectory.ai or grokbot.money as of 2026-09-15
- X teaser + 48h demand experiment: unshipped since 2026-09-04
- No on-chain dogfood receipt filed here
- First non-self paid call: has not happened

## LOOP-TEST

- #1 PASS + AUDIT CONFIRMED (2026-09-14): infra live, jsonl missing
- #2 PASS + AUDIT CONFIRMED (2026-09-15): tiers live, jsonl missing, no public listing

## Scope lock (2026-09-16)

This repo is now the **A2A Market Desk** control plane.

Out of scope: workplace bots, X growth fleet, human $200–1k clients, TA confluence SKU, 50-bot hierarchy, Whop, skill packs before a reconciled receipt.

In scope: discover, inspect, buy/sell under cap, score fulfillment, compound.

## SKU-0

`agent-search-pro` on aggregator-beta is the existing seller endpoint.
It stays private until:

1. mcp-calls.jsonl exists and is appended on every call
2. Lab self-canary tagged LAB_SELF_TEST is reconciled by Auditor
3. Human approves any public listing or X teaser

Do not rebuild the endpoint. Do not count self-tests as demand.
