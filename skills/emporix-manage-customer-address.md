---
name: emporix-manage-customer-address
description: Create, retrieve, update, and delete customer addresses through their lifecycle.
api: openapi/emporix-customer-management-openapi.yml
operations:
- POST-customer-add-address
- GET-customer-retrieve-address-by-id
- PATCH-customer-update-customer-address
- DELETE-customer-remove-customer-address-by-id
generated: '2026-10-18'
method: generated
generator: extract-docs-artifacts.py skills (deepseek)
source: openapi/emporix-customer-management-openapi.yml ; every operationId checked against the contract
---

# emporix-manage-customer-address

Create, retrieve, update, and delete customer addresses through their lifecycle.

## Steps

1. 1. Create a new customer address using `POST-customer-add-address` with the required address fields in the request body
2. 2. Retrieve the created address using `GET-customer-retrieve-address-by-id` with the `addressId` from the creation response
3. 3. Update the address using `PATCH-customer-update-customer-address` with the `addressId` and partial update fields in the request body
4. 4. Delete the address using `DELETE-customer-remove-customer-address-by-id` with the `addressId`

## Rules

- Authentication required using CustomerAccessToken or OAuth2 schemes
- All operations require the `tenant` path parameter
- Address-specific operations require the `addressId` path parameter
- POST operations require address data in the request body
