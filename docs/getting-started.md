# Getting started with the Acme Work OS API

> Synthetic demo content. Acme Work OS is a fictional product.

The Acme Work OS API lets you read and update boards, items and columns programmatically. All requests are made over HTTPS to `https://api.acme-work-os.example/v1` and return JSON.

## Authentication

Every request must include a bearer token in the `Authorization` header. Tokens are created from the workspace admin panel and are scoped to a single workspace. Example: `Authorization: Bearer <YOUR_TOKEN>`.

## Rate limits

Each workspace may issue up to 600 requests per minute. When the limit is exceeded the API responds with HTTP 429 and a `Retry-After` header indicating how many seconds to wait.

## Pagination

List endpoints return up to 50 records per page. Use the `cursor` value from the response to request the next page.
