---
name: emporix-import-run
description: Trigger and monitor an Import Tool run, then retry failures.
api: openapi/emporix-import-service-openapi.yml
operations:
- GET-importtool-list-configs
- POST-importtool-trigger-run
- GET-importtool-get-run
- GET-importtool-list-run-errors
- POST-importtool-retry-run
generated: '2026-10-18'
method: generated
---

# emporix-import-run

Trigger and monitor an Import Tool run, then retry failures.

## Steps

1. `GET-importtool-list-configs` — List import configurations to pick one.
2. `POST-importtool-trigger-run` — Trigger a run for the configuration (importtool.import_trigger).
3. `GET-importtool-get-run` — Poll the run status.
4. `GET-importtool-list-run-errors` — Read errors for failed records.
5. `POST-importtool-retry-run` — Retry the failed records.

## Rules

- Base URL https://api.emporix.io; send `Authorization: Bearer <token>`.
- Equivalent MCP tools exist on the importtool domain server (trigger-import-run, get-import-run, ...).
