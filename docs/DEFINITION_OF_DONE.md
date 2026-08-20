# Definition of Done

An Issue is **Done** only when all applicable items are true:

- [ ] Scope and acceptance criteria are met; out-of-scope work has not slipped in.
- [ ] Implementation is linked in a PR that says `Closes #<issue>`.
- [ ] Relevant unit/integration/end-to-end tests pass in GitHub Actions, or a waiver is explicitly approved and recorded.
- [ ] The critical journey was manually checked when automation is insufficient; evidence is in the PR.
- [ ] Security, authorization, data, accessibility, performance, and migration considerations were addressed where relevant.
- [ ] Documentation/contracts (`API.md`, `DATABASE.md`, requirements, ADR) changed when the behaviour or decision changed.
- [ ] Reviewer feedback is resolved; the designated human has approved and merged under branch rules.
- [ ] The Project item is set to Done only after merge. The orchestrator can then include it in `STATUS.md`.

## Waivers

A waiver must name the unmet item, risk, compensating control, expiry/review date, and human approver. Waivers never silently transfer to future releases.
