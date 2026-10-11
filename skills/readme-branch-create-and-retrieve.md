---
name: readme-branch-create-and-retrieve
description: Create a new branch and then retrieve its details.
api: openapi/readme-branches-api-openapi.yml
operations:
- postBranches
- getBranchesByBranch
generated: '2026-10-04'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/readme-branches-api-openapi.yml ; every operationId checked against the contract
---

# readme-branch-create-and-retrieve

Create a new branch and then retrieve its details.

## Steps

1. 1. Use `postBranches` with the request body fields required to create a branch.
2. 2. Use `getBranchesByBranch` with the `branch` path parameter to fetch the newly created branch.

## Rules

- Authentication: Provide either a Basic Auth header or a Bearer token in the Authorization header.
- Rate limiting: No rate limit is defined; no special handling on exhaustion.
