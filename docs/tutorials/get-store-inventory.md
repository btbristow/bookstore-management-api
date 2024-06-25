---
layout: single
title: Get a store inventory
toc: true
toc_sticky: true
sidebar:
  nav: "docs"
---
This tutorial takes about ten minutes to complete and explains how to `GET` a store inventory from the `/books` endpoint.

## Prerequisites

To complete this tutorial, you need command line access to curl and must be able to send requests to the Bookstore Management API. You can integrate the API with your test environment or run it locally.

To learn how to run the API locally, see [Test with JSON Server](test-with-json-server.md).

## Send your first request

You can get a store's inventory with a single request.

* To get a store's inventory, enter `curl -X GET {server_url}:{port}/books` with your server and port.

    The Bookstore Management API returns a `200 OK` and a response body in the following format:

    ```json
    {
      "id": "988c",
      "title": "Oryx and Crake",
      "author_last_name": "Atwood",
      "author_first_name": "Margaret",
      "publisher": "Knopf Canada",
      "year_published": 2010,
      "ISBN-10": 9780307400840,
      "genre": "fiction",
      "format": "hardcover",
      "condition": "new",
      "price": "19.99",
      "in_stock": 5
    }
    ```

## Troubleshoot errors

The Bookstore Management API uses standard HTTP response codes. The following table contains supported error codes and troubleshooting suggestions.

| Status code             | Fix by...                                       |
|-------------------------|---------------------------------------------------|
| 400 Bad request         | Checking your request for typos, such as invalid parameters. |
| 404 Not Found           | Confirming that you used the correct endpoint.|
| ECONNREFUSED            | Restarting JSON Server.                      |

## Related topics

* [Create an order](create-an-order.md)
* [Update a store](update-store.md)
* [Get orders by customer or date](orders-customer-date.md)
