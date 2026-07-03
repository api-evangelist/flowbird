# Flowbird (flowbird)

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
