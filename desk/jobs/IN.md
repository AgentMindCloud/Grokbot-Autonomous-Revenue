# HERMES IN — demand radar (daily)
Work folder: C:\\Users\\louis\\Documents\\Grokbot-Autonomous-Revenue
Models: kimi-k3:cloud for tools, qwen3.5:9b for JSON, gemma4:12b for review.
Cadence: **every day** when PC awake (densify d-20260927-06). Goal: external fills / live-402 candidates that unlock listing (self-canaries alone never will).

Each run:
1. git pull
2. GET https://aggregator-beta.vercel.app/health + latency
3. Scan CDP Bazaar + MPP for endpoints with **live 402**. Prefer payees already in ledger/decisions.jsonl. Flag any with fills_seen > 0 or strong external demand signals.
4. For each candidate write one research.jsonl line: id, ts, source, endpoint, payee, chain, asset, listed_usd, live_402_usd if fetched, fills_seen (0 if unknown), class live|spec|thin|hype, note
5. Do not treat listed price as live. Do not pay.
6. Write desk/jobs/OUT.md hermes_last_seen + one paragraph (lead with external-fill / demand hits)
7. Append desk/census/local-eod.md one line
8. Patch only hermes_last_seen in desk/queue/HUMAN.md
9. git add those files, commit hermes: radar, push if changed

Forbidden: policy.yaml, purchases.jsonl, receipts.jsonl, pay, list, post, 50-bot-system.
