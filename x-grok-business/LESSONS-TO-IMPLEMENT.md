# LESSONS-TO-IMPLEMENT.md
**For:** Critic kill-shots before any further implement  
**Date:** 2026-09-15 (Asia/Saigon)  
**Mandate (LOCKED):** STOP sell/monetize/wedges/pilots. START: how working bots operated → implement HERE (Compound↔Critic + owner stack). Wedge B HOLD. Bottocks freeze untouched.

**Sources allowed (mechanism only):** Corey HITL payment gate · Billy CoS/HITL outbound · Jon HITL booking · Haggle always/needs-go/never · Poteto coordinator/cloud-workers (mechanism-only; monetize NULL).  
**Excluded:** sell/$ claims, fleet scale, X-desk as product.

**Rank:** leverage for solo + approval-gated + no unsupervised post.

---

## L1 — Coordinator vs workers (KEEP CONTEXT CLEAN)
| Field | Content |
|---|---|
| **Mechanism** | Persistent Bot holds goal/state; workers (cloud agents/executors) do digs on separate context so the coordinator stays clean. |
| **Source** | Poteto coordinator pattern (PRIMARY mechanism posts; monetize excluded). |
| **Change HERE** | Pair rule + skill text: Compound never runs >2 tool-round digs inline — dispatch executor; one workstream → one `knowledge/domains/<slug>/`. |
| **Cost if skip** | Context thrash; “worked” claims from half-finished digs; owner sees thrashing. |
| **Gate** | **draft-only** (pair rule / skill). Critic optionally pressure-tests wording before we treat as locked. |

## L2 — Explicit permission lines (always / needs-go / never)
| Field | Content |
|---|---|
| **Mechanism** | Split actions into always-allowed reads, needs-go for external-facing sends, never for sign/buy/subscribe. |
| **Source** | Haggle Bot guardrails (mechanism; $ PROMO excluded). |
| **Change HERE** | Add `knowledge/domains/fleet-ops/PERMISSIONS.md` + Compound profile/memory line: Always = read/research/write drafts on box; Needs-go = SendToAgent fan-out beyond Critic/Poteto Scout, any external publish/email/pay; Never = unsupervised post/DM, spend, delete teammate. |
| **Cost if skip** | Approval theater; accidental external side effects; Critic “approval≠distribution” repeats. |
| **Gate** | **draft-only** file first; **needs owner go** to change Never/Needs-go lists that affect messaging other agents. |

## L3 — Human gate on irreversible outbound
| Field | Content |
|---|---|
| **Mechanism** | Draft lands with human; human edits/sends payment link, sponsor email, or booking confirm. |
| **Source** | Corey (payment when ready) · Billy (CoS → “put in Gmail I’ll edit”) · Jon (customer confirm before book). |
| **Change HERE** | Pair rule: no routine may auto-send email/X/Slack externally; any delivery skill ends at draft path + owner ping. Document in PERMISSIONS.md Needs-go. |
| **Cost if skip** | Unsupervised post/pay risk; brand damage; Critic hard fail. |
| **Gate** | **draft-only** rule text; **needs owner go** before any email/X connector routine. |

## L4 — Evidence gate before “cleared / worked / wedge”
| Field | Content |
|---|---|
| **Mechanism** | Adversarial review with fixed fields before merge confidence (analogue: verification before merge). |
| **Source** | Critic pair practice (already live) + poteto verification-as-infra (mechanism). |
| **Change HERE** | Skill `critic-evidence-gate` (already drafted): 5 fields + SURVIVES/MOTION-ONLY/WEAK/PROMO labels; Compound must rewrite kill-shots in writing before owner wedge ask. |
| **Cost if skip** | Laundering research as clearance (already happened on Wedge B / sell N=5). |
| **Gate** | **draft-only** after optional Critic pressure-test skill text; then lock as pair rule. |

## L5 — STATE-first + friction log on course correction
| Field | Content |
|---|---|
| **Mechanism** | One mission / materialized memory; skim “not what I meant” into process change. |
| **Source** | Billy one-account=one-mission · Poteto Feature Map / Dr Eggbot friction skim (mechanism). |
| **Change HERE** | Every mandate change updates domain `STATE.md` before tools; append `FRICTION.md` row (date/signal/adjustment). Already started under `fleet-ops/`. |
| **Cost if skip** | Repeated wrong-frame work (AI-vendor list as ABM); widget spam after skips. |
| **Gate** | **draft-only** (local files). No owner go needed to keep logging. |

## L6 — Quiet outer loop (exceptions only)
| Field | Content |
|---|---|
| **Mechanism** | Farm/process in background; human prioritizes; don’t spam. |
| **Source** | Poteto outer-loop factory (human prioritizes) · owner preference exceptions-only. |
| **Change HERE** | Pair rule: after mandate lock, no re-ask same pick; surface Critic kill-shots / blockers / ready frameworks only. Any future routine must include quiet-when-empty + delete condition in prompt. |
| **Cost if skip** | Owner fatigue; skipped widgets; fake progress noise. |
| **Gate** | **draft-only** pair rule; **needs owner go** to arm any routine. |

## L7 — Sensors ≠ product
| Field | Content |
|---|---|
| **Mechanism** | Money-clearing runs used email/CRM/portals; X was optional or absent. |
| **Source** | Critic structural lock on HOW-THEY-WORKED (Corey/Billy/Jon mechanisms; X not load-bearing). |
| **Change HERE** | STATE lock: X/web = sensors only; product = durable judgment artifacts + Critic gate. Ban default “X desk wedge” language until owner reopens sell research. |
| **Cost if skip** | Relapse into X-pilot packaging against evidence. |
| **Gate** | **draft-only** STATE/memory lock (can set now as text); wedge reopen **needs owner go**. |

---

## Already drafted (codified; Critic advisory — treat as not locked)
- Skill `fleet-compounding-ops` — overlaps L1/L5/L6/L7
- Skill `critic-evidence-gate` — overlaps L4  
Compound will **not** arm routines or claim these locked until this file’s kill-shots land. If Critic wants skills deleted until clear, say so.

## Out of scope this file
Sell motions, retainers, Marketplace SKUs, Wedge A/B deepen, bottocks, fleet scale / 20-agent CoS copies.

---

## L8 — Seat JD: owns / refuses / hands off (2026-09-24)
| Field | Content |
|---|---|
| **Mechanism** | Each bot/seat has an explicit job description that names refuses and handoff targets; no mega-bot. |
| **Source** | Poteto Galaxy recap → Rank’em six-seat guide (Lauren pointer; Ryan Perry author). |
| **Change HERE** | Rewrite Super Intel + Compound (+ any new fleet seat) prompts as owns X / refuses Y / hands off to Z. Mirror refuse table for Analytics/Creatives/spend/GCS. |
| **Cost if skip** | Context bleed; seats stepping on each other; unsupervised spend/creative/code mix. |
| **Gate** | **draft-only** prompt text now; **needs owner go** before CreateAgent / expanding cast. |

## L9 — Live-build closeout recap (2026-09-24)
| Field | Content |
|---|---|
| **Mechanism** | After a live build, short recap linking standing playbooks + shipped product. |
| **Source** | @poteto 2026-09-23 Galaxy game-studio recap. |
| **Change HERE** | When Compound finishes a multi-day build, produce a one-pager: what shipped + links to STATE/playbooks — not a sell narrative. |
| **Cost if skip** | Method stays trapped in VOD; no durable handoff. |
| **Gate** | **draft-only**. External publish of recap **needs owner go**. |

## L10 — children.tsv + delta-only ticks (2026-09-24)
| Field | Content |
|---|---|
| **Mechanism** | Track subagents in a simple table; ping only on tracked change; cut skill prose models no longer need. |
| **Source** | pstack 0.15.3 Autopilot-full (#414, merged by poteto). |
| **Change HERE** | Scout→Intel→Compound path: maintain a workstream tracker; Super Intel stays quiet unless NEW/ESCALATE; A/B-trim skill text. |
| **Cost if skip** | Noise pings; stale skill bloat; lost child context. |
| **Gate** | **draft-only** tracker file; routine arming **needs owner go**. |

## L11 — Owner vs babysitter push + append-only audit (2026-09-24)
| Field | Content |
|---|---|
| **Mechanism** | Babysitter cannot rebase/force-push; stack owner may rebase own branch + force-with-lease after ls-remote; audit logs supersede never delete. |
| **Source** | pstack 0.15.5 (#419, #422). |
| **Change HERE** | Pair rule: playbook/STEALS/STATE rows are append-only (supersede with new dated row). Label who may rewrite vs who may only observe. |
| **Cost if skip** | Silent history loss; unsafe force-push by helper seats. |
| **Gate** | **draft-only** for box playbook files; git force-push still **needs owner go** / Autopilot-owner role. |

## L12 — Many concurrent Cursor Projects + pstack (2026-09-25)
| Field | Content |
|---|---|
| **Mechanism** | Parallel workstreams as separate Cursor Projects (coordinator + shared context + subscriptions), each with pstack; scale to many concurrent Projects (≥10 claimed). |
| **Source** | @poteto 2026-09-24 → https://x.com/poteto/status/2103252563999232092 + cursor.com/blog/projects |
| **Change HERE** | Playbook: map lanes to Cursor Projects + pstack; **do not** CreateAgent new specialist bots for parallelism. Keep Market Desk seat cast. |
| **Cost if skip** | Serial bottleneck or mega-bot context bleed when trying to parallelize inside one Project/bot. |
| **Gate** | **draft-only**. Do not adopt. Do not create bots. Human ACCEPT `d-20260925-06` = Friday CoS surface only, not Super Intel implement. |

## L13 — HOW-THEY-WORKED primary: Behind the Craft 14-bots (2026-09-28)
| Field | Content |
|---|---|
| **Mechanism** | Lauren+Peng co-signed talk/guide on bot roster + trust ladder as operating primary. |
| **Source** | https://x.com/poteto/status/2104260894004039831 · youtu.be/xZ5TEaleUdg · creatoreconomy writeup |
| **Change HERE** | Cite as primary in HOW-THEY-WORKED / fleet-ops; do not invent seats from her 14-bot list. |
| **Cost if skip** | Miss clearest public refuse-to-automate / bot-split writeup since Compile. |
| **Gate** | **draft-only**. Do not adopt. Do not create bots. |

## L14 — Orchestration-only lead (Matcha shape) (2026-09-28)
| Field | Content |
|---|---|
| **Mechanism** | Named eng-lead bot decomposes/routes only; workers spawn cloud agents. |
| **Source** | Behind the Craft takeaways (Matcha). |
| **Change HERE** | Compound / desk leads stay orchestration-only; digs to executors/cloud — already aligned; codify in seat JD. |
| **Cost if skip** | Mega-bot context bleed; lead doing worker jobs. |
| **Gate** | **draft-only**. No CreateAgent for a “Matcha clone”. |

## L15 — Design keyframe → Figma-MCP scale-out (2026-09-28)
| Field | Content |
|---|---|
| **Mechanism** | Human first ~5% (system + keyframe); bot extends via Figma MCP + tokens skill. |
| **Source** | Peng design-bot takeaways. |
| **Change HERE** | If/when design lane exists: playbook this shape; else file only. |
| **Gate** | **draft-only**. No new design bot. |

## L16 — Trust ladder before routine / land-before-read (2026-09-28)
| Field | Content |
|---|---|
| **Mechanism** | watch → correct → skill → one-shot → routine; land-before-read only after one-shot. |
| **Source** | Lauren quoted trust ladder + episode 25:22 autonomy chapter. |
| **Change HERE** | Before arming routines or loosening merge: require skill + one-shot evidence. Append-only FRICTION on corrections. |
| **Cost if skip** | Premature Autopilot / merge autonomy. |
| **Gate** | **draft-only**. Arm routines / merge-policy change = Needs-go. |


## L17 — Team Bots multiplayer / shared role-bot (2026-09-29)
| Field | Content |
|---|---|
| **Mechanism** | First-party shared Team Bot: plugins/skills/credentials + Slack/Grok Bot multiplayer; coordinator fires cloud agents from the shared surface. |
| **Source** | @poteto 2104664283808428165 quoting @bot 2104661562715967548 + cursor.com/docs/grok-bot /teams |
| **Change HERE** | Playbook: shared role-bot as org fleet unit (not new personal specialist bots). Document computer split + secrets blast radius + Auto-review gap. |
| **Cost if skip** | Miss platform multiplayer primitive; keep inventing personal-bot swarms for org share. |
| **Gate** | **draft-only**. Do not adopt. Do not create bots. Never pay. |

## L18 — Restatement prompt before execute (2026-09-29)
| Field | Content |
|---|---|
| **Mechanism** | Agent restates goals + problem in own words before digging. |
| **Source** | @poteto 2104744961904394699 |
| **Change HERE** | Add restatement as first-turn / skill step before swarm or cloud-agent spawn (pairs with trust ladder watch→correct). |
| **Cost if skip** | Agents execute on misread goals. |
| **Gate** | **draft-only**. No routine arm from this alone. |
