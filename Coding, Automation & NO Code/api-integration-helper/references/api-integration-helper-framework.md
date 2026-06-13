# API Integration Framework

## Auth patterns

### API key header
`Authorization: Bearer YOUR_API_KEY`

### Basic auth
Username and password or key as username depending on API.

### OAuth2
Usually requires client ID, client secret, authorization URL, token URL, scopes, refresh token handling.

### Webhook signature
Validate payload signature before trusting the request.

## Request checklist

- base URL
- endpoint path
- method
- headers
- query parameters
- body payload
- auth
- required scopes
- pagination
- rate limits
- idempotency key
- retries
- timeout

## Code safety

Never hardcode secrets. Use environment variables. Log response status and request IDs, not secret headers.

## Error handling

Handle 400, 401, 403, 404, 409, 422, 429, and 5xx differently. Retry 429 and 5xx with backoff when safe.

## Data sync patterns

- one-way push
- one-way pull
- bidirectional sync
- webhook-triggered sync
- scheduled batch sync
- incremental sync using updated_at
- idempotent upsert using external IDs
