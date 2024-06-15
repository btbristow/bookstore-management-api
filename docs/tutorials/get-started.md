---
layout: page
---
# Get Started with the Boookstore Management API

This tutorial introduces the Bookstore Management API with instructions to make a `GET` request to the `/books` endpoint. It also contains an example response and next steps for troubleshooting errors. 

This tutorial takes about ten minutes to complete.

## Prerequisites

To complete these steps, you must have command line access to cURL and access to the `/books` endpoint, either integrated with your test environment or running locally as a mock server.

For more information, see [Test the Bookstore Management API](/docs/tutorials/test-bookstore-api.md).

## Send the request

You will use the `GET` method with the `/books` endpoint to obtain a list of the books in the store. 

To list the books in the store, on the command line, enter `curl -X GET {server_url}:{port}/books`.

The Bookstore Management API returns a `200 OK` along with a JSON response body in the following format.

```json
{
    "title": "Mastering the Art of French Cooking, Vol. 1",
    "author_last_name": "Child",
    "author_first_name": "Julia",
    "publisher": "Knopf Doubleday Publishing Group",
    "year_published": 2011,
    "ISBN-10": 9780307958174,
    "genre": "cookbooks",
    "format": "hardcover",
    "in_stock": 1,
    "book_id": 5,
}
```

## Troubleshoot errors

You may encounter the following errors when using this tutorial:

* **401 Unauthorized** — Invalid authentication credentials. To troubleshoot, see [Authentication](/docs/reference/authentication.md).
* **404 Not Found** — Unable to find the requested resources. Check your API request for typos.

## Related topics

- [Books endpoint](reference/books.md)
- [POST books](reference/post-books.md)
- [Work with customers and orders](tutorials/customers-and-orders.md)