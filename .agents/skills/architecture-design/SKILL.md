---
name: architecture-design
description: Select and document a pragmatic architecture tied to requirements.
---

# Architecture Design

## Steps

1. Trace components and quality attributes to accepted FR/NFR IDs.
2. Present viable alternatives for material decisions with costs, failure modes, and reversibility.
3. Choose the simplest design that meets current constraints; default to modular monolith.
4. Document components, boundaries, contracts, quality evidence in `ARCHITECTURE.md` and `API.md`/`DATABASE.md`.
5. Record accepted material choice as an ADR. Escalate security, data, billing, vendor lock-in, and irreversible changes.

## Exit criteria

Implementation agents can work independently because interfaces, dependencies, data ownership, and error handling are explicit.
