# Awesome Flight Data [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

A careful list of APIs for flight prices, booking links, ticketing, flight status, tracking, schedules, and adjacent travel inventory.

Last checked: 2026-06-12. Public pricing and access rules change often; treat the pricing column as a pointer to currently published terms, not a quote.

## Contents

- [Live self-serve / public-ish APIs](#live-self-serve--public-ish-apis)
- [Live partner, contract, or enterprise APIs](#live-partner-contract-or-enterprise-apis)
- [Dead, deprecated, or closing APIs](#dead-deprecated-or-closing-apis)
- [Choosing an API by use case](#choosing-an-api-by-use-case)
- [Contributing](#contributing)
- [License](#license)

## Live self-serve / public-ish APIs

| API | Offers | Access model | Indicative pricing/status | Notes |
| --- | --- | --- | --- | --- |
| [Ignav](https://ignav.com/pricing) | Fare search, booking links, airport search | Self-serve | 1,000 free requests, then $2.00 per 1,000 successful requests; no monthly minimums; no authenticated rate limits | Small usage-based API for apps and agents that need flight prices plus booking URLs. |
| [SerpApi Google Flights API](https://serpapi.com/google-flights-api) | Fare-search results and price insights | Self-serve scraping API | Free plan lists 250 searches/month; paid and enterprise plans are published/contact-sales | Useful when you want Google Flights-shaped result data and can accept scraping-style semantics. |
| [TubeText Google Flights](https://apify.com/tubetext/google-flights-scraper) | Route/date fare snapshots, optional price insights and date calendar | Self-serve Apify Actor; Apify account required | Usage-based; [current pricing](https://apify.com/tubetext/google-flights-scraper/pricing) | Structured public Google Flights observations for comparison; not ticketing or a historical purchased-ticket dataset. Fares can change after collection. |
| [FlightLabs](https://www.goflightlabs.com/) | Status/tracking, schedules, routes, airport data, advertised flight prices | Self-serve | Public site lists a 7-day/50-request trial and paid plans starting at Starter tier | Broad aviation-data API with a price endpoint; verify fare coverage for your markets. |
| [aviationstack](https://aviationstack.com/pricing) | Status/tracking, historical flights, schedules, routes, airport/airline data | Self-serve | Free plan available; commercial and advanced features require paid plans | Better fit for flight status and aviation reference data than fare shopping. |
| [Travelpayouts / Aviasales Data API](https://travelpayouts.github.io/slate/) | Cached prices, popular destinations, route trends | Affiliate registration/token | Pricing is not a simple public API tariff; access is tied to the Travelpayouts affiliate network | Official docs say data comes from cached Aviasales search history and is recommended for static pages. |
| [RapidAPI flight data APIs](https://rapidapi.com/collection/flight-data-apis) | Marketplace entries for fare search, status, schedules, and scrapers | Public-ish marketplace | Varies by provider | Treat third-party scraper listings carefully: uptime, provenance, rights, and source-site ToS vary. |
| [FlightAware AeroAPI](https://www.flightaware.com/commercial/aeroapi) | Flight status, tracking, historical tracks, alerts, predictive data | Self-serve tiers plus commercial terms | Personal has no monthly minimum and limited free monthly credit; Standard/Premium list monthly minimums plus per-query fees | Mature operational tracking API; not a fare-search or ticketing API. |
| [AeroDataBox](https://aerodatabox.com/) | Flight status, schedules, airport FIDS, history, aircraft/airport data | Public marketplace plans | Free/trial and paid marketplace tiers; direct access is generally custom | Practical status/schedule data for small teams; check endpoint tier costs before building. |
| [AirLabs](https://airlabs.co/) | Live flight data, schedules, routes, airports, airlines, IATA/ICAO data | Self-serve | Free and paid plans are advertised; check current plan limits before purchase | Lightweight aviation data hub, not a booking or ticketing system. |
| [Aviation Edge](https://aviation-edge.com/) | Flight tracker, real-time/future/historical schedules, routes, delays, ticket-price endpoint | Self-serve | Public pricing shows discounted first-month trials and higher renewal prices | Broad aviation datasets; read renewal pricing and coverage notes closely. |
| [Flightradar24 API](https://fr24api.flightradar24.com/) | Real-time aircraft positions, historical tracks, airline/airport reference data | Self-serve subscription | Public subscription page lists plans starting at $9/month | Strong for aircraft movement and ADS-B-backed tracking; not fare search or ticketing. |
| [OpenSky Network API](https://openskynetwork.github.io/opensky-api/) | Live airspace state vectors and ADS-B-derived flight data | Public/research | Free public API with research/non-commercial framing | Excellent for research and aircraft-position projects; official docs say it does not provide commercial schedules or delay data. |

## Live partner, contract, or enterprise APIs

| API | Offers | Access model | Indicative pricing/status | Notes |
| --- | --- | --- | --- | --- |
| [Duffel](https://duffel.com/flights) | Flight search, booking, orders, payments, ancillaries, managed content | Business onboarding; public docs and pricing | Public pricing lists per confirmed-order and ancillary fees, plus excess-search fees | The right answer if you need ticketing, order management, changes, and ancillaries rather than just booking links. |
| [Amadeus Enterprise APIs](https://developers.amadeus.com/enterprise) | Flight search, booking, ticketing, hotels, destination and travel content | Enterprise/contact-sales | Pricing is not public; Amadeus says enterprise pricing requires qualification and typically NDA | Enterprise path remains available even as Self-Service is being decommissioned. |
| [Sabre APIs](https://developer.sabre.com/) | Low-fare search, offers, booking management, PNR/ticketing, GDS/NDC workflows | Contract/developer credentials | Public pricing not clear; expect commercial agreement | Strong option for agencies and OTAs that need established GDS and ticketing workflows. |
| [Travelport TripServices / Universal API](https://developer.travelport.com/) | Air search, pricing, booking, ticketing, exchanges, NDC/GDS content | Customer/developer portal; sales-led access | Pricing not public | Full travel-retailing platform for agencies; heavier onboarding than simple data APIs. |
| [Skyscanner Travel APIs](https://www.partners.skyscanner.net/product/travel-api) | Flights live prices, indicative prices, routes, autosuggest and geo data | Partner application/commercial agreement | Pricing not public; partner approval required | Strong metasearch and referral product. Skyscanner support says API access is only via commercial agreement and approval. |
| [Kiwi.com Tequila / B2B platform](https://media.kiwi.com/articles-and-interviews/better-for-business-kiwi-com-takes-a-new-approach-to-partnerships/) | Flight search and booking services for selected B2B partners | Invitation-only partnerships | Pricing not public | Current public posture appears selected-partner access, not broad developer self-serve. |
| [Expedia Group Rapid Flight API](https://developers.expediagroup.com/rapid/flights) | Flight shopping, price/details verification, seat maps, booking, itinerary retrieval | Expedia partner onboarding | Pricing not public | Useful when you want an Expedia Group booking path across flights and adjacent travel inventory. |
| [KAYAK Affiliate Network/API](https://affiliates.kayak.com/) | Deeplinks, widgets, search box, API, autocomplete, affiliate reporting | Affiliate approval/contact | Public pricing not shown; affiliate revenue model | Best fit for click-out and affiliate monetization, not owning ticketing operations. |
| [Booking.com Demand API](https://developers.booking.com/demand) | Stays, cars, attractions, orders, and some flight-related surfaces | Managed Affiliate Partner access | Pricing not public | Adjacent travel API. Booking.com pages mention flights in some API references while the product page marks flights as coming soon, so treat flight capability as partner-dependent. |
| [OAG Flight Info API](https://www.oag.com/flight-info-api) | Schedules, status, connections, seats and operational flight data | Developer/enterprise access | Pricing not public | Longstanding aviation-data provider for schedule/status-heavy products and operations. |
| [Cirium Developer Studio](https://www.cirium.com/data/aviation-api/) | Status, tracking, alerts, schedules, connections, weather, fleet, NOTAMs, emissions | Evaluation account/contact-sales | Pricing not public | Deep aviation datasets for operations, analytics, and status/schedule use cases. |

## Dead, deprecated, or closing APIs

| API | Former offers | Access model | Status | Notes |
| --- | --- | --- | --- | --- |
| [Google QPX Express](https://duffel.com/blog/google-flights-api) | Airfare search | Dead | Shut down in 2018 | The old public Google/ITA airfare API is gone; current Google Flights does not offer the same public developer API. |
| [Amadeus Self-Service APIs](https://developers.amadeus.com/) | Self-serve travel APIs including flight search/booking examples | Closing | Amadeus says the Self-Service portal will be decommissioned on July 17, 2026 | Existing users should verify migration options. Amadeus Enterprise APIs are separate and remain available by contact. |
| [Kiwi.com Tequila self-serve access](https://media.kiwi.com/articles-and-interviews/better-for-business-kiwi-com-takes-a-new-approach-to-partnerships/) | Flight search and booking API for developers/partners | Closed to broad self-serve | Public self-serve access appears closed; new Tequila partnerships are invitation-only | Existing selected partners may still have B2B platform access. |

## Choosing an API by use case

- Need simple fare search plus booking links: start with Ignav, SerpApi, FlightLabs, or carefully vetted marketplace APIs.
- Need to sell and service tickets: start with Duffel. Consider Amadeus Enterprise, Sabre, or Travelport when you need GDS/NDC contracts, agency workflows, ticketing, exchanges, and settlement depth.
- Need metasearch or affiliate click-out: Skyscanner, KAYAK, Travelpayouts, Expedia, and Booking.com are closer fits than ticketing APIs.
- Need operational status, schedules, tracking, or airport displays: FlightAware, OAG, Cirium, aviationstack, FlightLabs, AeroDataBox, AirLabs, Aviation Edge, Flightradar24, and OpenSky are the relevant set.
- Need static SEO pages or trend pages: cached/indicative sources such as Travelpayouts and Skyscanner indicative prices may fit better than live-shopping APIs.
- Need research-grade aircraft positions: OpenSky is useful, but it is not commercial fare/status data and does not replace schedules or delay feeds.
- Avoid building new products on dead or closing APIs. Google QPX Express is gone, Amadeus Self-Service is closing on July 17, 2026, and broad Kiwi Tequila self-serve access appears closed.

## Contributing

Factual PRs are welcome. Please cite official, current sources where possible; use conservative wording when access, pricing, or status is unclear. Keep entries concise, avoid affiliate spam and referral links, and do not add unverifiable pricing.

## License

CC0-1.0. See [LICENSE](LICENSE).
