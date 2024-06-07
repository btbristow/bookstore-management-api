---
layout: page
---
# POST customers

Use `POST` with the `customers` endpoint to create new customers for a store. You can add one or more customers to the request body. You must create customers to create orders.

## Request

To create a customer with the `POST customers` method, use the following cURL request.

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

The following sections contain an example success response, along with error response codes.

### Success response

When your `POST` request is successful, the Bookstore Management API returns a `201 Created`, along with the following response body.

```json
{
    "status": "PASS",
    "message": "Customer created",
    "customer_id": 2
}
```

### Error responses

When your `POST` request is unsuccessful, the Bookstore Management API returns one of the following response codes.

| Response Code | Description                                      |
|---------------|--------------------------------------------------|
| 400           | Bad Request  |
| 401           | Unauthorized  |
| 503           | Service Unavailable |

## Related Topics

- [Customers endpoint](customers.md)
- [PATCH customers](patch-customers.md)
