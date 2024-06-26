---
layout: single
title: Get orders by customer or date
toc: true
toc_sticky: true
sidebar:
  nav: "docs"
---
This tutorial takes about 10 minutes to complete and explains how to use query parameters with the `orders` endpoint to get orders from a single customer or order date.

You can use query parameters with any endpoint in the Bookstore Management API.

## Prerequisites

To complete this tutorial, you must have command line access to curl and be able to send requests to the Bookstore Management API. You can integrate the API with your test environment or run it locally.

To learn how to run the API locally, see [Test with JSON Server](test-with-json-server.md).

## Step 1: Get orders by customer

To get orders by customer, first obtain the customer's `id` from their email address.

1. Enter `curl -X GET '{server_url}:{port}/customer?email={email}'` with your server and port.

    **Tip:** If testing with JSON Server, `mjameson@gmail.com` is a valid email in the database file.
    {: .notice--success}

    The Bookstore Management API returns a `200 OK` with the following response body:

    ```json
    {
      "id": "2ogb",
      "last_name": "Jameson",
      "first_name": "Michael",
      "telephone": 2018724543,
      "email": "mjameson@gmail.com"
    }
    ```

2. Enter `curl -X GET 'https://{server_url}:{port}/orders?customer_id=2ogb'` with a valid `id` such as `2ogb` and your server and port:

    The API returns a `200 OK` and a response body in the following format:

    ```json
    [
      {
        "id": "9fmo",
        "order_date": "2024-02-22",
        "items": 1,
        "customer_id": "2ogb",
        "book_id": [
          "7dpc"
        ],
        "subtotal": "7.99",
        "tax": "0.71",
        "total": "8.70"
      },
      {
        "id": "8pij",
        "order_date": "2023-12-20",
        "items": 2,
        "customer_id": "2ogb",
        "book_id": [
          "7dpc",
          "9rdk"
        ],
        "subtotal": "22.98",
        "tax": "2.04",
        "total": "25.02"
      }
    ]
    ```

## Step 2: View orders by date

To view orders placed on a certain date, enter `curl -X GET '{server_url}:{port}/orders?date={date}'` with your server and port.

**Tip:** If testing with JSON Server, `2024-02-22` is a valid order date in the database file.
{: .notice--success}

The Bookstore Management API returns a `200 OK` and a response body in the following format:

```json
[
  {
    "id": "9fmo",
    "order_date": "2024-02-22",
    "items": 1,
    "customer_id": "2ogb",
    "book_id": [
      "7dpc"
    ],
    "subtotal": "7.99",
    "tax": "0.71",
    "total": "8.70"
  }
]
```

## Related Topics

* [Get store inventory](get-store-inventory.md)
* [Create an order](create-an-order.md)
* [Update a store](update-store.md)
