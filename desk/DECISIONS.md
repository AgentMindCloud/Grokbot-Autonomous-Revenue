# Standing decisions — CoS and Desk Canon read this before asking the human

Updated: 2026-09-27
Human is only for Red items not already decided here.

## Defaults (week 1)

| Question | Answer | Until |
|---|---|---|
| Which Frontier steals to adopt? | **Named yes only.** Adopted 2026-09-18: sku-0 canary→fix fleet. **2026-09-25 Projects+pstack: ACCEPT trial** (d-20260925-06; supersedes HOLD d-20260925-05). Caps: steal-list #1–3 only; no new bots; Buyer-only payment stays. All other steals None. | Next Friday steal-list + explicit human yes per item |
| Lift SKU-0 public / X / directory hold? | **No.** | 10 reconciled LAB_SELF_TEST receipts + human yes |
| Inspect-only on SKU-0? | **Cleared 2026-09-18** (Auditor: live 402 logged, $ charged = 0). Card `p-20260916-01`. | — |
| Attach Payment MCP? | **Yes — Buyer Desk only** (d-20260918-04). Never attach to CoS, Seller, Lab, Governor, Canon, SKU-0 Fix. | Eggbot wires `buyer_payment_worker` |
| Run $0.02 self-canary / any pay? | **Yes — one shot only** on card `ledger/p-20260924-01-sku0-canary.md` (d-20260924-06). Governor ALLOW required. Not autopay. Key spent (d-20260924-07). | Further pays need new card |
| Standing: Buyer drafts next exact-match SKU-0 $0.02 canary cards? | **Yes** (d-20260926-01). Exact match only: same seller/sku/endpoint/payee/chain/asset as p-20260924-01; max $0.02; live 402; lab_self_test. Not novel payees. Exact-match health canaries: ENABLE_AUTOPAY d-20260927-23 (Governor ALLOW without per-shot CoS unlock; Buyer pays once per key; Auditor CLEARs). | Until human pause |
| Pace / rail cascade canaries #3–#10? | **CLOSED at #10** (DEMAND_CADENCE d-20260927-22). 10/10 paid self-canaries CLEARed through p-20260927-08. Do not draft further cards from densify d-20260927-06. | Closed |
| Densify pack (research daily, hermes daily, 7d+midday CoS, Demand Radar bot, daily friction)? | **Yes** (d-20260927-06), daily chase continued by DEMAND_CADENCE d-20260927-22. Self-canary rail CLOSED. Policy cuts (autopay 5→3 / list 10→5) **HOLD — do not start.** policy.yaml unchanged. | Until human pause |
| UNLOCK p-20260926-01 canary #2? | **Yes — one shot** (d-20260926-02) on `ledger/p-20260926-01-sku0-canary.md`. Governor ALLOW required. Not autopay. | Key spent after pay |
| UNLOCK p-20260927-01 canary #3? | **Yes — one shot** (d-20260927-02) on `ledger/p-20260927-01-sku0-canary.md`. Prior CLEAR #1+#2. Governor ALLOW required. Not autopay. | Key spent after pay |
| UNLOCK p-20260927-02 canary #4? | **Yes — one shot** (d-20260927-04) on `ledger/p-20260927-02-sku0-canary.md`. Prior CLEAR #3. Governor ALLOW required. Not autopay. | Key spent after pay |
| New SKUs / TA / human clients / skill packs | **No** | Scope lock in VERIFIED.md |
| Auto-pay? | **Yes — exact SKU-0 search $0.02 only** (ENABLE_AUTOPAY d-20260927-23). Same seller/sku/endpoint/payee/chain/asset as p-20260924-01. Policy gate 5 clean met (now 10/10). Caps still apply. Not novel. Not listing. Governor may ALLOW exact-match health canaries without per-shot CoS unlock; Buyer pays once per key; Auditor CLEARs. | Until human pause |
| DEMAND_CADENCE | **Yes** (d-20260927-22). Demand Radar + Hermes daily chase; CoS midday+friction must fire; refresh `desk/census/_ROLLUP.md`. No new SKU. No listing. No X. Self-canary densify rail CLOSED at #10. | Until human pause |
| External one-shot tick/all? | **Yes — one card, unlocked** (EXTERNAL_ONE_SHOT d-20260927-24; UNLOCK_PAY d-20260927-25). `https://tick.hugen.tokyo/tick/all` payee `0x29322Ea7EcB34aA6164cb2ddeB9CE650902E4f60` (matches demand-radar and accepted tick d-20260925-08). Max $0.005 Base USDC; live 402 MATCH. Card `ledger/p-20260927-09-tick-all.md` `pay: true`. Governor ALLOW; Buyer pays once. Not autopay. Not lab_self_test. | One shot only |
| Adopt workplace bots from Watch? | **Never** | Permanent |
| Arm canary→fix fleet bot (SKU-0 Fix)? | **Yes** (d-20260918-02). Still never pay/list. | Human pause/disarm |
| Money Maker / other chat bots fund or send desk USDC? | **No** | Permanent — payment worker connector only |
| 23 Sep novel payees + kronos | **Accepted** (d-20260924-01..05). Not a pay. | Pay still needs its own card |
| HUMAN.md novel-accept batch (nansen/omni/lonestar/agentservices/glassnode/voidfeed) | **Accepted** (d-20260924-08..13). Not a pay. Must-lines cleared. | Pay still needs its own card |
| HUMAN.md novel-accept batch (celerapi/anchor/blockrun; hold glim) | **Accepted** celerapi/anchor/blockrun (d-20260925-01..03). **HOLD** glim (d-20260925-04, live 402 Solana / new_chain). Not pays. Must-lines cleared. | Pay still needs its own card; glim needs Base live 402 or named new_chain yes |
| Novel payees r-20260924-e01..e05 | **Accepted** tick/geoprimitives/base-gas/x402atlas (d-20260925-08..10,12). **HOLD** svm402 (d-20260925-11, Solana/new_chain). Supersedes skip-HOLD d-20260925-07. Not pays. | Pay still needs its own card |
| Novel payees r-20260925-d01..d05 | **Accepted** agent-commerce-factory / lionx402 / ozmium / aiagentoracle / agentmercantile (d-20260925-13..17). Not pays. Must-lines cleared. | Pay still needs its own card |
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
