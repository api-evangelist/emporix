---
name: emporix-custom-entities
description: Extend Emporix with a custom entity type and manage its instances via the Schema Service.
api: openapi/emporix-schema-openapi.yml
operations:
- POST-schema-create-custom-schema-type
- POST-schema-create-custom-instance
- POST-schema-search-custom-instances
- PATCH-schema-patch-custom-instance
generated: '2026-10-18'
method: generated
---

# emporix-custom-entities

Extend Emporix with a custom entity type and manage its instances via the Schema Service.

## Steps

1. `POST-schema-create-custom-schema-type` — Define the custom entity type (schema.schema_manage).
2. `POST-schema-create-custom-instance` — Create an instance of the type.
3. `POST-schema-search-custom-instances` — Search instances.
4. `PATCH-schema-patch-custom-instance` — Patch an instance.

## Rules

- Base URL https://api.emporix.io; send `Authorization: Bearer <token>`.
- Instance scopes are schema.custominstance_* or custom.{lowerCaseType}_*. See the provider emporix-extensibility skill.
