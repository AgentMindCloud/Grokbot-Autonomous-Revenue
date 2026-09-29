# Standing decisions — CoS and Desk Canon read this before asking the human

Updated: 2026-09-28
Human is only for Red items not already decided here.

## Defaults (week 1)

| Question | Answer | Until |
|---|---|---|
| Which Frontier steals to adopt? | **Named yes only.** Adopted 2026-09-18: sku-0 canary→fix fleet. **2026-09-25 Projects+pstack: ACCEPT trial** (d-20260925-06; supersedes HOLD d-20260925-05). Caps: steal-list #1–3 only; no new bots; Buyer-only payment stays. All other steals None. | Next Friday steal-list + explicit human yes per item |
| Frontier self-hosted worker trial (`cursor agent worker start` / self-hosted machines)? | **HOLD until friday frontier list** (d-20260928-01 named). No trial. No new bots. Buyer-only pay stays. | Friday frontier list |
| Lift SKU-0 public / X / directory hold? | **No.** | 10 reconciled LAB_SELF_TEST receipts + human yes |
| Inspect-only on SKU-0? | **Cleared 2026-09-18** (Auditor: live 402 logged, $ charged = 0). Card `p-20260916-01`. | — |
| SKU-0 live seller (aggregator-beta / agent-search-pro)? | **HOLD / killed** (d-20260928-09). Human: project killed, repos gone (404). Cancel restore and vercel grant. Drop held $0.02 health canaries. No pay. No listing. No new bots. policy.yaml unchanged. | Until a new SKU-0 seller URL is named |
| Attach Payment MCP? | **Yes — Buyer Desk only** (d-20260918-04). Never attach to CoS, Seller, Lab, Governor, Canon, SKU-0 Fix. | Eggbot wires `buyer_payment_worker` |
| Run $0.02 self-canary / any pay? | **Yes — one shot only** on card `ledger/p-20260924-01-sku0-canary.md` (d-20260924-06). Governor ALLOW required. Not autopay. Key spent (d-20260924-07). | Further pays need new card |
| Standing: Buyer drafts next exact-match SKU-0 $0.02 canary cards? | **HOLD / killed** (d-20260928-09). Prior yes d-20260926-01 and ENABLE_AUTOPAY d-20260927-23 have no live seller (agent-search-pro / aggregator-beta repos gone). Do not draft or pay $0.02 health canaries. | Until a new SKU-0 seller URL is named |
| Pace / rail cascade canaries #3–#10? | **CLOSED at #10** (DEMAND_CADENCE d-20260927-22). 10/10 paid self-canaries CLEARed through p-20260927-08. Do not draft further cards from densify d-20260927-06. | Closed |
| Densify pack (research daily, hermes daily, 7d+midday CoS, Demand Radar bot, daily friction)? | **Yes** (d-20260927-06), daily chase continued by DEMAND_CADENCE d-20260927-22. Self-canary rail CLOSED. Policy cuts (autopay 5→3 / list 10→5) **HOLD — do not start.** policy.yaml unchanged. | Until human pause |
| UNLOCK p-20260926-01 canary #2? | **Yes — one shot** (d-20260926-02) on `ledger/p-20260926-01-sku0-canary.md`. Governor ALLOW required. Not autopay. | Key spent after pay |
| UNLOCK p-20260927-01 canary #3? | **Yes — one shot** (d-20260927-02) on `ledger/p-20260927-01-sku0-canary.md`. Prior CLEAR #1+#2. Governor ALLOW required. Not autopay. | Key spent after pay |
| UNLOCK p-20260927-02 canary #4? | **Yes — one shot** (d-20260927-04) on `ledger/p-20260927-02-sku0-canary.md`. Prior CLEAR #3. Governor ALLOW required. Not autopay. | Key spent after pay |
| New SKUs / TA / human clients / skill packs | **No** | Scope lock in VERIFIED.md |
| Auto-pay? | **Suspended** (d-20260928-09). ENABLE_AUTOPAY d-20260927-23 exact-match SKU-0 search $0.02 has no live seller (aggregator-beta gone). Suspended until a new seller URL is named. Not a pay. Not listing. Densify via external ticks + demand cadence only. policy.yaml unchanged. | Until a new SKU-0 seller URL is named |
| DEMAND_CADENCE | **Yes** (d-20260927-22). Demand Radar + Hermes daily chase; CoS midday+friction must fire; refresh `desk/census/_ROLLUP.md`. No new SKU. No listing. No X. Self-canary densify rail CLOSED at #10. | Until human pause |
| External one-shot tick/all? | **Yes — one card, unlocked** (EXTERNAL_ONE_SHOT d-20260927-24; UNLOCK_PAY d-20260927-25). `https://tick.hugen.tokyo/tick/all` payee `0x29322Ea7EcB34aA6164cb2ddeB9CE650902E4f60` (matches demand-radar and accepted tick d-20260925-08). Max $0.005 Base USDC; live 402 MATCH. Card `ledger/p-20260927-09-tick-all.md` `pay: true`. Governor ALLOW; Buyer pays once. Not autopay. Not lab_self_test. | One shot only |
| External one-shot tick/latest? | **Yes — one card, unlocked** (EXTERNAL_ONE_SHOT d-20260928-02; UNLOCK_PAY d-20260928-04). `https://tick.hugen.tokyo/tick/latest` payee `0x29322Ea7EcB34aA6164cb2ddeB9CE650902E4f60` (same as tick/all d-08/d-24). Max $0.005 Base USDC; no-pay 402 MATCH. Card `ledger/p-20260928-01-tick-latest.md` `pay: true`. Source demand-radar 2026-09-27. Governor ALLOW; Buyer pays once. Not autopay. Not lab_self_test. Not a pay in the decision row. | One shot only |
| External one-shot tick/symbols? | **Yes — one card, unlocked** (EXTERNAL_ONE_SHOT d-20260928-03; UNLOCK_PAY d-20260928-05). `https://tick.hugen.tokyo/tick/symbols` same payee/max/chain/asset. Card `ledger/p-20260928-02-tick-symbols.md` `pay: true`. Source demand-radar 2026-09-27. Governor ALLOW; Buyer pays once. Not autopay. Not lab_self_test. | One shot only |
| Weekly healthcheck 2026-09-28 (Frontier / Seller / Money Maker)? | **Yes** (WEEKLY_HEALTHCHECK d-20260928-06 named 2026-09-28T20:44+07). Frontier Watch pause daily/weekend → Friday-only steal-list. Seller Desk health 7d→weekdays 1-5 only. Money Maker pause/disable Quiet opportunity `0 */2 * * *`. Not a pay. No new bots. policy.yaml unchanged. | Until human pause |
| Adopt workplace bots from Watch? | **Never** | Permanent |
| Arm canary→fix fleet bot (SKU-0 Fix)? | **Yes** (d-20260918-02). Still never pay/list. | Human pause/disarm |
| Money Maker / other chat bots fund or send desk USDC? | **No** | Permanent — payment worker connector only |
| 23 Sep novel payees + kronos | **Accepted** (d-20260924-01..05). Not a pay. | Pay still needs its own card |
| HUMAN.md novel-accept batch (nansen/omni/lonestar/agentservices/glassnode/voidfeed) | **Accepted** (d-20260924-08..13). Not a pay. Must-lines cleared. | Pay still needs its own card |
| HUMAN.md novel-accept batch (celerapi/anchor/blockrun; hold glim) | **Accepted** celerapi/anchor/blockrun (d-20260925-01..03). **HOLD** glim (d-20260925-04, live 402 Solana / new_chain). Not pays. Must-lines cleared. | Pay still needs its own card; glim needs Base live 402 or named new_chain yes |
| Novel payees r-20260924-e01..e05 | **Accepted** tick/geoprimitives/base-gas/x402atlas (d-20260925-08..10,12). **HOLD** svm402 (d-20260925-11, Solana/new_chain). Supersedes skip-HOLD d-20260925-07. Not pays. | Pay still needs its own card |
| Novel payees r-20260925-d01..d05 | **Accepted** agent-commerce-factory / lionx402 / ozmium / aiagentoracle / agentmercantile (d-20260925-13..17). Not pays. Must-lines cleared. | Pay still needs its own card |
| Novel payees r-20260928-d02/d05 (m2msentinel + concordancehq) | **HOLD** (d-20260928-10, d-20260928-11 named). Not accepted. Not pays. Must-line cleared. | Until named yes ACCEPT |
| Novel payees r-20260929-d01..d04 (402signal + whaletape + straits.live + token-risk) | **HOLD** (d-20260929-12..15 named). Not accepted. Not pays. Must-line cleared. | Until named yes ACCEPT |
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
