---
name: task-dispatch
description: Assign ready work safely across specialized agents.
---

# Task Dispatch

## Steps

1. Inspect GitHub Project for Ready, unblocked tasks and active PR/file-contract conflicts.
2. Assign one accountable role and agent profile; add assignee/Owner/Role fields.
3. Give the agent Issue number, linked requirement IDs/contracts, boundaries, expected evidence, branch naming, and next handoff role.
4. Dispatch independent work in parallel only when interfaces are stable and overlapping files are unlikely.
5. When blocked, keep Project status Blocked, record exact missing decision/dependency, and notify orchestrator/human.

## Handoff prompt

`Work only on #<id>. Read AGENTS.md and <profile>. Meet each acceptance criterion. Open a draft PR with Closes #<id>, test evidence, risks, and a handoff to <role>. Do not widen scope.`
