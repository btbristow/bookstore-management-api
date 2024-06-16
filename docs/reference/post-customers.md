---
layout: page
---
# POST customers

Use `POST` with the `customers` endpoint to create new customers for a store. You can add multiple customers to a request body. You must create customers before you create orders.

## Request

To `POST` a new customer using curl, enter the following request with your own `{server_url}` and `{port}` values:

```bash
curl -X POST '{server_url}:{port}/customers' \
--header 'Content-Type: application/json' \
--data '{
    "last_name": "Johnson",
    "first_name": "Emily",
    "telephone": 5551234567,
    "email": "emily.johnson@example.com"
}'
```

## Response

The following sections list the success and error responses that the `POST customers` method supports.

### Success response

A successful `POST` returns `201 Created` along with the complete customer object, including a new `id` property (for example, `"id": "4g540"`).

### Error response

An error response contains one of the following HTTP response status codes.

| Status Code             | Description                                       |
|-------------------------|---------------------------------------------------|
| 404 Not Found           | The server could not find the requested resource. |
| 500 Service Unavailable | The server could not complete the request.        |
| ECONNREFUSED            | The service is unavailable.                      |

## Related Topics

- [Customers endpoint](customers.md)
- [PATCH customers](patch-customers.md)
