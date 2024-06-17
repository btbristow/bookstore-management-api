---
layout: page
---

# DELETE orders

Use `DELETE` with the `orders` endpoint to remove orders from a store's order management system (for example, to cancel an order).

## Request

To `DELETE` an order using curl, enter `curl -X DELETE http://{server_url}:{port}/orders/{id}` with your own `{server_url}` and `{port}` and a valid order `id`.

## Response

The following sections list the success and error responses that the `DELETE orders` method supports.

### Success response

A successful `DELETE` returns `200 OK` along with the complete order object that was deleted.

### Error response

An error response contains one of the following HTTP status codes.

| Status Code             | Description                                       |
|-------------------------|---------------------------------------------------|
| 404 Not Found           | The server could not find the requested resource. |
| 500 Service Unavailable | The server could not complete the request.        |
| ECONNREFUSED            | The service is unavailable.                      |

## Related Topics

* [Orders](reference/orders.md)
* [GET orders by customer](reference/get-orders.md)
* [POST orders](reference/post-orders.md)
* [PATCH orders](reference/patch-orders.md)
