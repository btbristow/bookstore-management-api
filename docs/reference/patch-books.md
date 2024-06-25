---
layout: single
title: PATCH books
toc_sticky: true
sidebar:
  nav: "docs"
---
Use `PATCH` with the `books` endpoint to change book information. You will use this method most commonly to update the number of books in stock.

**Note:** To add books that a store has not previously carried, use [POST books](post-books.md) instead.
{: .notice--info}

## Request

To update a book with `PATCH`, use a curl request similar to the following. Supply your server and port, and a valid book `id`:

```bash
curl -X PATCH \
     -H "Content-Type: application/json" \
     -d '{"in_stock": 7}' \
     http://{server_url}:{port}/books/{id}
```

## Response

The following sections list the success and error responses that the `PATCH books` method supports.

### Success response

A successful `PATCH` returns `200 OK` along with the updated book object.

### Error responses

An error response contains one of the following HTTP status codes.

| Status Code             | Description                                       |
|-------------------------|---------------------------------------------------|
| 404 Not Found           | The server could not find the requested resource. |
| 500 Service Unavailable | The server could not complete the request.        |
| ECONNREFUSED            | The service is unavailable.                      |

## Related Topics

* [Books](books.md)
* [POST books](post-books.md)
* [DELETE books](reference/delete-books.md)
