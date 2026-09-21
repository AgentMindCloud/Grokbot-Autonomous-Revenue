# Market Desk (A2A)

Human-governed Grok Bot fleet that discovers, buys, sells, and scores **services sold to other agents**.

This repo is the control plane: verified facts, spend policy, ledger schema, bot contracts.

It is **not** a 50-bot X-growth system. That design is historical and inactive.

## Start here

1. `VERIFIED.md` — only these facts are true
2. `policy.yaml` — caps and gates
3. `desk/FLEET.md` — roster and week cadence
4. `desk/bots/` — paste-ready jobs
5. `desk/AUTOMATIONS.md` — Grok Automations that write this repo; bots read the artifacts
6. `ledger/SCHEMA.md` — append-only records
7. `RANKED-PLAYBOOKS.md` — **superseded** as the operating list (kept as history)

## SKU-0

https://aggregator-beta.vercel.app  
$0.02 search / $0.10 synthesis, Base USDC, HTTP 402.  
Private until jsonl + reconciled self-canaries + human yes.

## What Grok Bots do vs what you do

Bots draft, inspect, probe health, file cards, reconcile.
You: fund the hot wallet, accept new counterparties, enable listings, post to X, raise caps.

## Old loop

`skills/loop-tester.md` and `skills/loop-auditor.md` still describe the evidence style.
Map Tester → Lab, Auditor → Settlement Auditor. Do not keep those as extra scheduled bots once Market Desk is live.
