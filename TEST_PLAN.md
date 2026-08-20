# Test Plan

## Quality strategy

| Layer | Purpose | Owner | Required evidence |
|---|---|---|---|
| Unit | business rules and edge cases | implementer | CI result |
| Integration | API/data boundaries | backend/database | CI result |
| End-to-end | critical user journeys | QA | run, screenshots where useful |
| Accessibility | keyboard, semantic and automated checks | frontend + QA | report/manual notes |
| Security | authz, input handling, dependency/secrets checks | reviewer | checklist/Action |

## Release-critical journeys

| ID | Journey | Preconditions | Expected outcome | Automation | Owner |
|---|---|---|---|---|---|
| TC-001 | <primary journey> | <state> | <outcome> | Yes / No | QA |

## Entry and exit criteria

**Ready for test:** deployed/locally runnable change, acceptance criteria linked, test data available, no known environment blocker.  
**Ready to merge:** relevant tests pass, critical acceptance criteria evidenced, review completed, no unresolved critical/high defect without explicit human waiver.  
**Ready to release:** merged PRs, Actions green, migration/rollback plan verified where relevant, release approver accepts residual risks.

## Defect severity

| Severity | Meaning | Release policy |
|---|---|---|
| Critical | data loss, security exposure, primary service unavailable | block |
| High | core journey materially fails | block unless human waiver |
| Medium | usable workaround exists | triage |
| Low | cosmetic/minor friction | backlog |
