---
layout: single
title: DELETE books
toc: true
toc_sticky: true
sidebar:
  nav: "docs"
---
Use `DELETE` with the `books` endpoint to remove books that a store will no longer carry.

**Note:** To set the number of copies in stock to zero, use [PATCH books](patch-books.md) instead.
{: .notice--info}

## Request

To `DELETE` a book enter `curl -X DELETE http://{server_url}:{port}/books/{id}` with your server and port and a valid book `id`.

## Response

The following sections describe possible responses from the `books` endpoint when using the `DELETE` method.

### Success response

A successful `DELETE` returns `200 OK` with the deleted book object.

### Error response

An error contains one of the following HTTP status codes.

| Status Code             | Description                                       |
|-------------------------|---------------------------------------------------|
| 404 Not Found           | The server could not find the requested resource. |
| 500 Service Unavailable | The server could not complete the request.        |
| ECONNREFUSED            | The service is unavailable.                      |

## Related Topics

* [Books](books.md)
* [POST books](post-books.md)
* [PATCH books](patch-books.md)
