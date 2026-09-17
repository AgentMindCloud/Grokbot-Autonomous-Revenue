# Market Desk group chats (max 6 members each)

Assume the cap is 6 including you. That is 5 bots + you per room.
If the cap is 6 bots plus you, add Lab to Command.

Do not put eggbot in either room.

## Room 1 — Market Command

Members: you, Market CoS, Desk Canon, Buyer Desk, Settlement Auditor, Spend Governor

Pin:

```
Room: Market Command. Repo: AgentMindCloud/Grokbot-Autonomous-Revenue.
Sources: VERIFIED.md, policy.yaml, desk/DECISIONS.md.

You = human. Speak last.
@Desk Canon = policy facts from repo only
@Market CoS = queue only, after Canon answers
@Buyer Desk = inspect/pay only with a Purchase Card
@Settlement Auditor = recon
@Spend Governor = ALLOW/DENY vs policy.yaml

Week-1: no Frontier steals, SKU-0 public HOLD, inspect-only YES, pay NO.
Human ping only if Canon says UNKNOWN.
NONE is valid. Do not invent work.
```

First work message:

```
@Desk Canon confirm next step is p-20260916-01 inspect-only.
@Buyer Desk if Canon says yes, run ledger/p-20260916-01-sku0-inspect.md. No pay.
@Settlement Auditor check the inspect output. No charge allowed.
```

## Room 2 — Market Intel

Members: you, Market CoS, Desk Canon, Protocol Scout, Frontier Watch, Seller Desk

Pin:

```
Room: Market Intel. Repo: AgentMindCloud/Grokbot-Autonomous-Revenue.
No payments in this room.

@Protocol Scout = bazaar/protocol diffs + SKU-0 health backup
@Frontier Watch = method cards only, no adopt
@Seller Desk = SKU-0 /health only. No listing. No X.
@Desk Canon = policy
@Market CoS = file cards onto the Command queue. Do not execute buys here.

Steals stay NONE until Friday list + human named yes.
```

## Who lives in DMs

- Lab — you or CoS forwards a scored artifact into Command after a canary
- dr eggbot — design only, never money

If a sixth bot seat opens in Command, add Lab.

## Routing

Intel results → CoS one-liner in Command.
Policy fight → Canon in the room where the question appeared.
Pay path exists only in Command.
