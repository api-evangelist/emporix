---
name: emporix-product-onboarding
description: 'Create a sellable product in Emporix: product, price, availability and category assignment, then verify.'
api: openapi/emporix-product-service-openapi.yml
operations:
- POST-product-create-product
- POST-price-create-price
- POST-availability-add-product
- POST-category-tree-assign-resource
- GET-product-retrieve-product
generated: '2026-10-18'
method: generated
---

# emporix-product-onboarding

Create a sellable product in Emporix: product, price, availability and category assignment, then verify.

## Steps

1. `POST-product-create-product` — Create the product (scope product.product_manage).
2. `POST-price-create-price` — Create its price (price.price_manage).
3. `POST-availability-add-product` — Create availability for the product on a site (availability.availability_manage).
4. `POST-category-tree-assign-resource` — Assign the product to a category (category.category_manage).
5. `GET-product-retrieve-product` — Read the product back to confirm.

## Rules

- Base URL https://api.emporix.io; send `Authorization: Bearer <token>`.
- All calls use a service access token; paths are tenant-scoped (/{tenant}/...).
