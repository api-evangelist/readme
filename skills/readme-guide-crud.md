---
name: readme-guide-crud
description: Create, retrieve, update, and delete a guide page for a specific branch.
api: openapi/readme-guides-api-openapi.yml
operations:
- postBranchesByBranchGuides
- getBranchesByBranchGuidesBySlug
- putBranchesByBranchGuidesBySlug
- deleteBranchesByBranchGuidesBySlug
generated: '2026-10-04'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/readme-guides-api-openapi.yml ; every operationId checked against the contract
---

# readme-guide-crud

Create, retrieve, update, and delete a guide page for a specific branch.

## Steps

1. 1. `postBranchesByBranchGuides` – requires request body with guide fields.
2. 2. `getBranchesByBranchGuidesBySlug` – requires path parameters `branch` and `slug`.
3. 3. `putBranchesByBranchGuidesBySlug` – requires path parameters `branch`, `slug` and request body with updated guide fields.
4. 4. `deleteBranchesByBranchGuidesBySlug` – requires path parameters `branch` and `slug`.

## Rules

- Authentication: include either a `Authorization: Basic <credentials>` header (basicAuth) or a `Authorization: Bearer <token>` header (bearerAuth).
