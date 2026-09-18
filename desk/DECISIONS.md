# Standing decisions — CoS and Desk Canon read this before asking the human

Updated: 2026-09-18
Human is only for Red items not already decided here.

## Defaults (week 1)

| Question | Answer | Until |
|---|---|---|
| Which Frontier steals to adopt? | **Named yes only.** Adopted 2026-09-18: sku-0 canary→fix fleet. All other steals None. | Next Friday steal-list + explicit human yes per item |
| Lift SKU-0 canary hold? | **No for public / X / directories.** | 10 reconciled LAB_SELF_TEST receipts + human yes |
| Run inspect-only on SKU-0? | **Yes.** Card `p-20260916-01` = HTTP 402 probe. **No wallet. No Payment MCP. No pay.** | Done when Auditor logs live 402 fields and $ charged = 0 |
| Ask for / attach Payment MCP? | **No** while inspect-only. Do not nag for `buyer_payment_worker`. | After Auditor clears inspect ($ charged = 0): ask human **once** — lift inspect-only and attach Payments MCP to **Buyer Desk only**? Never attach to CoS, Seller, Lab, Governor, Canon, SKU-0 Fix |
| Run $0.02 self-canary? | **No** until inspect card is complete and Auditor says fields match | Then human yes on a new pay card |
| New SKUs / TA / human clients / skill packs | **No** | Scope lock in VERIFIED.md |
| Auto-pay? | **No** | 5 clean canaries on exact seller+sku+chain+asset |
| Adopt workplace bots from Watch? | **Never** | Permanent |
| Arm canary→fix fleet bot (SKU-0 Fix)? | **Yes** (armed 2026-09-18 via d-20260918-02). Still never pay/list. | Human pause/disarm |
| Money Maker / other chat bots fund or send desk USDC? | **No** | Permanent — payment worker connector only |

## Who answers who

Specialists ask **Desk Canon** for policy facts.
Desk Canon cites the repo. It does not assign work.
**Market CoS** routes work and builds the queue using Canon's answers.
Human only if Canon returns UNKNOWN.

## If Canon / CoS is unsure

Output:
1. Recommended default from this table
2. Source path
3. One yes/no for the human only when the table says human yes
