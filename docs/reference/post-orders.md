---
layout: page
---
# POST orders

Use `POST` with the `orders` endpoint to create new orders. You can add multiple orders to a request body. Orders must contain at least one `book_id` and `customer_id`, as described in [Create an order](../tutorials/create-an-order.md)

## Request

To `POST` an order, use a curl request similar to the following. Supply your own `{server_url}` and `{port}`, as well one or more `book_id` properties and a `customer_id` property:

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

The following sections list the success and error responses that the `POST orders` method supports.

### Success response code

A successful `POST` returns `201 Created` along with the complete book object, including a new `id` property (for example, `"id": "3f50"`).

### Error response

An error response contains one of the following HTTP response status codes.

| Status Code             | Description                                       |
|-------------------------|---------------------------------------------------|
| 404 Not Found           | The server could not find the requested resource. |
| 500 Service Unavailable | The server could not complete the request.        |
| ECONNREFUSED            | The service is unavailable.                      |

## Related Topics

* [Orders](reference/orders.md)
* [GET orders by customer](reference/get-orders.md)
* [PATCH orders](reference/patch-orders.md)
* [DELETE orders](reference/delete-orders.md)
