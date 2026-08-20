# Risk Register

Risk score = likelihood (1–5) × impact (1–5). Escalate scores ≥12 or any security/privacy concern to the accountable human.

| ID | Risk / uncertainty | Likelihood | Impact | Score | Early signal | Mitigation / contingency | Owner | Status |
|---|---|---:|---:|---:|---|---|---|---|
| R-001 | Requirements are not yet validated with target users. | 3 | 4 | 12 | unanswered questions / rework | timebox discovery; human approves MVP | orchestrator | Open |
| R-002 | External service changes or rate limits. | 2 | 3 | 6 | errors / vendor notices | isolate adapter; define fallback | backend | Open |

## Review cadence

The orchestrator reviews risks at milestone planning, when a task is blocked, and before release. Closing a risk needs evidence, not optimism.
