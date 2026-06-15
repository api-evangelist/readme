# ReadMe (readme)

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
