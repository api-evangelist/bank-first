---
name: Look up Bank First banking products
description: >-
  Browse and inspect Bank First's publicly offered banking products via the CDR
  Product Reference Data API. Fully public and unauthenticated — no key or token.
api: openapi/bank-first-cds-banking-products-openapi.yml
operations:
  - listBankingProducts
  - getBankingProductDetail
---

# Look up Bank First banking products

Bank First exposes a public, unauthenticated Consumer Data Right (CDR) Product
Reference Data API. Use it to list products and fetch full detail. No credentials
are required.

Base URL: `https://public.cdr.bankfirst.com.au/cds-au/v1/banking`

## Rules

- Send an `x-v: 3` request header on every call (the API negotiates version via
  `x-v` / `x-min-v`; the response echoes the served version in `x-v`).
- No `Authorization` header — this surface is public.
- Responses are `application/json`.
- Errors use the CDR envelope `{ "errors": [ { "code", "title", "detail" } ] }`
  with URN codes like `urn:au-cds:error:cds-all:Resource/Invalid` (see
  `errors/bank-first-problem-types.yml`).

## Steps

1. **List products** — call `listBankingProducts`:
   `GET /banking/products` with header `x-v: 3`.
   Optional query params: `effective` (`CURRENT` default / `FUTURE` / `ALL`),
   `product-category`, `page`, `page-size` (default 25, max 1000).
   Read `data.products[]`, `meta.totalRecords` / `meta.totalPages`, and the
   `links` object (`self`/`first`/`prev`/`next`/`last`) to paginate.

2. **Pick a product** — take a `productId` from a `data.products[]` entry.

3. **Get product detail** — call `getBankingProductDetail`:
   `GET /banking/products/{productId}` with header `x-v: 3`.
   The detail payload adds `bundles`, `features`, `constraints`, `eligibility`,
   `fees`, `depositRates`, and `lendingRates`.

## Notes

- A `404` with `urn:au-cds:error:cds-all:Resource/Invalid` means the `productId`
  is malformed or unknown — re-fetch it from `listBankingProducts`.
- A `406` `Header/UnsupportedVersion` means the requested `x-v` is unsupported;
  retry with `x-v: 3`.
- This skill covers only the public product catalog. Account, balance, and
  transaction data require CDR accreditation and the consent flow (see
  `authentication/bank-first-authentication.yml`).
