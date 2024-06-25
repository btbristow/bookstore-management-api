---
layout: single
title: PATCH orders
toc: true
toc_sticky: true
sidebar:
  nav: "docs"
---
Use `PATCH` with the `orders` endpoint to update order information. For example, build a feature to update the books purchased in an order.

## Request

To update an order with `PATCH`, use a curl request similar to the following, which adds an additional book. Supply your server and port and a valid order `id`:

```bash
curl -X PATCH '{server_url}:{port}/orders/{id}' \
--header 'Content-Type: application/json' \
--data `{
    "order_date": "2024-06-16",
    "number_of_items": 2,
    "book_id": ["03d7", "f2e5"],
    "subtotal": "22.98",
    "tax": "2.04",
    "total": "25.02"
  }'
```

## Response

The following sections list the success and error responses that the `PATCH orders` method supports.

### Success response

A successful `PATCH` returns `200 OK` along with the complete book object. This includes updated properties.

### Error responses

An error response contains one of the following HTTP response status codes.

| Status Code             | Description                                       |
|-------------------------|---------------------------------------------------|
| 404 Not Found           | The server could not find the requested resource. |
| 500 Service Unavailable | The server could not complete the request.        |
| ECONNREFUSED            | The service is unavailable.                      |

## Related Topics

* [Orders](reference/orders.md)
* [POST orders](reference/post-orders.md)
* [DELETE orders](reference/delete-orders.md)
