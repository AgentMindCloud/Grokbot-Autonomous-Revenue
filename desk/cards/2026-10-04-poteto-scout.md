# Poteto Scout — 2026-10-04

**Status:** ESCALATE  
**Lead:** INNOVATION | USAGE | GUIDE (ESCALATE — Lauren shipped pstack **0.15.9** with new `/correct` + `/benchmark-checklist` skills and a Grok Bot Project-agent rearchitect prompt)

## INNOVATION
- **source:** https://x.com/poteto/status/2106542593656111276 (2026-10-04 00:31 UTC / ~07:31 ICT) — primary Lauren post.
- **ship:** pstack **0.15.9** (was **0.15.5** in prior census).
  - **new `/correct` skill:** if you keep correcting agents for the same mistakes, it finds the pattern and fixes it with architecture, types, and checks (environment shaping vs micromanaging agents).
  - **`/architect` improved:** now includes instructions on designing agent-friendly architecture.
  - **new `/benchmark-checklist` skill:** based on @brendangregg's benchmarking checklist.
- **framing (Lauren):** prefer correcting the environment that shapes agent behavior over micromanaging agents; commits as bonsai — tame growth with intentional constraints.
- **quoted prior:** her older correction ladder (https://x.com/poteto/status/2089067865098113024) — eliminate via architecture/data structures → lint/test/CI → skill/rule → human review (ngmi).
- **vs baseline:** version was still 0.15.5 as of 2026-10-03; `/correct` and `/benchmark-checklist` not in known extension set. ESCALATE because Lauren **shipped skill primitives**.
- **steal (file only; do not adopt / do not create bots):** note 0.15.9 skill set + environment-correction framing as playbook pointer only.
- **confidence:** high (Lauren primary + shitter RSS full text; user-X MCP client-not-enrolled)

## USAGE
- **same post — Grok Bot prompt recipe** (copyable spell):
  - `/poteto-mode create a new Project agent to refactor and rearchitect my repo so that our architecture is more agent friendly. it should use both the /correct and /architect skill to look through past commits and find the most common pitfalls that agents fall into, whether its with code quality, performance, or bugs. if relevant you can also use the /recall skill to find past conversations for context. it should make a high level plan for me to review. it should also answer its own open questions by prototyping rather than defer to me. come back to me with a plan backed by real data. once i approve the plan, use either the stack or full autopilot playbook (ask me which i want) to execute`
- **pattern:** Project agent + `/correct` + `/architect` (+ optional `/recall`) → human-reviewed plan backed by prototype data → then **stack** or **full autopilot** playbook (operator chooses).
- **vs baseline:** Project-agent / full-autopilot / stack playbooks were known; NEW is binding them to the new `/correct`+`/architect` commit-pitfall scan and prototype-before-ask gate.

## GUIDE
- Soft companion replies on same thread:
  - https://x.com/poteto/status/2106542725017604277 — pstack plugin link `x.ai/bot/plugin/9717366`
  - https://x.com/poteto/status/2106542831804502141 — points to **dr eggbot** (`https://x.ai/bot/93gOz3op1UQdBdbekQFLK`) to help make a high-quality engineering bot that uses pstack for all its work.
- Dr Eggbot itself already baseline (2026-09-28 Behind the Craft / Matcha); do not re-report creation. NEW angle is pairing Eggbot with the 0.15.9 `/correct`+`/architect` rearchitect recipe.

## FLEET
- N/A as Lauren-authored fleet recipe this window. Soft RT cosign only: @sahiln123 Crisp/Stripe customer-service sweep bot (human-in-loop for money+judgment) — third-party ops pattern, not Lauren method.

## LIVE-DEMO
- N/A — no new live Galaxy/company-build stream this window. Matt Pocock VOD already filed 2026-10-03.

## GUARDRAIL
- No new merge/autonomy policy text from Lauren this window.
- densify: do not adopt / do not create bots; never pay; file only.
- Owner lock: follow @poteto patterns; do not critique methods.

## Skipped (not NEW)
- RT @mattpocockuk "use MORE abstractions" hot take from the Lauren chat (`2106425743479546343`) — interview afterglow; dual-plugin GUIDE already filed 2026-10-03.
- RT Teslaconomics overnight math worksheets (`2106412651395830250`) — third-party consumer demo.
- RT usage/product cheers (mrfundman, mikepat booking cards, KatieMiller bills, Primeagen, theaaron Dot-vs-GrokBot, lingxi feedback ask) — product cheer / third-party UX, not Lauren operating spells.
- `2106436624309768414` "where do you see yourself in 10 years" meme image — not an operating pattern.
- Prior-window items already in 2026-10-03 card: Matt live aired, Viticci multitasking RT, deleting-the-product rant, dogfood cheer, usage-limits.
- Slack `@bot repro and fix full autopilot` + Team engineer manager — already baseline 2026-10-01/02.

## Sources / limits
- user-X MCP: `client-not-enrolled` — timeline via shitter RSS (`shitter.thepixora.com/poteto/rss`); fxtwitter/nitter.cz/jina x.com blocked or challenged this run.
- Do not reply/post/impersonate @poteto. Do not pay. Do not adopt methods or create bots.
- Routing (user 2026-10-02): file-only in-repo; do **not** message Market CoS, Compound, or Super Intel.
