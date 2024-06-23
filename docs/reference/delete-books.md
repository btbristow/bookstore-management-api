---
layout: page
---

# DELETE books

Use `DELETE` with the `books` endpoint to remove books from a store's inventory. This method is used when a store will no longer carry a book, rather than when a book is out of stock.

## Request

To `DELETE` a book using curl, enter `curl -X DELETE http://{server_url}:{port}/books/{id}` with your own `{server_url}` and `{port}` and a valid book `id`.

## Response

The following sections list the success and error responses that the `DELETE books` method supports.

### Success response

A successful `DELETE` returns `200 OK` along with the complete book object that was deleted.

### Error response

An error response contains one of the following HTTP status codes.

| Status Code             | Description                                       |
|-------------------------|---------------------------------------------------|
| 404 Not Found           | The server could not find the requested resource. |
| 500 Service Unavailable | The server could not complete the request.        |
| ECONNREFUSED            | The service is unavailable.                      |

## Related Topics

* [Books](reference/books.md)
* [POST books](reference/post-books.md)
* [PATCH books](reference/patch-books.md)
