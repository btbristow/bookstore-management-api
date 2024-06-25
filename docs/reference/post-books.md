---
layout: single
title: POST books
toc: true
toc_sticky: true
sidebar:
  nav: "docs"
---
Use `POST` with the `books` endpoint to create new books in a store inventory. When testing with JSON Server, you must add one book at a time.

**Note:** To update the number of book copies in stock, use [PATCH books](patch-books.md) instead.
{: .notice--info}

## Request

To add a new book, enter a request similar to the following, with your server and port:

```bash
curl -X POST '{server_url}:{port}/books' \
--header 'Content-Type: application/json' \
--data '{
    "title": "The Power Broker",
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

TThe following sections describe possible responses from the `books` endpoint when using the `POST` method.

### Success response

A successful `POST` returns `201 Created` with the book object, including a new `id` property (for example, `"id": "3f50"`).

### Error response

An error contains one of the following HTTP status codes.

| Status Code             | Description                                       |
|-------------------------|---------------------------------------------------|
| 404 Not Found           | The server could not find the requested resource. |
| 500 Service Unavailable | The server could not complete the request.        |
| ECONNREFUSED            | The service is unavailable.                      |

## Related Topics

* [Books](books.md)
* [PATCH books](patch-books.md)
* [DELETE books](delete-books.md)
