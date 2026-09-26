# Fleet Command Dashboard Skeleton

**Build with Grok Build / Build Mode.**

## Components
- Left: Bot roster (status idle/planning/executing/revenue, role tags, current task)
- Center: Active pipelines (Gantt or graph view of multi-step)
- Right: Live metrics (X impressions/ER/velocity from main, revenue today/cumulative, originality avg, risk score)
- Bottom: Content candidate queue with predicted scores + one-click approve/schedule
- Drill-down: Any bot memory/contract + recent outputs + performance

## Controls
- Trigger simulation
- Adjust goal weights
- Pause fleet
- Force Optimizer run
- Dual-approval financial gate

## Data Flow
Shared memory → Metrics bots → Dashboard → Human / Governance gates → TaskQueues → Specialists

This is both internal tool and sellable prototype/skill.
