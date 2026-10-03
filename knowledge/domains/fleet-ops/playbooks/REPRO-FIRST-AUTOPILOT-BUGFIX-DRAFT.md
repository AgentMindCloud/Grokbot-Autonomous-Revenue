# DRAFT — Slack @bot repro-first full-autopilot bugfix
**Status:** draft-only · do not adopt · do not create bots · never pay  
**Lesson:** L21 · Delta §21 · Steals 2026-10-02

## Pattern
Bug-fix intake on Slack: `@<team-bot> repro and fix full autopilot` with stack-trace / crash context. Cloud agent on full autopilot **reproduces the failure in the app before any code change**, then fix → regression test → re-check the **same click** → open PR. Bot reports root cause + PR link + before/after screenshots. Humans can hand off overnight (“lmk when its done”).

## Recipe (Lauren demo; file only)
1. Slack `@bot repro and fix full autopilot` (+ stack trace / repro notes)
2. Cloud agent: **reproduce first**, then change code
3. Fix → add regression test → same-click verify → PR
4. Slack closeout: root cause + PR + screenshots
5. Optional async: go to bed; bot pings when done

## Vs baseline
Extends L19 Team engineer Slack-manager + L16 trust ladder with a concrete **repro-before-edit** gate and evidence pack under “gave my bot my brain” (prefs already on the Team Bot).

## Gate
No CreateAgent / Full Autopilot adopt / merge-policy loosen without owner go. densify: file only. Repro gate is a guardrail to file, not a license to unsupervised merge. L20 Matt live still watch — do not invent / do not bump.
