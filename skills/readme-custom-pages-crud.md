---
name: readme-custom-pages-crud
description: Create, retrieve, update, and delete a custom page for a branch.
api: openapi/readme-custom-pages-api-openapi.yml
operations:
- postBranchesByBranchCustomPages
- getBranchesByBranchCustomPagesBySlug
- putBranchesByBranchCustomPagesBySlug
- deleteBranchesByBranchCustomPagesBySlug
generated: '2026-10-04'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/readme-custom-pages-api-openapi.yml ; every operationId checked against the contract
---

# readme-custom-pages-crud

Create, retrieve, update, and delete a custom page for a branch.

## Steps

1. 1. Use `postBranchesByBranchCustomPages` to create a custom page. Provide the required request body fields as defined in the API contract.
2. 2. Use `getBranchesByBranchCustomPagesBySlug` to retrieve the newly created custom page by its slug.
3. 3. Use `putBranchesByBranchCustomPagesBySlug` to update the custom page. Include the fields to be updated in the request body.
4. 4. Use `deleteBranchesByBranchCustomPagesBySlug` to delete the custom page.

## Rules

- Authentication: Include either a Basic Auth header or a Bearer token in the `Authorization` header.
- Idempotency: The `PUT` operation (`putBranchesByBranchCustomPagesBySlug`) should be idempotent when the same payload is sent.
