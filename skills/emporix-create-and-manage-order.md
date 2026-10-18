---
name: emporix-create-and-manage-order
description: Create a new order and manage it through its complete lifecycle including updates, status changes, and calculations.
api: openapi/emporix-order-openapi.yml
operations:
- POST-order-create-order-employee
- GET-order-retrieve-order-employee
- PUT-order-update-order
- POST-order-update-order-transition-employee
- POST-order-calculate-order-entries-employees
generated: '2026-10-18'
method: generated
generator: extract-docs-artifacts.py skills (deepseek)
source: openapi/emporix-order-openapi.yml ; every operationId checked against the contract
---

# emporix-create-and-manage-order

Create a new order and manage it through its complete lifecycle including updates, status changes, and calculations.

## Steps

1. 1. Create a new order using `POST-order-create-order-employee` with order details in the request body
2. 2. Retrieve the created order using `GET-order-retrieve-order-employee` with the `orderId` from the response
3. 3. Update the order using `PUT-order-update-order` with the `orderId` and updated order data
4. 4. Update order status using `POST-order-update-order-transition-employee` with the `orderId` and transition data
5. 5. Recalculate order entries using `POST-order-calculate-order-entries-employees` with the `orderId`

## Rules

- Use OAuth2 or oAuth2 authentication scheme
- Include the `tenant` parameter in all paths
- Include the `orderId` parameter for operations targeting specific orders
