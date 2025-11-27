# Authentication

The BookHive API uses API key authentication. Every request must include your API key inside the Authorization header.

## Header Format

Authorization: Bearer YOUR_API_KEY

Example:

curl -H "Authorization: Bearer abc123xyz" \
https://api.bookhive.com/v1/books

## Notes

- Keep your API key secure.
- Do not expose it publicly.
- Keys can be regenerated from the developer dashboard.
- Rate limits may apply based on your plan.
