---
name: emporix-returns
description: Create a return for an Emporix order, track its state, and partially update it (for example its status) through the Returns Service.
api: openapi/emporix-returns-openapi.yml
operations:
- POST-returns-create-return
- GET-returns-retrieve-return
- PATCH-returns-update-return
generated: '2026-10-18'
method: generated
---

# emporix-returns

Create and track a return for an order.

## Steps

1. `POST-returns-create-return` — Create a return (returns.returns_manage or returns.returns_manage_own).
2. `GET-returns-retrieve-return` — Retrieve the return to check its state.
3. `PATCH-returns-update-return` — Partially update the return, e.g. its status.

## Rules

- Base URL https://api.emporix.io; send `Authorization: Bearer <token>`.
- The documented MCP tools create-return / get-return / partial-update-return map to these operations.
