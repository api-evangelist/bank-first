# Bank First (bank-first)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

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
