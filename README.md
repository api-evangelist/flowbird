# Flowbird (flowbird)

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
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Flowbird is a global urban mobility and parking technology company that builds pay stations, mobile parking apps, digital permits, EV charging, and transit ticketing systems for cities and transport authorities worldwide. Flowbird was **acquired by EasyPark Group** in an acquisition that closed in **January 2025**. Its integration surface is the **Flowbird HUB**, an open platform that exposes documented but **partner/agency-gated** APIs (OAuth2 and client-certificate secured, with role-based access control and ownership filters) for tariffs, rights/permits, parking sessions, pay stations, and transactions.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/flowbird/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/flowbird/refs/heads/main/apis.yml)

## Access Model (Read This First)

Flowbird does **not** offer self-service, public API sign-up. The integration surface is the **Flowbird HUB**, documented at [docs.flowbirdhub.com](https://docs.flowbirdhub.com/) (Stoplight) and secured with **OAuth2 and client certificates**, with role-based access control and ownership filters. Access is granted to cities, transport agencies, and integration partners under contract; the live endpoint reference is not publicly crawlable. The Flowbird HUB API entries in `apis.yml` are therefore **modeled logical APIs** (`endpointsModeled: true`) derived from Flowbird's published platform descriptions, not scraped from a public reference.

**Pricing is contract/tender-based** (municipal procurement, G-Cloud listings) and is not published as public tiers, so no `plans/` is included. No public WebSocket API is offered (see `review.yml`).

> **Ownership note:** Flowbird is owned by EasyPark Group. The **ParkWhiz / BestParking** parking product and its v4 developer API are **not** part of Flowbird — that lineage (ParkWhiz + BestParking → Arrive/Arrive Mobility) merged into **FlashParking (Flash)** in January 2021 and is cataloged separately as `all/parkwhiz`. Flowbird does not own or expose the ParkWhiz/Arrive API.

## Tags

- Parking
- Urban Mobility
- Transit Ticketing
- Payments
- Smart City
- Pay Stations
- EV Charging
- Digital Permits
- Partner Gated

## Timestamps

- **Created:** 2026-07-03
- **Modified:** 2026-07-03

## APIs

### Flowbird HUB Parking Sessions API

Start, stop, extend, and query active and historical parking sessions across pay-station, mobile-app, and permit channels, and expose real-time session state to enforcement and occupancy consumers. *Endpoints modeled from Flowbird HUB platform descriptions; live reference is OAuth2/certificate secured and contract-gated.*

- **Human URL:** [https://docs.flowbirdhub.com/](https://docs.flowbirdhub.com/)

#### Tags

- Parking Sessions
- Mobile Parking
- Enforcement

### Flowbird HUB Tariffs and Rights API

Configure and read parking tariffs, pricing rules, and rights (digital permits, subscriptions, eligibility) consistently across every sales channel. Flowbird documents that tariffs and rights can be managed through the HUB UI or via the API. *Endpoints modeled; live surface is partner/agency-gated.*

- **Human URL:** [https://docs.flowbirdhub.com/](https://docs.flowbirdhub.com/)

#### Tags

- Tariffs
- Rights
- Permits

### Flowbird HUB Pay Stations API

Retrieve the inventory, configuration, health/status, and collection (coin, card, cash) data for Flowbird pay stations and terminals managed by the central platform. *Endpoints modeled; documented live API is certificate-secured and access-scoped per contract.*

- **Human URL:** [https://docs.flowbirdhub.com/](https://docs.flowbirdhub.com/)

#### Tags

- Pay Stations
- Terminals
- Assets

### Flowbird HUB Transactions API

Read parking and mobility payment transactions and revenue/reporting data across channels for reconciliation and analytics, with role-based access and ownership filters. Bulk export is also available via Flowbird's service desk. *Endpoints modeled; live API is OAuth2/certificate secured and contract-gated.*

- **Human URL:** [https://docs.flowbirdhub.com/](https://docs.flowbirdhub.com/)

#### Tags

- Transactions
- Payments
- Reporting

## Common Properties

- [LinkedIn](https://www.linkedin.com/company/flowbird)
- [Website](https://www.flowbird.group)
- [Documentation](https://docs.flowbirdhub.com/)
- [Partner Access](https://www.flowbird.com/customer-partner-access/)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
