# Poteto Scout — 2026-10-06

**Status:** ESCALATE  
**Lead:** INNOVATION | GUIDE. Lauren shipped a new pstack skill, `/poteto-help` in v0.15.13. It's an in-plugin guide skill trained on all her written guides that answers "would a pstack skill or poteto-mode help here?" Also noted: an official Grok Bot changelog and RSS feed (RT), SpaceXAI's free live Grok Bot workshops Oct 6–9 (RT), a Creator Rewards template push, and a voice-mode cosign.

## INNOVATION (ESCALATE: skill ship)
- **source:** https://x.com/poteto/status/2107158163145576902 (2026-10-05 17:17 UTC / 2026-10-06 00:17 ICT). This is Lauren's own post.
- **content:** "new pstack skill: /poteto-help in v0.15.13! … if you're ever wondering how pstack can help you, you can now ask /poteto-help! i fed it all the guides i've written, so anytime you're not sure if a pstack skill or poteto-mode would help - just ask!" Plugin link: https://x.ai/bot/plugin/9717366
- **thread:** In a self-reply she jokes "maybe i should've called this skill /grill-poteto" (2107175192078553224). Asked whether her recent X advice is bundled in, she said "it is not but maybe i can distill myself into the skill 🤔" (2107159719433650470). That's an intent signal, not shipped. A replier compared it to Matt Pocock's ask-Matt skill.
- **vs baseline:** The baseline has pstack 0.15.9 (`/correct`, `/architect`, `/benchmark-checklist`) and the dual-plugin compose with Matt's skills. What's NEW is a meta or router skill: the guide corpus is packaged as a skill so the agent picks the right pstack skill or poteto-mode itself. The version jumped from 0.15.9 to 0.15.13 in about two days.
- **steal (file only; do not adopt):** a "help/router skill fed with the author's own guides" pattern for any skill pack.

## GUIDE
- **Official changelog (RT of @ericzakariasson, 2107161574247129284, 2026-10-05 17:30 UTC):** "grok bot has a changelog now! every release since launch … there's also an rss feed" at https://x.ai/changelog/bot. **signal:** this is a programmatic source for product deltas, a candidate cross-check feed for future scout runs (read-only).
- **Workshops (RT of @tetsuoai, 2107215500992451040):** SpaceXAI is running four free live Grok Bot Zoom workshops Oct 6–9, each 10–11 a.m. PT (00:00–01:00 ICT the next day). Tue is Grok Bot 101 (Martin Lacsamana), Wed is marketing workflows (Jenna Nanpei), Thu is "the people building Grok Bot walk through what's new", and Fri is Grok Bot 201 (Joseph Yang). Lauren isn't named as a presenter; Thursday's session could include the builders. Watch for this in the galaxy-pulse.
- **Creator Rewards push (Lauren, 2107236325271404601, 2026-10-05 22:27 UTC):** "you can get rewarded for creating high quality Grok Bot templates! … share them in this thread", quoting the @SawyerMerritt Creator Rewards announcement (2103612173687861404; biweekly, usage-based, must post public bots on X). This is FLEET/distribution context, not a method.

## USAGE
- **Voice mode cosign (Lauren, 2107186688472813638, 2026-10-05 19:10 UTC):** "voice mode in grok bot is incredibly smooth and actually does real work for you! watch with sound on", quoting @johnbai's voice-call demo with audio (2107184174276780189). She also RT'd voice praise (@thecsguy, @brianchew, @woosal1337). Voice intake is already in the FLEET baseline (Viticci); this is reinforcement.
- **Community pstack throughput RTs:** @fredjmchale said "pstack opened more PRs this week than I did. I started letting agents merge small things this morning" (2107155595799478316). @DanielLockyer reported 19 perf PRs in a day with pstack and about 30% faster deploys from giving the agent deploy logs plus source (2107090228712456662). These are third-party, but she reposted them.

## FLEET
- RT @benjitaylor: "Team Grok Bots are insanely powerful… your entire org able to take advantage of it in minutes" (2107230053939679450). Team Bots is baseline.
- RT @Baconbrix: a bot reserved a Mac Mini (price compare, booking, scheduling, setup) and Motion Bot made a video recap (2107116712109990239). Third-party.

## LIVE-DEMO
- None from Lauren. The workshops are the only scheduled live items (see GUIDE).

## GUARDRAIL
- No new merge/autonomy policy text from Lauren. The "letting agents merge small things" line is a third-party RT, not her policy change.
- Owner lock: follow @poteto patterns; do not critique. Do not adopt methods. Do not create bots. Never pay. File only.

## Skipped (not NEW)
- "hey @bot help me think of some bangers to post about the temu knockoff of you" (2107286347883180315) and "grok bot will keep getting better!" (2107173759962771569) are sentiment.
- RT @housecor recap of the Matt Pocock interview (trust ladder, Michelin restaurant, inner/outer loops, skills shrink over time) is already baseline.
- RT @sweatystartup and @UziObi are general praise.

## Sources / limits
- user-X MCP is still `client-not-enrolled`. The timeline came via api.fxtwitter.com profile statuses (it needed a non-browser User-Agent this run because the default UA got a Cloudflare challenge). The thread came via fxtwitter conversation.
- Do not reply/post/impersonate @poteto. Routing (user 2026-10-02): file-only in-repo; do not message Market CoS, Compound, or Super Intel.
