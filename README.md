# ReadMe (readme)

ReadMe is a developer hub platform that helps companies design, document, and operate their APIs. The platform combines hosted API reference (OpenAPI-driven), guides and changelog, bi-directional Git sync (GitHub and GitLab), interactive API explorer, Try-It console, Developer Dashboard with real-time API logs, and a deep layer of AI tooling — including the ReadMe Agent for multi-page editing, Inline AI rewrites, the AI Linter for style-guide enforcement, Docs Audit, GitHub AI Writer for PR-triggered doc updates, Ask AI for end users, and Model Context Protocol (MCP) servers for both ReadMe itself and each customer project so AI tools can search, read, update docs, and call APIs.

**URL:** [Visit APIs.yml URL](https://raw.githubusercontent.com/api-evangelist/readme/refs/heads/main/apis.yml)

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
- **Modified:** 2026-05-22

## APIs

### ReadMe API

The ReadMe API (v2) lets you programmatically control your ReadMe developer hub. It manages API definitions, API reference pages, guides, changelog, custom pages, categories, branches (versions), images, recipes, and search. Authentication uses a Bearer API key.

- **Human URL:** [https://docs.readme.com/main/reference/intro-to-the-readme-api](https://docs.readme.com/main/reference/intro-to-the-readme-api)
- **Base URL:** `https://api.readme.com/v2`

**Tags:** Documentation, Developer Hub, Content Management, API Reference

**Properties**

- [Documentation](https://docs.readme.com/main/reference/intro-to-the-readme-api)
- [Authentication](https://docs.readme.com/main/reference/authentication)
- [OpenAPI](openapi/readme-openapi.yml)
- [Capability — APIs](capabilities/readme-apis.yaml)
- [Capability — Guides](capabilities/readme-guides.yaml)
- [Capability — Changelog](capabilities/readme-changelog.yaml)
- [Capability — Custom Pages](capabilities/readme-custom-pages.yaml)
- [Capability — Categories](capabilities/readme-categories.yaml)
- [Capability — Branches](capabilities/readme-branches.yaml)
- [Capability — Images](capabilities/readme-images.yaml)
- [Capability — Search](capabilities/readme-search.yaml)
- [Capability — API Keys](capabilities/readme-api-keys.yaml)

### ReadMe Developer Metrics API

The ReadMe Developer Metrics API powers the Developer Dashboard. It accepts API request logs from Metrics SDKs (Node.js, Python, Ruby, PHP, .NET) and exposes analytics including page quality scores, page view statistics, and search analytics so teams can investigate API usage by key or email and debug requests in real time.

- **Human URL:** [https://docs.readme.com/main/docs/sending-api-logs](https://docs.readme.com/main/docs/sending-api-logs)
- **Base URL:** `https://metrics.readme.io/v1`

**Tags:** Analytics, Metrics, Logging, Developer Dashboard

**Properties**

- [Documentation](https://docs.readme.com/main/docs/sending-api-logs)
- [OpenAPI](openapi/readme-developer-metrics-openapi.yml)
- [SDK Repo (Metrics SDKs)](https://github.com/readmeio/metrics-sdks)
- [Capability — Metrics](capabilities/developer-metrics-metrics.yaml)
- [Capability — Analytics](capabilities/developer-metrics-analytics.yaml)

### ReadMe MCP Server

ReadMe operates a hosted Model Context Protocol (MCP) server that lets AI tools (Claude, Cursor, IDEs, CI pipelines) search, read, and update ReadMe documentation through natural language. ReadMe also auto-provisions a per-project MCP server for every customer so end users' AI tools can read, search, and call that project's API directly.

- **Human URL:** [https://docs.readme.com/main/docs/readmes-mcp-server](https://docs.readme.com/main/docs/readmes-mcp-server)

**Tags:** MCP, AI, Model Context Protocol, Agents

**Properties**

- [Documentation — ReadMe's MCP Server](https://docs.readme.com/main/docs/readmes-mcp-server)
- [Use Cases — ReadMe's MCP Server](https://docs.readme.com/main/docs/readmes-mcp-use-cases)
- [Documentation — Your Project's MCP Server](https://docs.readme.com/main/docs/your-projects-mcp-server)
- [Use Cases — Your Project's MCP Server](https://docs.readme.com/main/docs/your-projects-mcp-use-cases)
- [What is MCP?](https://docs.readme.com/main/docs/mcp-servers)
- [Capability — MCP Bridge](capabilities/readme-mcp.yaml)

## Common Properties

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
- [GitHub Org](https://github.com/readmeio)
- [LinkedIn](https://www.linkedin.com/company/readme)
- [LLMs.txt](https://docs.readme.com/llms.txt)
- [CLI — rdme](https://github.com/readmeio/rdme)
- [Metrics SDKs](https://github.com/readmeio/metrics-sdks)
- [OAS Tooling](https://github.com/readmeio/oas)
- [Auto SDK Generation (api)](https://github.com/readmeio/api)
- [Markdown Parser](https://github.com/readmeio/markdown)
- [MDX Marketplace](https://github.com/readmeio/marketplace)

## Pricing

Sourced from [readme.com/pricing](https://readme.com/pricing).

| Plan | Price | Notes |
|---|---|---|
| Starter | $0 / mo | Free; custom domain, bi-directional sync, interactive API reference, usage metrics. |
| Pro | $250 / mo | Billed annually. Branching, reviews, private docs, MDX components, reusable content. |
| Enterprise | $3,000+ / mo | Annual billing; multi-project, SSO, audit logs, dedicated support. |
| Ask AI add-on | $150 / mo | OpenAI-powered end-user assistant; available on all tiers. |

See [`plans/readme-plans-pricing.yml`](plans/readme-plans-pricing.yml) for the machine-readable definition.

## Rate Limits

ReadMe does not publish numeric rate limits for the v2 API. Throttling is signaled via standard `X-RateLimit-*` headers, `429 Too Many Requests`, and `Retry-After`. The Metrics ingestion endpoint at `metrics.readme.io/v1/request` is designed for high-volume server-side logging and SDKs batch entries automatically.

See [`rate-limits/readme-rate-limits.yml`](rate-limits/readme-rate-limits.yml) for full details.

## FinOps

FOCUS-aligned cost-allocation framework at [`finops/readme-finops.yml`](finops/readme-finops.yml). The ReadMe APIs are unlocked by the hub subscription; there is no per-call consumption price.

## Artifacts

| Type | Path |
|---|---|
| APIs index | [`apis.yml`](apis.yml) |
| OpenAPI | [`openapi/readme-openapi.yml`](openapi/readme-openapi.yml), [`openapi/readme-developer-metrics-openapi.yml`](openapi/readme-developer-metrics-openapi.yml) |
| Capabilities | 10 files in [`capabilities/`](capabilities/) — APIs, Guides, Changelog, Custom Pages, Categories, Branches, Images, Search, API Keys, Metrics, Analytics, and the MCP bridge |
| JSON Schema | 5 schemas in [`json-schema/`](json-schema/) — APIDefinition, Guide, Changelog, Branch, MetricsRequest |
| JSON Structure | [`json-structure/readme-developer-hub-structure.json`](json-structure/readme-developer-hub-structure.json) |
| JSON-LD | [`json-ld/readme-context.jsonld`](json-ld/readme-context.jsonld) |
| Examples | 5 request/response examples in [`examples/`](examples/) |
| Spectral rules | [`rules/readme-rules.yml`](rules/readme-rules.yml) |
| Vocabulary | [`vocabulary/readme-vocabulary.yml`](vocabulary/readme-vocabulary.yml) |
| Plans | [`plans/readme-plans-pricing.yml`](plans/readme-plans-pricing.yml) |
| Rate limits | [`rate-limits/readme-rate-limits.yml`](rate-limits/readme-rate-limits.yml) |
| FinOps | [`finops/readme-finops.yml`](finops/readme-finops.yml) |

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
