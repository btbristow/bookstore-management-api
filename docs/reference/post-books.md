---
layout: page
---

# POST books

Use `POST` with the `books` endpoint to create new books in the store inventory. You can add multiple books in one request body.

> **Note**
> To update the number of copies of _existing_ books, use [PATCH books](patch-books.md) with the `in_stock` property instead.

## Request

To add a new book using curl, enter a `POST` request similar to the following, along with your own `{server_url}` and `{port}`:

```bash
curl -X POST '{server_url}:{port}/books' \
--header 'Content-Type: application/json' \
--data '{
    "title": "The Power Broker: Robert Moses and the Fall of New York",
    "author_last_name": "Caro",
    "author_first_name": "Robert A.",
    "publisher": "Knopf Doubleday Publishing Group",
    "year_published": 1974,
    "ISBN-10": 9780394480763,
    "genre": "non-fiction",
    "format": "paperback",
    "condition": "new",
    "price": "15.99",
    "in_stock": 1,
}'
```

## Response

The following sections list the success and error responses that the `POST books` method supports.

### Success response

A successful `POST` returns `201 Created` along with the complete book object, including a new `id` property (for example, `"id": "3f50"`).

### Error response

An error response contains one of the following HTTP status codes.

| Status Code             | Description                                       |
|-------------------------|---------------------------------------------------|
| 404 Not Found           | The server could not find the requested resource. |
| 500 Service Unavailable | The server could not complete the request.        |
| ECONNREFUSED            | The service is unavailable.                      |

## Related Topics

- [Books endpoint](books.md)
- [PATCH books](patch-books.md)
