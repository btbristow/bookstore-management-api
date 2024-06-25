---
layout: single
title: DELETE orders
toc: true
toc_sticky: true
sidebar:
  nav: "docs"
---
Use `DELETE` with the `orders` endpoint to cancel orders or remove them from the order management system.

## Request

To `DELETE` an order enter `curl -X DELETE http://{server_url}:{port}/orders/{id}` with your server and port and a valid order `id`.

## Response

The following sections describe possible responses from the `orders` endpoint when using the `DELETE` method.

### Success response

A successful `DELETE` returns `200 OK` with the deleted order object.

### Error response

An error contains one of the following HTTP status codes.

| Status Code             | Description                                       |
|-------------------------|---------------------------------------------------|
| 404 Not Found           | The server could not find the requested resource. |
| 500 Service Unavailable | The server could not complete the request.        |
| ECONNREFUSED            | The service is unavailable.                      |

## Related Topics

* [Orders](orders.md)
* [POST orders](post-orders.md)
* [PATCH orders](patch-orders.md)
