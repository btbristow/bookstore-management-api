---
layout: single
title: Update a store
toc: true
toc_sticky: true
sidebar:
  nav: "docs"
---
This tutorial takes about 15 minutes to complete and presents a workflow where you add books from a delivery, update customer information, and edit an order.

## Prerequisites

To complete this tutorial, you must have command line access to curl and be able to send requests to the Bookstore Management API. You can integrate the API with your test environment or run it locally.

To learn how to run the API locally, see [Test with JSON Server](test-with-json-server.md).

## Step 1: Update books in stock

To update the number of books in stock after a delivery, enter the following `PATCH` request. Supply your own `{server_url}` and `{port}`:

```bash
curl -X PATCH '{server_url}:{port}/books/988c' \
--header 'Content-Type: application/json' \
--data '{
    "in_stock": 5
  }'
```

The Bookstore Management API returns a `200 OK` with a response body that contains the updated book:

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

## Step 2: Change customer details

To update a customer phone number, enter the following `PATCH` request. Supply your own `{server_url}` and `{port}`:

```bash
curl -X PATCH '{server_url}:{port}/books/988c' \
--header 'Content-Type: application/json' \
--data '{
    "telephone": 7187486732
  }'
```

The Bookstore Management API returns a `200 OK` with a response body that contains the updated customer:

```json
{
   "id": "8azr",
   "last_name": "Jones",
   "first_name": "Jenny",
   "telephone": 7187486732,
   "email": "jjones@proton.me"
}
```

## Step 3: Edit an order

To update a the books in an order, enter the following `PATCH` request. Supply your own `{server_url}` and `{port}`:

**Note:** In the following request, be sure to change `order_date`, `subtotal`, `tax`, and `total` to correctly update your order management system.
{: .notice--info}

```bash
curl -X PATCH '{server_url}:{port}/books/9fmo' \
--header 'Content-Type: application/json' \
--data '{
      "order_date": "2024-04-25",
      "items": 2,
      "book_id": [
        "7dpc",
        "988c"
      ],
      "subtotal": "17.98",
      "tax": "1.60",
      "total": "19.58"
  }'
```

The Bookstore Management API returns a `200 OK` with a response body that contains the updated order:

```json
{
   "id":"9fmo",
   "order_date":"2024-02-22",
   "items":2,
   "customer_id":"2ogb",
   "book_id":[
      "7dpc",
      "988c"
   ],
   "subtotal":"17.98",
   "tax":"1.60",
   "total":"19.58"
}
```

## Related topics

* [Get store inventory](get-store-inventory.md)
* [Create an order](tutorials/create-an-order.md)
* [Get orders by customer or date](tutorials/orders-customer-date.md)
