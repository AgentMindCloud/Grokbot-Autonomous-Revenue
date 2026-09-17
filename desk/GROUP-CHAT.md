# Market Desk group chat

Name: Market Desk
Members: Market CoS, Desk Canon, Protocol Scout, Frontier Watch, Buyer Desk, Seller Desk, Lab, Settlement Auditor, Spend Governor
Do not add dr eggbot (builder stays outside the money room)
Do not add a payment worker personality

## Standing orders (pin this as the first message)

```
This chat is Market Desk. Repo: AgentMindCloud/Grokbot-Autonomous-Revenue.
Sources: VERIFIED.md, policy.yaml, desk/DECISIONS.md, desk/FLEET.md.

Who speaks
- Specialists post results only. No policy debates.
- Policy / "what should we do" → @Desk Canon
- After Canon answers → @Market CoS files the queue line
- Money inspect/pay → @Buyer Desk only after a Purchase Card
- Health of SKU-0 → @Seller Desk
- Score quality → @Lab
- Did pay match output → @Settlement Auditor
- Allowed or not → @Spend Governor
- Human is only pinged when Canon says UNKNOWN

Rules
- One topic per message. Name the artifact (card id or file).
- Default answer if unsure: @Desk Canon
- Do not ask the human open questions Canon can answer
- No X posts, listings, new SKUs, TA, or human-client work
- No payment talk without a Purchase Card
- NONE is a valid scheduled result — do not invent work
- Week-1 defaults: no Frontier steals, SKU-0 public hold stays, inspect-only yes, pay no
```

## How a question should look

Specialist:
```
@Desk Canon SKU-0: lift canary hold for public listing?
```

Desk Canon:
```
No. Public/X/directories stay HOLD until 10 reconciled LAB_SELF_TEST receipts + human yes.
Source: desk/DECISIONS.md
```

Market CoS:
```
Logged. Queue: keep SKU-0 private. Next: Buyer inspect p-20260916-01 only.
```

## How work should look

CoS:
```
@Buyer Desk run ledger/p-20260916-01-sku0-inspect.md inspect only. No pay.
```

Buyer posts the 402 fields.
```
@Settlement Auditor confirm no charge and fields complete.
@Desk Canon any hold left after this inspect?
```

## Anti-pattern

Do not use this chat for eggbot redesign, X drafts, or general research essays.
Those stay in DMs with the owning bot.
