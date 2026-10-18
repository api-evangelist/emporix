---
name: emporix-retrieve-and-update-order-status
description: Retrieve order details and update order status transitions for customer-managed orders.
api: openapi/emporix-order-openapi.yml
operations:
- GET-order-retrieve-order-storefront
- GET-order-retrieve-transitions
- POST-order-update-order-transition-storefront
generated: '2026-10-18'
method: generated
generator: extract-docs-artifacts.py skills (deepseek)
source: openapi/emporix-order-openapi.yml ; every operationId checked against the contract
---

# emporix-retrieve-and-update-order-status

Retrieve order details and update order status transitions for customer-managed orders.

## Steps

1. 1. Retrieve order details using `GET-order-retrieve-order-storefront` with the `tenant` and `orderId` path parameters
2. 2. Check order status transitions using `GET-order-retrieve-transitions` with the `tenant` and `orderId` path parameters
3. 3. Update order status using `POST-order-update-order-transition-storefront` with the `tenant` and `orderId` path parameters and the required request body fields

## Rules

- Use CustomerAccessToken or OAuth2 authentication schemes for customer-managed resources
- All operations require the `tenant` path parameter to identify the tenant context
- The `orderId` path parameter is required for order-specific operations
- Operations use the base server URL https://api.emporix.io
