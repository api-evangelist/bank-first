# Bank First (bank-first)

Bank First is an Australian customer-owned mutual bank headquartered in Hawthorn East, Victoria. Founded in 1972 as VTU Credit Union by members of the Victorian Teachers Union and rebranded from Victoria Teachers Mutual Bank in December 2017, it is owned by its 90,000-plus members rather than external shareholders and serves the education and healthcare communities. As an Authorised Deposit-taking Institution (ADI), Bank First is a data holder under Australia's Consumer Data Right (CDR / Open Banking) and publishes a public, unauthenticated Product Reference Data API built to the Data Standards Body Consumer Data Standards.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/bank-first/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/bank-first/refs/heads/main/apis.yml)

## Tags

- Financial
- Banks
- Open Banking
- CDR
- Consumer Banking
- Australia
- Mutual Bank
- Product Reference Data

## Timestamps

- **Created:** 2026-07-20
- **Modified:** 2026-07-20

## APIs

### Bank First CDR Product Reference Data API

Public, unauthenticated Consumer Data Right Product Reference Data (PRD) API conforming to the DSB Consumer Data Standards. Exposes `GET /banking/products` (a paginated list of Bank First's publicly offered products) and `GET /banking/products/{productId}` (full detail for a single product). Confirmed live on 2026-07-20 returning HTTP 200 with header `x-v: 3` and a `data.products` array of 176 records. No authentication or registration is required.

- **Human URL:** [https://www.bankfirst.com.au/open-banking](https://www.bankfirst.com.au/open-banking)
- **Base URL:** `https://public.cdr.bankfirst.com.au/cds-au/v1/banking`

#### Tags

- CDR
- Open Banking
- Product Reference Data
- Banking Products
- Australia

#### Properties

- [Documentation](https://www.bankfirst.com.au/open-banking)
- [API Reference](https://consumerdatastandardsaustralia.github.io/standards/#banking-products)
- [OpenAPI](openapi/bank-first-cds-banking-products-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

> The harvested OpenAPI is the shared DSB Consumer Data Standards "CDR Banking API" (v1.36.0), captured verbatim — not a Bank First proprietary contract. Bank First's PRD endpoint conforms to its `getProducts` and `getProductDetail` operations.

## Common Properties

- [Website](https://www.bankfirst.com.au/)
- [About](https://www.bankfirst.com.au/about-us)
- [Developer Portal](https://www.bankfirst.com.au/open-banking)
- [Documentation](https://consumerdatastandardsaustralia.github.io/standards/)
- [Privacy Policy](https://www.bankfirst.com.au/privacy-policy)
- [Terms of Service](https://www.bankfirst.com.au/disclosure-documents)
- [Support](https://www.bankfirst.com.au/contact-us)
- [LinkedIn](https://www.linkedin.com/company/bank-first)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
