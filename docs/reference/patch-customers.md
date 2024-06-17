---
layout: page
---
# PATCH customers

Use `PATCH` with the `customers` endpoint to update customer information. For example, you might use this method to update a customer email address.

## Request

To update customer information with `PATCH`, use the following curl request with your own `{server_url}` and `{port}`:

```bash
curl -X PATCH \
     -H "Content-Type: application/json" \
     -d '"email": "brian.smith@gmail.com"' \
     http://{server_url}:{port}/customers/{id}
```

## Response

The following sections list the success and error responses that the `PATCH customers` method supports.

### Success response

A successful `PATCH` returns `200 OK` along with the complete customer object. This includes updated properties.

### Error responses

An error response contains one of the following HTTP status codes.

| Status Code             | Description                                       |
|-------------------------|---------------------------------------------------|
| 404 Not Found           | The server could not find the requested resource. |
| 500 Service Unavailable | The server could not complete the request.        |
| ECONNREFUSED            | The service is unavailable.                      |

## Related Topics

* [Customers endpoint](customers.md)
* [POST customers](post-customers.md)
* [DELETE customers](delete-customers.md)
