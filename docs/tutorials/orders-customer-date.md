---
layout: page
---
# Get orders by customer or date

This tutorial takes about 15 minutes to complete and explains how to use query parameters with the `orders` endpoint to get orders by customer or order date.

You can use query parameters with any endpoint in the Bookstore Management API.

## Prerequisites

To complete this tutorial, you must have command line access to curl and be able to send requests to the Bookstore Management API. You can integrate the API with your test environment or run it locally.

To learn how to run the API locally, see [Test with JSON Server](test-with-json-server.md).

## Step 1: Get orders by customer

To get orders by customer, obtain a customer's `id` from their email address and use it as a query parameter in a request to `/orders`.

1. Enter `curl -X GET '{server_url}:{port}/customer?email=mjameson@gmail.com'`, using your own `{server_url}` and `{port}`.

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

2. Enter `curl -X GET 'https://{server_url}:{port}/orders?customer_id=2ogb'`, using your own `{server_url}` and `{port}`.

    > Note: Use the customer `id` from your last request for the `customer_id` property.

    The API returns a `200 OK` and a response body with an array of orders:

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

To view orders placed on a certain date, enter `curl -X GET '{server_url}:{port}/orders?date=2024-02-22'`, using your own `{server_url}` and `{port}`.

The Bookstore Management API returns a `200 OK` and a response body with an array of orders in the following format:

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
* [Create an order](tutorials/create-an-order.md)
* [Update a store](update-store.md)
