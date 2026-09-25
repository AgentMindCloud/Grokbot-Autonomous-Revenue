# Playbook draft — Concurrent Cursor Projects + pstack (USAGE 2026-09-25)
Status: **draft-only** · Do not adopt · Do not create bots · Source: @poteto status/2103252563999232092

## Steal
Run many workstreams as separate Cursor Projects in parallel (often ≥10), each with pstack — not one mega-bot / one mega-project.

## Shape to copy (when owner/CoS Friday surface or explicit go)
1. One Cursor Project per workstream (perf, debt, experiment, feedback fix, dashboard, etc.)
2. Coordinator + shared context + subscriptions (see cursor.com/blog/projects)
3. Outer loop stays Grok Bot pair seats; Projects are dig lanes, not new teammate bots
4. Cap concurrency to what the box/owner can supervise; quiet unless delta

## Refuse
- Spawning new specialist bots for each lane (CreateAgent = Needs-go; default refuse)
- Adopting this live before Friday CoS surface / owner go
- Collapsing all lanes into one mega-bot context

## Gate
draft-filed now · adopt = owner go or Friday CoS surface · CreateAgent still Needs-go
