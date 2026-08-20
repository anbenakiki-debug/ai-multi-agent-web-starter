# API Contract

## Rules

- Define APIs before parallel frontend/backend implementation begins.
- Specify authentication, authorization, validation, error format, pagination, idempotency, and versioning where applicable.
- Never expose internal errors, secrets, or fields not intended for the caller.

## Common conventions

**Base URL:** `<environment URL>/api`  
**Format:** JSON over HTTPS  
**Errors:** `{ "error": { "code": "VALIDATION_ERROR", "message": "…", "fields": {} } }`

## Endpoint template

### `POST /v1/<resource>` — <purpose>

**Auth:** <none / role/permission>  
**Request:**

```json
{ "name": "example" }
```

**Success:** `201`

```json
{ "id": "<id>", "name": "example" }
```

**Errors:** `400` malformed input; `401` unauthenticated; `403` unauthorized; `409` conflict; `422` validation.  
**Acceptance / test:** <FR ID, test ID, Issue link>
