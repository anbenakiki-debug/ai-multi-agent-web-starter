# AI Multi-Agent Website Development Rules

## Authority and source of truth

Use this precedence order when sources disagree:

1. Approved GitHub Issue acceptance criteria and linked PR
2. `REQUIREMENTS.md` and accepted entries in `DECISIONS.md`
3. Approved architecture/API/database contracts
4. This file and role/skill instructions
5. Chat messages (context only; never authoritative project state)

GitHub is the operational source of truth: Issues are planned work, the Project is delivery status, PRs are proposed changes and review evidence, and Actions are automated verification evidence. Do not claim a task is complete without its Issue, PR, and checks reflecting that fact.

## Operating loop

1. The orchestrator clarifies requirements, writes or updates the project documents, then creates small Issues.
2. Each Issue has one accountable owner, testable acceptance criteria, a dependency list, and a linked Project item.
3. An implementation agent works only within the assigned Issue scope, creates a branch and draft PR, and reports evidence in the PR.
4. QA and reviewer agents comment on the PR; only the assigned human approver merges it.
5. The orchestrator updates Project fields and `STATUS.md` only by reconciling GitHub state, then reports blockers and next decisions.

## Non-negotiable behaviour

- Ask before any irreversible production, billing, credential, personal-data, or external-user action.
- Never invent requirements, test results, approvals, API contracts, or progress.
- Work in small, reviewable changes. Keep one Issue focused on one outcome; split work that needs more than one independently testable outcome.
- Link Issue ↔ branch ↔ PR using `Closes #123` in the PR body. Use conventional branch names: `feat/123-short-name`, `fix/123-short-name`, `chore/123-short-name`.
- Preserve unrelated changes. Do not rewrite history or close issues merely to make charts look better.
- Record consequential, accepted decisions in `DECISIONS.md`; record unresolved material risks in `RISKS.md`.
- Treat `STATUS.md` as a human-readable snapshot generated from GitHub, never as a substitute for it.

## Required Issue fields

Every delivery Issue must include: problem/outcome, scope, out of scope, acceptance criteria, owner role, dependencies, verification, priority, estimate, and human approval need. It must be in the GitHub Project.

Recommended GitHub Project fields: `Status` (Backlog / Ready / In progress / In review / Blocked / Done), `Owner`, `Role`, `Priority`, `Milestone`, `Estimate`, `Risk`, `Approval`, `PR`, and `Updated`.

## Definition of Ready

An Issue may move to **Ready** only when its requirements are understandable, acceptance criteria are testable, ownership and dependencies are explicit, and the human approval requirement is known.

## Definition of Done

See [`docs/DEFINITION_OF_DONE.md`](docs/DEFINITION_OF_DONE.md). “Code written” is not done.

## Agent handoff contract

Each handoff comment or report contains:

```text
Issue: #123
Status: Ready | In progress | Blocked | In review | Done
What changed: <one or two sentences>
Evidence: <PR, test run, screenshots, links>
Blocker / decision needed: <none or explicit question>
Next owner: <role/person>
```

## Human gates

Human approval is mandatory before: accepting requirements, selecting a stack or irreversible architecture, changing data retention/auth/payment/permissions, merging to protected branches, and deploying production. The human may delegate routine approvals in GitHub branch-protection rules, but the policy must be documented in `DECISIONS.md`.
