---
name: emporix-create-update-customer-profile
description: Create or update a customer profile in the Emporix system.
api: openapi/emporix-customer-management-openapi.yml
operations:
- POST-customer-tenant-create-customer
- GET-customer-tenant-retrieve-customer
- PUT-customer-tenant-update-customer
generated: '2026-10-18'
method: generated
generator: extract-docs-artifacts.py skills (deepseek)
source: openapi/emporix-customer-management-openapi.yml ; every operationId checked against the contract
---

# emporix-create-update-customer-profile

Create or update a customer profile in the Emporix system.

## Steps

1. 1. Create a new customer using `POST-customer-tenant-create-customer` with the required customer data fields
2. 2. Retrieve the created customer profile using `GET-customer-tenant-retrieve-customer` with the customerNumber from the creation response
3. 3. Update the customer profile using `PUT-customer-tenant-update-customer` with the customerNumber and updated fields
4. 4. Verify the update by retrieving the customer profile again using `GET-customer-tenant-retrieve-customer` with the same customerNumber

## Rules

- Authentication is required using CustomerAccessToken, OAuth2, or AnonymousAccessToken schemes
- All customer operations require the tenant parameter in the URL path
- Customer updates require the customerNumber parameter in the URL path for specific customer operations
