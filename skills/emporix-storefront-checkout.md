---
name: emporix-storefront-checkout
description: 'Run a storefront purchase: cart, items, payment mode, checkout and order lookup.'
api: openapi/emporix-checkout-openapi.yml
operations:
- POST-cart-create-cart
- POST-cart-add-item-to-cart
- GET-payment-gateway-list-payment-modes-frontend
- POST-checkout-trigger-checkout
- GET-order-retrieve-order-storefront
generated: '2026-10-18'
method: generated
---

# emporix-storefront-checkout

Run a storefront purchase: cart, items, payment mode, checkout and order lookup.

## Steps

1. `POST-cart-create-cart` — Create a cart for the session/customer.
2. `POST-cart-add-item-to-cart` — Add product items to the cart.
3. `GET-payment-gateway-list-payment-modes-frontend` — List payment modes available to the storefront.
4. `POST-checkout-trigger-checkout` — Trigger checkout with the customer access token to place the order.
5. `GET-order-retrieve-order-storefront` — Retrieve the placed order (order.history_view or customer token).

## Rules

- Base URL https://api.emporix.io; send `Authorization: Bearer <token>`.
- Checkout requires a CustomerAccessToken per the spec security; obtain it via emporix-authenticate.
