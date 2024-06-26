---
layout: single
title: PATCH customers
toc: true
toc_sticky: true
sidebar:
  nav: "docs"
---
Use `PATCH` with the `customers` endpoint to update customer information, for example when upating a customer's email address.

## Request

To update customer information using `PATCH`, enter a curl request similar to the following, with your server and port:

```bash
curl -X PATCH \
     -H "Content-Type: application/json" \
     -d '"email": "brian.smith@gmail.com"' \
     http://{server_url}:{port}/customers/{id}
```

## Response

The following sections describe possible responses from the `customers` endpoint when using the `PATCH` method.

### Success response

A successful `PATCH` returns `200 OK` with the updated customer object.

### Error responses

An error contains one of the following HTTP status codes.

| Status Code             | Description                                       |
|-------------------------|---------------------------------------------------|
| 404 Not Found           | The server could not find the requested resource. |
| 500 Service Unavailable | The server could not complete the request.        |
| ECONNREFUSED            | The service is unavailable.                      |

## Related Topics

* [Customers](customers.md)
* [POST customers](post-customers.md)
* [DELETE customers](delete-customers.md)
