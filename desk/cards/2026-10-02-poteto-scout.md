# Poteto Scout — 2026-10-02

**Status:** ESCALATE  
**Lead:** USAGE | LIVE-DEMO | GUARDRAIL | FLEET (ESCALATE — Slack `@bot repro and fix full autopilot` live bug-fix loop with repro-first cloud agent)

## USAGE
- **source:** https://x.com/poteto/status/2105576730413134291 (2026-10-01 08:33 UTC / ~15:33 ICT) — “i gave my bot my brain so it knows exactly what i want. this is how i fix bugs now”
- **method (from Slack screenshot on that post):**  
  1. In Slack, `@poteto repro and fix full autopilot` (team bot handle; intake is Slack `@`)  
  2. Bot starts a **cloud agent on full autopilot** to **reproduce first** (here: draft submit crash from Baltazar’s stack trace), **then** change code  
  3. Pipeline after repro: fix → add regression test → re-check the same click → open PR  
  4. Bot reports root cause + PR link + before/after screenshots back in Slack  
  5. Companion replies on same thread: shout-out for stack trace (`2105576926593302770`); “hey @bot lmk when its done im going to bed” (`2105577346329870440`) — async overnight handoff
- **vs baseline:** Team engineer Slack-manager + Projects/cloud agents (2026-10-01) and Full Autopilot=`/goal`+`/loop`+`/swarm` were known. NEW is the concrete **bug-fix spell** + **repro-before-edit** gate + evidence pack (regression test, same-click verify, screenshots) under “gave my bot my brain” (bot already holds her prefs/standards).
- **steal (file only; do not adopt / do not create bots):** Slack `@bot <repro and fix full autopilot>` with stack-trace context; require repro before code; close with test + PR + screenshots.
- **confidence:** high (Lauren primary + readable Slack demo)

## LIVE-DEMO
- Same post is a live SpaceXAI/Cursor engineering demo (draft submit crash), not a long-form Galaxy stream.
- Screenshot OCR: Lauren Tan → `@poteto repro and fix full autopilot`; poteto [APP] acknowledges cloud-agent full autopilot plan as above.

## GUARDRAIL
- Explicit **reproduce the crash in the app before it changes any code** — autonomy bound by repro gate.
- densify: do not adopt / do not create bots; file only.
- No new merge-policy text in Lauren’s posts this window.

## FLEET
- Reinforces manager Team Bot on Slack dispatching cloud-agent workers; coding stays off the bot’s own keyboard.
- Ties to 2026-10-01 manager recipe without re-stating Projects spawn steps.

## INNOVATION
- N/A as a new primitive — composition of known Full Autopilot + Team Bot Slack intake. Value is the filed recipe, not a new skill/Dune surface.

## GUIDE
- Matt Pocock live still **upcoming** (Fri 2026-10-02 9AM PT / ~23:00 ICT): https://youtube.com/live/MN9dGgmLyso — cosign already filed 2026-10-01; do not re-report; watch/file after air. Not live yet at this scout (~09:37 ICT).

## Skipped (not NEW)
- `2105718847181656361` “you can do anything with grok bot” + RT `2105713240701538538` (@bot proactive suggestions) — product cheer / meme art, no Lauren operating recipe.
- RT `2105766335951065517` (@jediahkatz Grok Bot 3x faster) — product perf RT.
- RT `2105751999220429265` (@benjitaylor Grok in X Chat) — product RT.
- `2105733341618253878` pepsi/coke meme — joke.
- RT `2105628270930845990` (@mattpocockuk restatement prompt echo) — restatement already baseline 2026-09-29.
- `2105520338998304814` “make me a billion dollars…” — joke.
- Team engineer manager recipe + Matt Pocock cosign — baseline as of 2026-10-01.
- pstack still treated **0.15.5** (no new version signal in window).

## Sources / limits
- user-X MCP: `client-not-enrolled` — timeline via twiiit/shitter RSS + api.fxtwitter.com status + local screenshot OCR.
- Do not reply/post/impersonate @poteto. Do not pay. Do not adopt methods or create bots.
