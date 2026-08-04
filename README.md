# ReadMe (readme)

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

ReadMe is a developer hub platform that helps companies design, document, and operate their APIs. The platform combines hosted API reference (OpenAPI-driven), guides and changelog, bi-directional Git sync (GitHub and GitLab), interactive API explorer, Try-It console, Developer Dashboard with real-time API logs, and a deep layer of AI tooling — including the ReadMe Agent for multi-page editing, Inline AI rewrites, the AI Linter for style-guide enforcement, Docs Audit, GitHub AI Writer for PR-triggered doc updates, Ask AI for end users, and Model Context Protocol (MCP) servers for both ReadMe itself and each customer project so AI tools can search, read, update docs, and call APIs.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/readme/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/readme/refs/heads/main/apis.yml)

## Scope

- **Type:** Index
- **Position:** Consumer
- **Access:** 3rd-Party

## Tags

- Documentation
- Developer Hub
- API Reference
- Portals
- Analytics
- AI
- MCP
- Bi-Directional Sync

## Timestamps

- **Created:** 2025-01-08
- **Modified:** 2026-05-30

## APIs

### ReadMe API

The ReadMe API (v2) lets you programmatically control your ReadMe developer hub. It manages API definitions, API reference pages, guides, changelog, custom pages, categories, branches (versions), images, recipes, and search. Authentication uses a Bearer API key.

- **Human URL:** [https://docs.readme.com/main/reference/intro-to-the-readme-api](https://docs.readme.com/main/reference/intro-to-the-readme-api)
- **Base URL:** `https://api.readme.com/v2`

#### Tags

- Documentation
- Developer Hub
- Content Management
- API Reference

#### Properties

- [Documentation](https://docs.readme.com/main/reference/intro-to-the-readme-api)
- [Authentication](https://docs.readme.com/main/reference/authentication)
- [OpenAPI](https://raw.githubusercontent.com/api-evangelist/readme/refs/heads/main/openapi/readme-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/readme-developer-metrics.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/readme-developer-metrics.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/readme.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/readme.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### ReadMe Developer Metrics API

The ReadMe Developer Metrics API powers the Developer Dashboard. It accepts API request logs from Metrics SDKs (Node.js, Python, Ruby, PHP, .NET) and exposes analytics including page quality scores, page view statistics, and search analytics so teams can investigate API usage by key or email and debug requests in real time.

- **Human URL:** [https://docs.readme.com/main/docs/sending-api-logs](https://docs.readme.com/main/docs/sending-api-logs)
- **Base URL:** `https://metrics.readme.io/v1`

#### Tags

- Analytics
- Metrics
- Logging
- Developer Dashboard

#### Properties

- [Documentation](https://docs.readme.com/main/docs/sending-api-logs)
- [OpenAPI](https://raw.githubusercontent.com/api-evangelist/readme/refs/heads/main/openapi/readme-developer-metrics-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [SDK](https://github.com/readmeio/metrics-sdks)
- [Postman Collection](collections/readme-developer-metrics.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/readme-developer-metrics.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/readme.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/readme.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### ReadMe MCP Server

ReadMe operates a hosted Model Context Protocol (MCP) server that lets AI tools (Claude, Cursor, IDEs, CI pipelines) search, read, and update ReadMe documentation through natural language. ReadMe also auto-provisions a per-project MCP server for every customer so end users' AI tools can read, search, and call that project's API directly.

- **Human URL:** [https://docs.readme.com/main/docs/readmes-mcp-server](https://docs.readme.com/main/docs/readmes-mcp-server)

#### Tags

- MCP
- AI
- Model Context Protocol
- Agents

#### Properties

- [Documentation](https://docs.readme.com/main/docs/readmes-mcp-server)
- [Use Cases](https://docs.readme.com/main/docs/readmes-mcp-use-cases)
- [Documentation](https://docs.readme.com/main/docs/your-projects-mcp-server)
- [Use Cases](https://docs.readme.com/main/docs/your-projects-mcp-use-cases)
- [Explainer](https://docs.readme.com/main/docs/mcp-servers)
- [Postman Collection](collections/readme-developer-metrics.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/readme-developer-metrics.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/readme.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/readme.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### ReadMe Personalized Docs Webhook

ReadMe's Personalized Docs Webhook is the outbound, customer-hosted webhook the developer hub calls at user sign-in to look up a reader's account data. ReadMe POSTs a JSON body containing the user's email, signs the request with a Stripe-style `ReadMe-Signature` header (`t=<unix-ms>,v0=<hmac-sha256-hex>`) using the project's webhook secret, and expects a JSON response describing the user (apiKey, keys array, server-variable parameters, Basic Auth, GraphQL bearer, etc.) which the hub then merges into the rendered API Reference, Try-It console, and Recipes. The single documented event is the user-data lookup.

- **Human URL:** [https://docs.readme.com/main/docs/personalized-docs-webhook](https://docs.readme.com/main/docs/personalized-docs-webhook)

#### Tags

- Webhooks
- Personalized Docs
- Developer Hub
- Authentication

#### Properties

- [Documentation](https://docs.readme.com/main/docs/personalized-docs-webhook)
- [Explainer](https://docs.readme.com/main/docs/personalized-docs)
- [Documentation](https://docs.readme.com/main/docs/user-data-options)
- [SDK](https://github.com/readmeio/metrics-sdks)
- [AsyncAPI](https://raw.githubusercontent.com/api-evangelist/readme/refs/heads/main/asyncapi/readme-personalized-docs-webhook-asyncapi.yml) — [AsyncAPI Specification](https://www.asyncapi.com/docs/reference/specification/latest)
- [Postman Collection](collections/readme-developer-metrics.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/readme-developer-metrics.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/readme.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/readme.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [Arazzo Workflows](arazzo/) — [Arazzo Specification](https://spec.openapis.org/arazzo/latest.html)
- [Portal](https://readme.com)
- [Getting Started](https://docs.readme.com/main/docs/quickstart)
- [Documentation](https://docs.readme.com)
- [API Reference](https://docs.readme.com/main/reference/intro-to-the-readme-api)
- [Pricing](https://readme.com/pricing)
- [Sign Up](https://dash.readme.com/signup)
- [Login](https://dash.readme.com/login)
- [Blog](https://readme.com/blog)
- [Changelog](https://docs.readme.com/main/changelog)
- [About](https://readme.com/about)
- [Status Page](https://www.readmestatus.com)
- [Terms of Service](https://readme.com/tos)
- [Privacy Policy](https://readme.com/privacy)
- [Git Hub Org](https://github.com/readmeio)
- [LinkedIn](https://www.linkedin.com/company/readme)
- [L L Ms Txt](https://docs.readme.com/llms.txt)
- [C L I](https://github.com/readmeio/rdme)
- [SDK](https://github.com/readmeio/metrics-sdks)
- [Tools](https://github.com/readmeio/oas)
- [Tools](https://github.com/readmeio/api)
- [Tools](https://github.com/readmeio/markdown)
- [Git Hub Action](https://github.com/readmeio/rdme)
- [Marketplace](https://github.com/readmeio/marketplace)
- [Plans](plans/readme-plans-pricing.yml)
- [Rate Limits](rate-limits/readme-rate-limits.yml)
- [Fin Ops](finops/readme-finops.yml)
- [Vocabulary](vocabulary/readme-vocabulary.yml)
- [J S O N L D Context](json-ld/readme-context.jsonld)
- [Spectral Rules](rules/readme-rules.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
