# DRAFT — Team Bots multiplayer (shared role-bot)
**Status:** draft-only · do not adopt · do not create bots · never pay  
**Lesson:** L17 · Delta §17 · Steals 2026-09-29

## Pattern
Org fleet unit = **shared Team Bot** for a named role (plugins/skills/credentials on the bot), worked from Slack or Grok Bot, coordinating cloud agents — not a pile of personal specialist bots for the same role.

## Computer / secrets (docs)
| Surface | Computer | Secrets |
|---|---|---|
| Member 1:1 chat | Usually that member’s computer | Owner-added secrets available to teammates using the Team Bot |
| Slack / group | Team Bot’s own computer | Same |

## Auto-review
Team Bots in chats where nobody can answer approval (teammate chats + Slack) run **without Auto-review** unless Enterprise **Enforce Auto-review** is on. File as guardrail; do not loosen desk Auto-review from this card alone.

## Vs baseline
Extends Matcha orchestration-only + Projects≥10 with a first-party multiplayer primitive.

## Gate
No CreateAgent / publish Team Bot / Slack install without owner go. densify: file only.
