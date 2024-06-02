---
layout: page
---
# POST orders

Use `POST` with the `orders` endpoint to create new orders. You can add one or more orders to the request body. You must [create customers](post-customers.md) before you can create orders. In addition,orders must contain at least one `book_id`.

## Request

To create an order with the `POST orders` method, use the following cURL request.

```bash
curl -X POST '{server_url}:{port}/orders' \
--header 'Content-Type: application/json' \
--data `{
    "order_date": "2024-02-22",
    "number_of_items": 1,
    "customer_id": 3,
    "book_id": [2]
  }'
```

## Response

The following sections contain an example success response, along with error response codes.

### Success response code

When your `POST` request is successful, the Bookstore Management API returns a `201 Created`, along with the following response body.

```json
{
    "order_date": "2023-06-15",
    "items": 2,
    "customer_id": 1,
    "order_id": [3, 5]
}
```

### Error response codes

When your `POST` request is unsuccessful, the Bookstore Management API returns one of the following response codes.

| Response Code | Description                                      |
|---------------|--------------------------------------------------|
| 400           | Bad Request  |
| 401           | Unauthorized  |
| 503           | Service Unavailable |

## Related Topics

- [Orders endpoint](orders.md)
- [PATCH orders](patch-orders.md)
