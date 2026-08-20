# Database Contract

## Principles

- A migration is the authoritative schema history; do not alter production data manually.
- Every schema change has a migration, rollback/forward recovery plan, owner, and linked Issue/PR.
- Store the minimum necessary personal data; document retention and access controls before collecting it.

## Entity template

### `<entity>`

| Field | Type | Null? | Constraints / meaning | Classification |
|---|---|---|---|---|
| `id` | UUID / bigint | No | primary key | internal |
| `created_at` | timestamp | No | creation time | internal |

**Indexes:** <index and query it supports>  
**Relationships:** <cardinality / foreign keys>  
**Invariants:** <rules that must always hold>  
**Retention/deletion:** <policy>  
**Migration notes:** <backfill/lock/rollback consideration>

## Migration checklist

- [ ] Backwards-compatible deployment order defined, or maintenance window approved.
- [ ] Index and query impact reviewed.
- [ ] Backfill, rollback, and monitoring plan recorded if data is changed.
- [ ] Test data and privacy implications considered.
