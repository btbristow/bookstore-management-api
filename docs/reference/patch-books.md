---
layout: page
---
# PATCH books

Use `PATCH` with the `books` endpoint to update book information. You will use this method most commonly to change the number of books in stock.

> **Note:**
> To add books that a store has not previously carried, use [POST books](post-books.md) instead.

## Request

To update a book with `PATCH`, use the following curl request. Supply your own `{server_url}` and `{port}`, along with a valid book `id`:

```bash
curl -X PATCH \
     -H "Content-Type: application/json" \
     -d '{"in_stock": 7}' \
     http://{server_url}:{port}/books/{id}
```

## Response

The following sections list the success and error responses that the `PATCH books` method supports.

### Success response

A successful `PATCH` returns `200 OK` along with the complete book object. This includes updated property values.

### Error responses

An error response contains one of the following HTTP status codes.

| Status Code             | Description                                       |
|-------------------------|---------------------------------------------------|
| 404 Not Found           | The server could not find the requested resource. |
| 500 Service Unavailable | The server could not complete the request.        |
| ECONNREFUSED            | The service is unavailable.                      |

## Related Topics

- [Books endpoint](books.md)
- [POST books](post-books.md)
