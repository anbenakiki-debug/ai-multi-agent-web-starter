# Architecture and Product Decisions

## ADR-001 — GitHub is the operational source of truth

**Status:** Accepted — <date>  
**Context:** Multiple agents need shared, auditable task and review state.  
**Decision:** Issues, Project items, PRs, and Actions hold live delivery state; Markdown documents hold contracts and durable rationale.  
**Consequences:** Agents must link work to Issues/PRs. `STATUS.md` may be stale and must cite GitHub evidence.

---

## ADR-<number> — <title>

**Status:** Proposed / Accepted / Superseded  
**Date:** <date>  
**Context:** <problem and constraints>  
**Options considered:** <at least two viable choices and trade-offs>  
**Decision:** <choice>  
**Consequences:** <what becomes easier, harder, cost/risk>  
**Approval / evidence:** <Issue/PR/comment link>
