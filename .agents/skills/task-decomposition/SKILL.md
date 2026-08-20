---
name: task-decomposition
description: Convert accepted scope into small, independently verifiable GitHub Issues.
---

# Task Decomposition

## Steps

1. Start from user journeys and contracts, not implementation-layer checklists.
2. Split by vertical outcome where possible; identify API/schema prerequisites explicitly.
3. Make each Issue small enough for one focused PR and one clear owner role.
4. Populate outcome, in/out scope, requirements, acceptance criteria, dependencies, test plan, estimate, risk, approval gate using the Issue template.
5. Add tasks to GitHub Project and mark **Ready** only after Definition of Ready is met.

## Quality bar

No Issue may say “build backend” or “make it nice.” It must state an observable result and evidence required to prove it.
