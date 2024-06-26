---
layout: single
title: PATCH books
toc_sticky: true
sidebar:
  nav: "docs"
---
Use `PATCH` with the `books` endpoint to change book information, most commonly when updating the number of copies in stock.

**Note:** To add books that a store has not previously carried, use [POST books](post-books.md) instead.
{: .notice--info}

## Request

To update a book with `PATCH`, enter a request similar to the following, using a valid book `id` and your server and port:

```bash
curl -X PATCH \
     -H "Content-Type: application/json" \
     -d '{"in_stock": 7}' \
     http://{server_url}:{port}/books/{id}
```

## Response

The following sections describe possible responses from the `books` endpoint when using the `PATCH` method.

### Success response

A successful `PATCH` returns `200 OK` with the updated book object.

### Error responses

An error contains one of the following HTTP status codes.

| Status Code             | Description                                       |
|-------------------------|---------------------------------------------------|
| 404 Not Found           | The server could not find the requested resource. |
| 500 Service Unavailable | The server could not complete the request.        |
| ECONNREFUSED            | The service is unavailable.                      |

## Related Topics

* [Books](books.md)
* [POST books](post-books.md)
* [DELETE books](delete-books.md)
