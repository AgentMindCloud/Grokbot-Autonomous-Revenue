# Standing decisions — CoS and Desk Canon read this before asking the human

Updated: 2026-09-25
Human is only for Red items not already decided here.

## Defaults (week 1)

| Question | Answer | Until |
|---|---|---|
| Which Frontier steals to adopt? | **Named yes only.** Adopted 2026-09-18: sku-0 canary→fix fleet. All other steals None. | Next Friday steal-list + explicit human yes per item |
| Lift SKU-0 public / X / directory hold? | **No.** | 10 reconciled LAB_SELF_TEST receipts + human yes |
| Inspect-only on SKU-0? | **Cleared 2026-09-18** (Auditor: live 402 logged, $ charged = 0). Card `p-20260916-01`. | — |
| Attach Payment MCP? | **Yes — Buyer Desk only** (d-20260918-04). Never attach to CoS, Seller, Lab, Governor, Canon, SKU-0 Fix. | Eggbot wires `buyer_payment_worker` |
| Run $0.02 self-canary / any pay? | **Yes — one shot only** on card `ledger/p-20260924-01-sku0-canary.md` (d-20260924-06). Governor ALLOW required. Not autopay. Key spent (d-20260924-07). | Further pays need new card |
| New SKUs / TA / human clients / skill packs | **No** | Scope lock in VERIFIED.md |
| Auto-pay? | **No** | 5 clean canaries on exact seller+sku+chain+asset |
| Adopt workplace bots from Watch? | **Never** | Permanent |
| Arm canary→fix fleet bot (SKU-0 Fix)? | **Yes** (d-20260918-02). Still never pay/list. | Human pause/disarm |
| Money Maker / other chat bots fund or send desk USDC? | **No** | Permanent — payment worker connector only |
| 23 Sep novel payees + kronos | **Accepted** (d-20260924-01..05). Not a pay. | Pay still needs its own card |
| HUMAN.md novel-accept batch (nansen/omni/lonestar/agentservices/glassnode/voidfeed) | **Accepted** (d-20260924-08..13). Not a pay. Must-lines cleared. | Pay still needs its own card |
| HUMAN.md novel-accept batch (celerapi/anchor/blockrun; hold glim) | **Accepted** celerapi/anchor/blockrun (d-20260925-01..03). **HOLD** glim (d-20260925-04, live 402 Solana / new_chain). Not pays. Must-lines cleared. | Pay still needs its own card; glim needs Base live 402 or named new_chain yes |
| Who may message the human? | **Market CoS only.** Never ping unless Settlement Auditor wrote CLEAN or FAIL on a **new** ledger file, or `desk/queue/HUMAN.md` has a **new** must-line. Max one message per event. No widgets unless Red. Specialists write the repo or message CoS — never the human. NONE is valid. | Permanent (NOTIFY RULE 2026-09-24) |

## Who answers who

Specialists ask **Desk Canon** for policy facts.
Desk Canon cites the repo. It does not assign work.
**Market CoS** routes work and builds the queue using Canon's answers.
Human only if Canon returns UNKNOWN — and only under the NOTIFY RULE above.

## If Canon / CoS is unsure

Output:
1. Recommended default from this table
2. Source path
3. One yes/no for the human only when the table says human yes **and** the NOTIFY RULE gate is met
