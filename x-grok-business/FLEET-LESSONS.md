# Fleet lessons → implement HERE (2026-09-15)

Mandate: how fleets *work*, not how they sell. Apply to Compound + Critic (+ Poteto Scout when relevant).
Sell research (HOW-THEY-WORKED) = reference only. Wedge B HOLD.

## Ranked lessons (steal → local change)

### L1 — Coordinator vs workers
**Source:** @poteto — Bot keeps context clean; cloud agents / executors do build-verify on their own machines.
**Here now:** Compound already dispatches executor subagents; Critic is adversarial peer not a worker.
**Implement:** Explicit rule in every multi-step research: Compound = supervisor (goal, bar, synthesis, Critic handoff); executors = workers (fetch/write files); never make Compound redo long digs inline. One workstream = one durable folder under knowledge/domains/.

### L2 — Outer loop with human priority
**Source:** poteto — farm signals → human prioritizes → /goal /loop /swarm.
**Here now:** User drives pivots; we over-asked widgets.
**Implement:** Default quiet research loops; surface only exceptions / ready frameworks. When owner sets a mandate, lock STATE and run until Critic gate — don’t re-ask the same pick.

### L3 — Verification as infrastructure
**Source:** poteto — /swarm verification = merge confidence; Critic evidence bar.
**Here now:** Critic pair exists; evidence bar written for sell cases.
**Implement:** Generalize evidence bar to ALL major Compound outputs (not just sell). No “worked” / “cleared” / “pilot ready” language without Critic fields or an explicit WEAK/PROMO/MOTION-ONLY tag.

### L4 — Materialized memory (Feature Map analogue)
**Source:** poteto Feature Map; Billy “one account = one mission.”
**Here now:** knowledge/domains/* + profile memory.
**Implement:** Every active domain has STATE.md with Mode / Locked findings / Do-not / In-flight. Update STATE on every mandate change before tooling.

### L5 — Approval / distribution split
**Source:** Haggle never-sign; Corey Stripe; Billy CoS gate; Critic “approval ≠ distribution.”
**Here now:** Draft-only external.
**Implement:** Keep. Add: internal “cleared” never means external send. Landing channel must be real before any delivery routine.

### L6 — Fleet hygiene (Dr Eggbot v0.2 analogue)
**Source:** weekly unused/expensive routines; friction skim (“not what i meant”).
**Here now:** No routines; automations empty.
**Implement:** Before creating any routine, require: purpose, quiet-when-empty, delete condition. After owner corrections, log a FRICITION.md line and adjust skill/prompt — don’t just apologize.

### L7 — X is optional input, not the product
**Source:** Critic structural lock from sell batch.
**Here now:** Earlier X-desk wedge overweighted X.
**Implement:** X/connectors = sensors. Product = judgment + durable state + Critic gate.

## Implementation queue (this turn → next)
1. Write this doc + update domain STATE to FLEET-OPS mode — DONE this turn
2. Save shared skill: fleet-compounding-ops (coordinator / evidence / STATE discipline)
3. Save shared skill: critic-evidence-gate (when to send Critic, required fields)
4. Add FRICITION.md log for owner corrections
5. Critic reviews skills before any standing routine is armed

## Do not
- Arm sell/X-desk pilots
- Invent monetize models from poteto
- Create routines that ping owner without quiet-when-empty

---

## Added 2026-09-24 (Super Intel ← Poteto Scout ESCALATE)

### L8 — Seat JD with refuses
**Source:** Lauren Galaxy recap → Rank’em guide.
**Here now:** Super Intel profile already refuses monetize/sell/impersonation; Compound pair-only.
**Implement:** Codify owns/refuses/handoff table for every fleet seat; spend + player-facing ship behind named gate or human.

### L9 — Recap → playbooks → product
**Source:** @poteto Galaxy game-studio recap post.
**Implement:** Multi-day build closeout = short draft recap + links; no external post without owner go.

### L10 — children.tsv + delta-only
**Source:** pstack 0.15.3 Autopilot-full.
**Implement:** Workstream tracker under fleet-ops; Super Intel quiet unless NEW/ESCALATE.

### L11 — Owner vs babysitter + append-only audit
**Source:** pstack 0.15.5.
**Implement:** Playbook rows supersede, never delete; helper seats cannot force-push.

### L12 — Parallel Cursor Projects + pstack (not more bots)
**Source:** @poteto 2026-09-24 Projects+pstack scale post.
**Here now:** Desk seats fixed; Compound pair draft; CreateAgent = Needs-go / refuse.
**Implement (draft only):** Document “one Cursor Project per parallel lane + pstack”; refuse creating bots for concurrency. Owner/CoS Friday surface before any adopt.

### L13 — Behind the Craft as HOW-THEY-WORKED primary
**Source:** Lauren+Peng Peter Yang episode (2026-09-27).
**Implement (draft):** Cite; do not clone her 14-bot roster.

### L14 — Orchestration-only eng lead (Matcha)
**Implement (draft):** Lead seats decompose/route only; workers + cloud agents dig.

### L15 — Design first-5% keyframe
**Implement (draft):** File pattern only until design seat exists with owner go.

### L16 — Trust ladder → routine / land-before-read
**Implement (draft):** No new routine or land-before-read without watch→correct→skill→one-shot evidence.


### L17 — Team Bots multiplayer (shared role-bot)
**Source:** Lauren cosign of @bot Team Bots launch (2026-09-28/29).
**Here now:** Desk seats are personal Grok Bots; CreateAgent = Needs-go / refuse without owner.
**Implement (draft only):** File shared role-bot + Slack + cloud-agent spawn as org unit; note credential blast radius and Auto-review-off-in-Slack unless Enforce. Do not CreateAgent / publish Team Bot without owner go.

### L18 — Restatement before swarm
**Source:** Lauren most-used prompt (2026-09-29).
**Implement (draft):** Mandatory restatement turn before cloud-agent / executor spawn; pairs with L16 trust ladder.
