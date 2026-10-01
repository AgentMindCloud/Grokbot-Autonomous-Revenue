# Poteto Scout — 2026-10-01

**Status:** ESCALATE  
**Lead:** FLEET | USAGE | INNOVATION | GUIDE (ESCALATE — Team engineer bot as manager + Projects spawn recipe Lauren posted; Matt Pocock live talk cosign)

## FLEET
- **source:** @poteto favorite-use-case note quoting @bot software-power update  
  - Lauren: https://x.com/poteto/status/2105377066942349794 (2026-09-30 19:19 UTC / 2026-10-01 ~02:19 ICT)  
  - @bot: https://x.com/bot/status/2105373767568621895 (2026-09-30 19:06 UTC) — “Grok Bot is now more powerful for building software. Bots can hand off coding tasks to Cursor, manage your PRs with GitHub and Origin plugins, and share video demos of what they build.”
- **method (Lauren recipe):**  
  1. Create a new **team engineer bot** and add it to Slack  
  2. `@` the bot whenever you want coding work  
  3. Tell it to **create new Projects** — “a way to group together many related agents into one conversation”  
  - Cloud agents can use **any model available on Cursor**; each cloud agent has **its own computer**  
  - This **frees the bot to be a manager** rather than write the code itself
- **vs baseline:** Team Bots multiplayer (2026-09-29: shared plugins/skills/credentials + Slack + fire cloud agents) and Projects≥10 parallel were known. NEW is the concrete **manager split**: Team Bot stays coordinator; coding goes to cloud agents with own computers; Projects are the grouping surface for related agents; product also names **GitHub + Origin PR plugins** and **video demos** of builds.
- **steal (file only; do not adopt / do not create bots):** Role Team Bot on Slack → @ for work → spawn Projects/cloud agents; keep the bot managerial.
- **confidence:** high (Lauren primary + @bot product)

## USAGE
- Slack `@` Team engineer bot as the default work intake (not only 1:1 Grok Bot chat).
- Prefer “create Projects” language when spawning related cloud agents so they share one conversation group.
- **confidence:** high

## INNOVATION
- Explicit **bot-as-manager / cloud-agents-as-workers** operating pattern with per-agent computers + model choice.
- Product surface: handoff to Cursor + GitHub/Origin PR management + shareable video demos (Lauren amplified same day).

## GUARDRAIL
- No new merge/autonomy policy in today’s Lauren posts.
- densify: do not adopt / do not create bots; file only.
- Prior Team Bot credential / Auto-review gaps still apply (see 2026-09-29 card).

## LIVE-DEMO
- Lauren attached a screenshot on `2105377066942349794`; @bot product image on `2105373767568621895`. No new long-form live company-build stream in this window.

## GUIDE
- **Upcoming talk (ESCALATE):** Lauren cosigned Matt Pocock live YouTube interview — skills, high-velocity software factories, SOTA agent shipping.  
  - Lauren: https://x.com/poteto/status/2105324768186777634 (2026-09-30 15:51 UTC) — “extremely excited about this!”  
  - Matt: https://x.com/mattpocockuk/status/2105239236178018636 — Friday 9AM PT; https://youtube.com/live/MN9dGgmLyso  
  - Watch/file when live (Fri 2026-10-02 ~9:00 PT / ~23:00 ICT); do not invent content before air.

## Skipped (not NEW)
- `2105336247548006760` burnout/fun-at-work quote of @jenny_wen — personal, no operating method.
- `2105051957258055938` trebuchets aphorism — already skipped 2026-09-30.
- Pinned Compile talk `2102050467505430555` — baseline.
- Team Bots launch / restatement prompt — baseline (2026-09-29).
- pstack still **0.15.5** (`pstack/.cursor-plugin/plugin.json`).

## Sources / limits
- user-X MCP: `client-not-enrolled` — timeline via Playwright (`https://x.com/poteto`) + api.fxtwitter.com status fetches.
- Do not reply/post/impersonate @poteto. Do not pay. Do not adopt methods or create bots.
