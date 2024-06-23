---
layout: page
---

# DELETE customers

Use `DELETE` with the `customers` endpoint to remove customers from a store database. When you delete customers, you must also [delete their orders](delete-orders.md).

## Request

To `DELETE` a customer object using curl, enter `curl -X DELETE http://{server_url}:{port}/customer/{id}` with your own `{server_url}` and `{port}` and a valid customer `id`.

## Response

The following sections list the success and error responses that the `DELETE customers` method supports.

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

* [Customers endpoint](customers.md)
* [POST customers](post-customers.md)
* [PATCH customers](patch-customers.md)
