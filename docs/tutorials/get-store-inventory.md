---
layout: page
---
# Get store inventory

This tutorial takes about ten minutes to complete and explains how to `GET` a store's inventory from the `/books` endpoint. It also contains an example response and provides next steps for troubleshooting errors.

## Prerequisites

To complete this tutorial, you need command line access to curl and must be able to send requests to the Bookstore Management API. You can integrate the API with your test environment or run it locally.

To learn how to run the API locally, see [Test with JSON Server](test-with-json-server.md).

## Send the request

You can get a store's inventory with a single API request.

* To get a store's inventory, enter `curl -X GET {server_url}:{port}/books`.

    > **Tip:**
    > For example, if using json-server, you might enter `curl -X GET localhost:3000/books`.

    The Bookstore Management API returns a `200 OK` along with a JSON response body in the following format.

    ```json
    {
      "id": "5rzn",
      "title": "Mastering the Art of French Cooking, Vol. 1",
      "author_last_name": "Child",
      "author_first_name": "Julia",
      "publisher": "Knopf Doubleday Publishing Group",
      "year_published": 2011,
      "ISBN-10": 9780307958174,
      "genre": "cookbooks",
      "format": "hardcover",
      "condition": "used",
      "price": "9.99",
      "in_stock": 2
    }
    ```

> **Note:** Out of stock books appear in this request with `"in_stock": 0`. To delete books that a store has ceased to carry, see [DELETE books](delete-books.md).

## Troubleshoot errors

The following table lists errors you may encounter, along with suggested resolutions.

| Status code             | Fix by...                                       |
|-------------------------|---------------------------------------------------|
| 404 Not Found           | Check your API request for typos. |
| ECONNREFUSED            | Restart JSON Server.                      |

## Related topics

* [Create an order](tutorials/create-an-order.md)
* [Update a store](tutorials/update-store.md)
* [Get orders by customer or date](tutorials/orders-customer-date.md)
