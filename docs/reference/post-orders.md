---
layout: single
title: POST orders
toc: true
toc_sticky: true
sidebar:
  nav: "docs"
---
Use `POST` with the `orders` endpoint to create new orders. When testing with JSON Server, you must add one customer at a time.

Orders must contain at least one `book_id` and `customer_id`, as described in [Create an order](../tutorials/create-an-order.md)

## Request

To add a new order, enter a `POST` request similar to the following with your server and port. Supply valid `book_id` properties and a valid `customer_id`.

```bash
curl -X POST '{server_url}:{port}/orders' \
--header 'Content-Type: application/json' \
--data `{
    "order_date": "2024-02-22",
    "number_of_items": 1,
    "customer_id": "2ogb",
    "book_id": ["7dpc"],
    "subtotal": "7.99",
    "tax": "0.71",
    "total": "8.70"
  }'
```

## Response

The following sections describe possible responses from the `orders` endpoint when using the `POST` method.

### Success response code

A successful `POST` returns `201 Created` with the order object, including a new `id` property (for example, `"id": "3f50"`).

### Error response

An error contains one of the following HTTP response status codes.

| Status Code             | Description                                       |
|-------------------------|---------------------------------------------------|
| 404 Not Found           | The server could not find the requested resource. |
| 500 Service Unavailable | The server could not complete the request.        |
| ECONNREFUSED            | The service is unavailable.                      |

## Related Topics

* [Orders](orders.md)
* [PATCH orders](patch-orders.md)
* [DELETE orders](delete-orders.md)
