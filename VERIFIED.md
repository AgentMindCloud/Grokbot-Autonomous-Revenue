# VERIFIED — Market Desk 2026-09-25

Rule: only facts below are treated as true.

## Mission
Find products **other agents pay for** (Base USDC / x402). SKU-0 is the rail, not the company.

Three fronts:
1. Rail — inspect, pay under cap, receipt, score
2. Demand radar — who got paid on-chain / live 402 fills, not catalog listings
3. Gap build — at most one new SKU after radar shows external repeat spend

## Live seller (SKU-0)
- URL: https://aggregator-beta.vercel.app
- Health: 200, mock=false, v0.2.0
- Tiers: $0.02 search / $0.10 synthesis, Base USDC
- Public: false until 10 reconciled LAB_SELF_TEST + 5 external paid calls + human yes

## Money facts
- First self-canary PAID 2026-09-24: card p-20260924-01, receipt rc-20260924-01, tx 0x126454b6fdbd9691bf62cc6b7578ceee72882024b8aaf5283818b025da933d71, $0.02 USDC Base, lab_self_test. Not revenue.
- Buyer worker: 0xB56Bf6B023E94D2059Da1F86b70A90b73333C15B (Base)
- Caps: $0.25/call, $5/session, $10/day, hot $25. No autopay.
- ledger-push-cos-note GitHub trigger: PAUSED (commit loop).

## Out of scope unless human names a front-3 card
Workplace bots, X-growth fleet, 50-bot hierarchy, Whop, TA confluence SKU, skill packs as products.

## Do not count as demand
Any lab_self_test / SKU-0 self-pay.
