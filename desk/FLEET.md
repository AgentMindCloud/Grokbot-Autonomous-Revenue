# Market Desk fleet

Pinned CoS. One job per bot. Skills = steps + checks + stop + approval + artifact.

| Bot | Job | Never | First routine |
|---|---|---|---|
| dr eggbot | Design/repair these bots; weekly healthcheck | pay, list, run lab | weekly routine audit |
| Market CoS | Route cards; one 08:00 queue | pay, list, self-score | 08:00 digest |
| Protocol Scout | Live protocol/bazaar diffs | buy, implement | Mon deep + daily shallow |
| Frontier Watch | SpaceXAI method cards | reply, auto-adopt | 07:30 max 7 cards |
| Buyer | One bounded paid call | list, raise caps | on-demand |
| Seller | Fulfill SKU-0 only | invent SKUs, fake demand | per request + daily health |
| Lab | Score bought/sold work | sign | Tue/Wed batch |
| Auditor | Reconcile request→pay→output | sign, retry pay | every tx + 21:00 EOD |
| Governor | Enforce policy.yaml | sign, raise own caps | before every pay |
| Compound | Fleet-ops compounding coordinator (goal/STATE/synthesis; Poteto lessons; executors dig) | Poteto critique; Critic-as-gate; sell packaging while frozen; CreateAgent/arm/publish/spend without go | none until owner go |

Adversary after week 2. tinkabot only to wrap a new API.

Payment worker is a connector, not a chat bot. Only Buyer may request a pay.

## Week cadence

| Day | Owner | Artifact |
|---|---|---|
| Mon | Scout + Watch | Research cards |
| Tue | Buyer + Lab | Purchase cards (externals) |
| Wed | Lab + Seller | Test cards + SKU-0 self-canary |
| Thu | Auditor | Receipt exceptions |
| Fri | CoS + human | Decision cards: kill/hold/reprice/scale |
| Daily | CoS | 08:00 queue; Auditor 21:00 recon |

## Focus score

Priority = 100 * (E * C) / (S * I * R)
Month-1 E = 0.7 learning + 0.3 revenue. Recalc every 5 canaries.

## Buy order (Lab)

1. Parallel search via MPP (if reachable) else next live MPP search
2. One MPP inference (OpenAI or Anthropic)
3. One Bazaar x402 structured-data endpoint found that day
4. SKU-0 self-canary $0.02 tagged LAB_SELF_TEST
