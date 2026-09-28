# HUMAN QUEUE
updated: 2026-09-28T09:05:00+07:00
hermes_last_seen: 2026-09-26T13:27:00+07:00

## must
- [ ] weekly-healthcheck: Frontier Watch — pause daily/weekend frontier-watch-daily; keep Friday-only steal-list (FLEET Fri-only; cards still 7d incl Sat/Sun). named yes. (eggbot 2026-09-28)
- [ ] weekly-healthcheck: Seller Desk — seller-desk-daily-health 7d→weekdays 1-5 only. named yes. (eggbot 2026-09-28; open since 2026-09-21)
- [ ] weekly-healthcheck: Money Maker Bot — pause/disable Quiet opportunity `0 */2 * * *` leftover (parked; AUTOMATIONS forbids 2h loop). named yes or bot self-pause. (eggbot 2026-09-28)
- [ ] Frontier self-hosted worker trial — `cursor agent worker start` / self-hosted machines (desk/cards/2026-09-28-watch.md USAGE #1). named yes required; no new bots; Buyer-only pay stays. (frontier-watch 2026-09-28)
- [x] Paste desk/HERMES.md into Hermes and run demand radar (human: done 2026-09-26)
- [x] Archive leftover 50-bot-system → archive/50-bot-system/ (14 files; commit 58a2067; README says do not revive)
- [x] Keep Grok Task notify OFF; keep ledger-push paused (standing)
- [x] Lab scorecard on rc-20260924-01 — already filed t-20260924-01 q=0.9 hold scale
- [x] Frontier Friday steal Projects+pstack — ACCEPT trial d-20260925-06 (named yes; supersedes HOLD d-05; no new bots; Buyer-only pay)
- [x] Novel payees r-20260924-e01..e05 — ACCEPT tick/geo/base-gas/x402atlas d-08..10,12; HOLD svm402 d-11 (named yes; not pays)
- [x] Standing Buyer draft exact-match SKU-0 $0.02 canary cards — d-20260926-01 (named yes; not autopay)
- [x] Novel payees r-20260925-d01..d05 — ACCEPT agent-commerce-factory/lionx402/ozmium/aiagentoracle/agentmercantile d-13..17 (named yes; not pays)
- [x] Densify pack — d-20260927-06 (named yes; research daily; hermes daily; 7d+midday cos; Demand Radar via Eggbot; daily friction; policy cuts HOLD). Self-canary rail CLOSED 10/10.
- [x] DEMAND_CADENCE — d-20260927-22 (named yes; Demand Radar + Hermes daily chase; CoS midday+friction must fire; refresh census/_ROLLUP; no new SKU; no listing; no X; densify rail CLOSED at #10)
- [x] ENABLE_AUTOPAY — d-20260927-23 (named yes; exact-match SKU-0 search $0.02 only, same as p-20260924-01; gate 5 clean met, now 10/10; caps apply; not novel; not listing; Governor may ALLOW without per-shot CoS unlock; Buyer once per key; Auditor CLEARs)
- [x] EXTERNAL_ONE_SHOT tick/all — d-20260927-24 (named yes; ONE card https://tick.hugen.tokyo/tick/all; payee 0x29322Ea7EcB34aA6164cb2ddeB9CE650902E4f60 verified vs demand-radar and d-20260925-08; max $0.005 Base USDC; not autopay)
- [x] UNLOCK_PAY p-20260927-09 — d-20260927-25 (one-shot; card pay:true; Buyer pays once after Governor ALLOW; NOT autopay; NOT lab_self_test; not a pay in the decision row)

## running
- Demand cadence (d-20260927-22): Demand Radar + Hermes daily chase; CoS midday+friction must fire; refresh census/_ROLLUP; no new SKU; no listing; no X
- Densify self-canary rail CLOSED 10/10 (p-20260927-08 CLEAR). Do not cascade further cards from d-20260927-06.
- Auto-pay standing (d-20260927-23): exact-match SKU-0 search $0.02 only. Governor may ALLOW health canaries without per-shot CoS unlock. Buyer pays once per key. Auditor CLEARs.
- External one-shot UNLOCKED d-20260927-25: ledger/p-20260927-09-tick-all.md pay:true. Buyer pays once after Governor ALLOW. This queue does not pay.
- Daily: research Poteto→Super Intel→Compound
- Demand Radar live: cards → CoS; never pays
- Other demand-radar paths are not standing pays (tick/latest, tick/symbols, blockrun events, nansen current-balance, x402atlas /trend). No new SKU. No listing.
- Frontier trial: Projects+pstack capped per d-20260925-06
- weekly-healthcheck open: see desk/status/weekly-healthcheck-2026-09-28.md

## parked
Money Maker, Agent Zero, X Growth Coach
