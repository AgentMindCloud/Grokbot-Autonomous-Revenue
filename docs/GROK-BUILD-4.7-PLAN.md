# Grok Build 4.7 — Operating plan (not a cleanup list)

Repo: https://github.com/AgentMindCloud/Grokbot-Autonomous-Revenue
Branch: `main`. Commit in small batches. Never pay. Never CreateAgent. Never re-enable `ledger-push-cos-note`.

You are finishing a **control plane for finding what agents actually pay for**.
Cleanup is step 0. If you stop at deletes, you failed.

## 0. Scoreboard (this is the mission)

Win in 14 days (2026-09-25 → 2026-10-09) if ANY one is true:

1. **External demand:** 5 paid calls to SKU-0 from wallets that are not `0xB56Bf6B023E94D2059Da1F86b70A90b73333C15B`, reconciled in `ledger/receipts.jsonl`, tagged `lab_self_test=false`.
2. **Radar hit:** one non-SKU-0 endpoint with evidence of **repeat fills by others** (`fills_seen >= 3` in 7 days) AND we ran one named-card canary ≤ $0.03 that Lab scored `scale` or `hold`.
3. **Gap SKU:** one new tiny product shipped because radar proved a hole, with 1 external pay or a documented kill.

Lose / kill a front if:

- Only self-canaries exist on day 14
- Radar rows have `fills_seen=0` and `live_402` missing
- Any bot lists SKU-0 or posts X without human yes
- Daily spend > $10 or hot wallet > $25
- Notification loop returns

Number-1 here means: **fastest honest loop from listed → someone else paid → we copy or kill.** Not most bots. Not most files.

## 1. Why the previous 4.7 draft was not enough

It only deleted old folders and patched stale text. That stops the circus. It does not measure demand, force Lab to score canary #1, produce an external purchase card, define fills_seen, or run weekly keep/merge/kill.

## 2. Non-negotiables

- Caps stay in policy.yaml. No autopay.
- Pay only on a new named card + Governor ALLOW + live_402 match.
- Self-pay is not demand.
- Human sees Market CoS only.
- ledger-push-cos-note stays PAUSED. Task notify OFF.
- Do not revive 50-bot-system, TA, X-growth, workplace bots.
- Do not create bots.

## 3. Repo work

### 3A Delete if present
50-bot-system/**, contracts/planner-role.yaml, creative/formats.md, phase0/hybrid-setup.md, .github/ISSUE_TEMPLATE/loop-test.md
Keep ledger/**, policy.yaml, desk/**, receipts, purchases, VERIFIED.md.

### 3B Patch
DECISIONS.md demand radar YES; pay named card; listing NO.
ROUTINES.md Buyer MCP exists; Lab scores existing receipts.
AUTOMATIONS.md push PAUSED; notify OFF.
LAB.md first job score rc-20260924-01.
PROTOCOL-SCOUT.md fills_seen + live_402_usd.
MARKET-COS.md week scoreboard.
SCHEMA.md research fields fills_seen, live_402_usd, evidence_url, class.

### 3C Add desk/RADAR.md, desk/SCOREBOARD.md, ledger/p-TEMPLATE-external.md
Radar: accepted payees → live 402 → Base USDC transfers to payTo last 7d → rank fills then cheap → max 3 external candidates.
If fills cannot be counted: unknown + evidence_url. Never invent volume.

### 3D Do not revert VERIFIED.md, FRONT.md, FLEET.md, HERMES.md, jobs/IN.md. Point IN.md at RADAR.md.

## 4. Bots — paste only, no CreateAgent
CoS queue + recommend + scoreboard.
Governor ALLOW/DENY.
Buyer named card only.
Auditor recon.
Lab score #1 now.
Scout radar.
Seller private health.
Watch Friday only.
Park Money Maker / Agent Zero / X Coach.
eggbot idle until gap card.
MUTE footer on specialists.

## 5. Tasks
Keep notify OFF: rollup, health, protocol-research, eod, frontier-cards, poteto-daily.
Paused: ledger-push, galaxy-pulse (dup).
Patch protocol-research-file to write fills_seen or NONE.

## 6. Hermes
C:\\Users\\louis\\Documents\\Grokbot-Autonomous-Revenue
HERMES.md + IN.md + RADAR.md
kimi-k3:cloud / qwen3.5:9b / gemma4:12b
Every 2h 07:00-23:00 ICT while awake. No pay.

## 7. 14-day sequence
D0 Build: files. Lab/Auditor close #1.
D1-2 radar 10 rows.
D3 CoS recommends one external ≤ $0.03.
D3-4 human yes, Buyer once.
D5-7 repeat or kill.
D8-10 gap card only if radar agrees. Human yes to build.
D11-14 hit a win condition or write the kill.

## 8. Build exit
50-bot-system gone. RADAR+SCOREBOARD exist. SCHEMA has fills_seen. No inspect-only lies. No new bots. No pay from Build.

## 9. Refuse
Directory listing to fake demand. Self-canary as PMF. Extra bots. Catalog tour of the $25 wallet. X theater.
