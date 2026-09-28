# Poteto Scout — 2026-09-28

**Status:** ESCALATE  
**Lead:** GUIDE | FLEET | USAGE | GUARDRAIL (ESCALATE — new Lauren-cosigned talk/guide + merge/autonomy policy signal)

## GUIDE
- **source:** @poteto quote-endorsed Peter Yang *Behind the Craft* episode with @poteto + @pengzheng_ (Grok Bot eng + design leads).  
  - Lauren: https://x.com/poteto/status/2104260894004039831 (~2026-09-27 17:15 UTC / 2026-09-28 ~00:15 ICT) — “had a lot of fun chatting with @petergyang about our grok @bot setups!”  
  - Peter: https://x.com/petergyang/status/2104213287353356531 (2026-09-27 14:15 UTC)  
  - YouTube: https://youtu.be/xZ5TEaleUdg  
  - Newsletter (paid full; free TOC + top takeaways): https://creatoreconomy.so/p/grok-bot-team-14-best-bots-peng-zheng-lauren-tan (Sep 27, 2026)  
  - Spotify: https://open.spotify.com/episode/6Plo01OWMIMD7U9RgFnLRk  
- **method:** Public “14 bots we use for work and life” operating walkthrough — first clean refuse-to-automate / org bot-split style writeup gap from Compile baseline now partially filled via interview + takeaways.
- **vs baseline:** Compile talk + Galaxy Rank’em guides were known; this is a **new** co-signed talk/guide focused on personal+team bot roster and trust ladder.
- **steal (file only; do not adopt):** Treat as HOW-THEY-WORKED primary source for Compound/Super Intel; do not create bots from it.
- **confidence:** high

## FLEET
- **Matcha eng-lead pattern:** Lauren hands big projects to eng lead bot **Matcha**. Matcha does **not** do the work — it breaks the project down for other eng bots. Each eng bot spins coding agents in the cloud → “really massive agent swarms.”
- **vs baseline:** Extends “Grok Bots as coordinators spawning cloud agents” + Projects≥10 with a **named non-executing lead bot** that only decomposes/routes.
- **Cross-room:** PM + design + eng bots put “in the same room” (episode chapter 06:31).
- **Dr. Eggbot:** meta-bot that **designs and audits** other bots (chapter 17:59) — bot-for-bots ops layer.
- **steal:** Coordinator ≠ worker; keep lead bots orchestration-only. Meta-auditor bot as fleet hygiene (file only).
- **confidence:** high (public takeaways; full episode paywalled)

## USAGE
- **Design bot (Peng):** Figma MCP + skill describing file layout + design-system tokens. Human does first ~5% (system + one keyframe); bot extends to full user flow.
- **Life/ops bots:** CoS bot buys supplies / lists gear; assistant bot booked Lauren’s multi-city trip — work+life delegation (“everything I touch with keyboard and mouse…”).
- **Self-test before merge:** Lauren’s bots test their own work before merging (chapter 14:16) — aligns with verification skill / Autopilot rounds but restated as bot-owned gate.
- **confidence:** high for takeaways listed publicly; medium for unpaid full transcript details.

## GUARDRAIL
- **Trust ladder (quoted):** “First, watch your bot work and correct it. Turn what worked into a skill. Once it nails the task in one shot, make it a routine.”
- **vs baseline:** Compile “trust before scale” → now an explicit **watch → correct → skill → one-shot → routine** pipeline.
- **Autonomy / merge policy signal:** “Sometimes I actually don't even look at the PR until after it's landed…” + episode chapter “Eng bots that sometimes land PRs before Lauren reads them” (25:22). Stronger than Galaxy “Land merges” — human post-land review is acceptable when trust ladder is earned.
- **Michelin kitchen** restated (anti-“software factory” slop) — already Compile baseline; not NEW alone.
- **steal:** Skill→routine promotion gate; land-before-read only after one-shot reliability. Do not loosen merge policy without that ladder.
- **confidence:** high

## LIVE-DEMO
- Episode itself is a live walkthrough of 14 real bots (work + life). YouTube free; Substack writeup partially free.

## Skipped (not NEW)
- `2103923390327509419` “poteto poteto poteto” meme (Sep 26/27) — joke only.
- `2103894438397546787` “using opus 5.5 max fast to fix a typo” — joke quote-tweet; Opus 5.5 already pstack 0.15.5 default.
- `2103604741695799347` Starship-launch contest promo — marketing, no operating method.
- pstack still **0.15.5** on cursor/plugins (`plugin.json`); no pstack commits since 2026-09-25.
- Compile / Rank’em / Galaxy bot-split / Projects≥10 — already baseline.

## Sources / limits
- user-X MCP: client-not-enrolled (forbidden). Verified via Apify scrape of x.com/poteto + Playwright timeline + creatoreconomy/unrollnow mirrors.
- Full Substack episode body paywalled; card uses free TOC, public X quotes, and free “Top takeaways” section only.
- Do not reply/post/impersonate @poteto. Do not pay. Do not adopt methods or create bots.
