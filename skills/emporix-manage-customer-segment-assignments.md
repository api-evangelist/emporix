---
name: emporix-manage-customer-segment-assignments
description: Manage customer assignments to customer segments including retrieving, updating, and removing assignments.
api: openapi/emporix-customer-segments-openapi.yml
operations:
- GET-customer-segment-retrieve-customers
- POST-customer-segment-search-customers
- PUT-customer-segment-update-customer-by-customerId
- PUT-customer-segment-update-customer
- DELETE-customer-segment-remove-customer-by-customerId
- DELETE-customer-segment-remove-customer
- PUT-customer-segment-update-customers-bulk
- DELETE-customer-segment-remove-customers-bulk
generated: '2026-10-18'
method: generated
generator: extract-docs-artifacts.py skills (deepseek)
source: openapi/emporix-customer-segments-openapi.yml ; every operationId checked against the contract
---

# emporix-manage-customer-segment-assignments

Manage customer assignments to customer segments including retrieving, updating, and removing assignments.

## Steps

1. 1. Retrieve all customer assignments for a segment using `GET-customer-segment-retrieve-customers` with `tenant` and `segmentId` path parameters
2. 2. Search for specific customer assignments using `POST-customer-segment-search-customers` with `tenant` and `segmentId` path parameters and search parameters in the request body
3. 3. Update individual customer assignments using `PUT-customer-segment-update-customer-by-customerId` (B2C) or `PUT-customer-segment-update-customer` (B2B) with `tenant`, `segmentId`, `customerId`, and optional `legalEntityId` path parameters
4. 4. Remove customer assignments using `DELETE-customer-segment-remove-customer-by-customerId` (B2C) or `DELETE-customer-segment-remove-customer` (B2B) with `tenant`, `segmentId`, `customerId`, and optional `legalEntityId` path parameters
5. 5. Perform bulk operations using `PUT-customer-segment-update-customers-bulk` for bulk updates or `DELETE-customer-segment-remove-customers-bulk` for bulk removals with `tenant` and `segmentId` path parameters

## Rules

- Authentication requires one of: AnonymousAccessToken, CustomerAccessToken, OAuth2, or oAuth2 authorization headers
- All operations require `tenant` and `segmentId` path parameters
- B2C operations use `customerId` only, while B2B operations require both `customerId` and `legalEntityId` path parameters
- Bulk operations use the `/bulk` endpoint for updating or removing multiple customer assignments at once
