---
layout: page
---
# Get store inventory

This tutorial takes about ten minutes to complete and explains how to `GET` a store inventory from the `/books` endpoint. It also contains an example response and provides next steps for troubleshooting errors.

## Prerequisites

To complete this tutorial, you need command line access to curl and must be able to send requests to the Bookstore Management API. You can integrate the API with your test environment or run it locally.

To learn how to run the API locally, see [Test with JSON Server](test-with-json-server.md).

## Send the request

You can get a store's inventory with one API request.

* To get a store's inventory, on the command line, type `curl -X GET {server_url}:{port}/books`.

    > **Tip:**
    > For example, if using json-server, you might type `curl -X GET localhost:3000/books`.

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
        "id": 5,
    }
    ```

## Troubleshoot errors

You may encounter the following errors:

* **404 Not Found** — Unable to find the requested resources. Check your API request for typos.
* **ECONNREFUSED** — Service offline. To resolve this issue, restart JSON Server.

## Related topics

* [Books endpoint](../reference/books.md)
* [POST books](../reference/post-books.md)
* [Create an order](create-an-order.md)
