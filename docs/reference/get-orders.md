---
layout: page
---

# GET orders by customer

You can make a `GET` reqest to the `/orders` endpoint and use query parameters to list all orders made by a customer.

## Request

To `GET` orders by customer using curl, enter `curl -X GET http://{server_url}:{port}/orders?customer_id={customer_id}` with your own `{server_url}` and `{port}` and a valid order `id`.

## Response

The following sections list the success and error responses that this method supports. 

### Success response

A successful `GET` request for orders by customer returns a `200 OK` along with all orders for that customer in the response body.

> **Note:**
> If you send incorrect query parameters (such as the wrong property), you receive a `200 OK` with an empty array `[]`. When this happens, confirm the properties and syntax in your request.

### Error response

An error response contains one of the following HTTP status codes.

| Status Code             | Description                                       |
|-------------------------|---------------------------------------------------|
| 404 Not Found           | The server could not find the requested resource. |
| ECONNREFUSED            | The service is unavailable.                      |

## Related Topics

* [orders endpoint](orders.md)
* [POST orders](post-orders.md)
* [PATCH orders](patch-orders.md)
* [DELETE orders](delete-orders.md)
