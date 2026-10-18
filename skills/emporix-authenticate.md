---
name: emporix-authenticate
description: 'Obtain the right Emporix access token: service (client credentials) token for backend calls, anonymous token for storefront sessions, and customer token after login.'
api: openapi/emporix-oauth-service-openapi.yml
operations:
- POST-oauth-request-client-credentials
- GET-oauth-generate-anonymous-access-token
- POST-customer-authenticate-customer
generated: '2026-10-18'
method: generated
---

# emporix-authenticate

Obtain the right Emporix access token: service (client credentials) token for backend calls, anonymous token for storefront sessions, and customer token after login.

## Steps

1. `POST-oauth-request-client-credentials` — Request a service access token (POST /oauth/token, client_credentials) with your API key client ID/secret; use it as `Authorization: Bearer` on tenant APIs.
2. `GET-oauth-generate-anonymous-access-token` — For storefront flows, request an anonymous token (GET /customerlogin/auth/anonymous/login).
3. `POST-customer-authenticate-customer` — Log the customer in with the anonymous token to receive a customer access token.

## Rules

- Base URL https://api.emporix.io; send `Authorization: Bearer <token>`.
- Scopes are attached to the API key; a 401 means an invalid/expired token, a 403 a missing scope (see the provider emporix-auth skill in skills/_original/).
