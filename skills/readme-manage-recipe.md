---
name: readme-manage-recipe
description: Create, retrieve, update, and delete a recipe using the ReadMe Recipes API.
api: openapi/readme-recipes-api-openapi.yml
operations:
- postRecipes
- getRecipesBySlug
- putRecipesBySlug
- deleteRecipesBySlug
generated: '2026-10-04'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/readme-recipes-api-openapi.yml ; every operationId checked against the contract
---

# readme-manage-recipe

Create, retrieve, update, and delete a recipe using the ReadMe Recipes API.

## Steps

1. 1. `postRecipes` – send a POST request to `/recipes` with the required request body fields for a new recipe.
2. 2. `getRecipesBySlug` – send a GET request to `/recipes/{slug}` using the `slug` returned from the creation step to retrieve the recipe details.
3. 3. `putRecipesBySlug` – send a PUT request to `/recipes/{slug}` with the `slug` of the recipe and the fields to update in the request body.
4. 4. `deleteRecipesBySlug` – send a DELETE request to `/recipes/{slug}` with the `slug` of the recipe to remove it.

## Rules

- Include an `Authorization` header using either `basicAuth` or `bearerAuth` as defined by the API.
- POST and PUT requests should be idempotent when the same payload is sent with the same `slug`.
- The `GET /recipes` endpoint supports pagination via standard `page` and `limit` query parameters (if used).
- On error, the API returns standard HTTP status codes; handle 4xx for client errors and 5xx for server errors.
