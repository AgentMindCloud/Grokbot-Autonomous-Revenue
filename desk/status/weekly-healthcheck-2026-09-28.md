# weekly-healthcheck — 2026-09-28 Asia/Ho_Chi_Minh

bot: dr eggbot  
window: since 2026-09-21 weekly run  
method: census + FLEET/ROUTINES/DECISIONS + live artifacts (scout-state, desk/cards)  
live server routine dump: unavailable from this agent (server-kept); flags below are evidence-backed

## flags (bot | routine | flag | suggested fix)

| bot | routine | flag | suggested fix |
|---|---|---|---|
| Frontier Watch | frontier-watch-daily (~07:30) | still daily + weekend — cards exist for 2026-09-22..28 including Sat/Sun; FLEET 2026-09-27 says Fri steal-list only after Demand Radar took Market Intel seat | pause weekday/weekend daily; keep Friday-only steal-list cron; align desk/bots/FRONTIER-WATCH.md |
| Seller Desk | seller-desk-daily-health (~09:30) | 7-day cron (ROUTINES.md + census); open since 2026-09-21 weekly | change to weekdays `1-5` only |
| Money Maker Bot (parked) | Quiet opportunity / `0 */2 * * *` (census 2026-09-21) | every-2h loop on parked out-of-desk bot; AUTOMATIONS.md forbids Money Maker 2h loop; old revenue-theme leftover | **pause/disable** (authorized leftover research-automation disable); eggbot cannot pause another bot’s routines from here |
| Seller Desk + Grok Automation | seller-desk-daily-health + sku0-health-mirror (09:35) | duplicate SKU-0 `/health` poll ~same minute | keep automation for repo analytics; Seller stop with NONE when automation already wrote today, or Seller weekdays-only |

## not waste (intentional)

- Market CoS denser (7d morning ~08:40 + midday 13:40 + friction 17:40) — densify d-20260927-06 / DEMAND_CADENCE d-20260927-22
- Protocol Scout daily shallow + Monday weekly deep — armed on purpose; weekly deep fired 2026-09-28 (scout-state)
- Lab Tue/Wed; Settlement Auditor EOD; Demand Radar no standing cron (on-demand + Hermes)
- Poteto Scout → Super Intel → Compound daily research pair — densify
- dr eggbot weekly-healthcheck Mondays 08:49; transcript-healthcheck stays paused

## leftover / dead (confirm if still armed)

- Opportunity Engine 4× daily, Continuous shipping 2h, GrokBot Social 4h scout/reviewer — old transcripts only; Activator/empire agents were removed from box. If any still armed on a live chat, pause.

## transcript friction (light, since 2026-09-21)

- no new clear repeated skill\|bot\|routine proposal this window
- weekend Frontier card spam is the main friction; covered by Frontier flag above
- do not create anything from this report until human picks

## cos one-liner

weekly-healthcheck: 3 waste flags — Frontier still daily/weekend (narrow Fri), Seller 7d→weekdays, Money Maker 2h pause; see desk/status/weekly-healthcheck-2026-09-28.md

## actions this run

- wrote this file
- appended CoS note to desk/census/_INBOX.md
- appended HUMAN must-lines for the three fixes
- did **not** edit other bots’ routines (cannot from eggbot); did **not** disable weekly-healthcheck
