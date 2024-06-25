---
layout: single
title: Create an order
toc: true
toc_sticky: true
sidebar:
  nav: "docs"
---
This tutorial takes about 20 minutes to complete and presents a standard order creation workflow. You start by listing the books in stock, add a new customer, and then create an order that references both the customer and the book purchased.

## Prerequisites

To complete this tutorial, you must have command line access to curl and be able to send requests to the Bookstore Management API. You can integrate the API with your test environment or run it locally.

To learn how to run the API locally, see [Test with JSON Server](test-with-json-server.md).

## Step 1: Get the book inventory

To add a book to an order, you must know its `id`. We will use `GET` with the `/books` endpoint to obtain a list of example books. Then, we will choose a book to use in this tutorial.

1. To list the books in stock, enter `curl -X GET {server_url}:{port}/books`, using your own `{server_url}` and `{port}`:

    > **Tip:**
    > For example, if using json-server, you might enter `curl -X GET localhost:3000/books`.

    The Bookstore Management API returns a `200 OK` along with a response body in the following format:

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

1. Choose any book `id` and note it for later use in this tutorial.

## Step 2: Create a customer

When you create an order, you must specify a customer. We will use `POST` with the `/customers` endpoint to add a new customer who has not yet visited the store.

1. To create a customer, enter the following curl request:

    ```bash
    curl -X POST '{server_url}:{port}/customers' \
    --header 'Content-Type: application/json' \
    --data '{
        "last_name": "Jameson",
        "first_name": "Michael",
        "telephone": 2018724543,
        "email": "mjameson@gmail.com",
        }'
    ```

    The Bookstore Management API returns a `201 Created`, along with a response body similar to the following:

    ```json
    {
      "id": "2ogb",
      "last_name": "Jameson",
      "first_name": "Michael",
      "telephone": 2018724543,
      "email": "mjameson@gmail.com"
    }
    ```

1. Note the `id` for use in the next step.

## Step 3: Create an order

Now that you know the book and the customer, use `POST` with the `/orders` endpoint to create a new order.

> **Tip:**  
> In the following example, `book_id` is an array. To add multiple books to an order, you might use `["9hne", "7dpc"]`, where each number is the `id` for one book.

* To create an order, enter the following curl request. Use the value of book `id` in `book_id` and the value of customer `id` in `customer_id`:

    ```bash
    curl -X POST '{server_url}:{port}/orders' \
    --header 'Content-Type: application/json' \
    --data `{
        "order_date": "2024-02-22",
        "number_of_items": 1,
        "customer_id": "3mys",
        "book_id": ["8ajv"]
        }'
    ```

    The Bookstore Management API returns a `201 Created`, along with a response body similar to the following:

    ```json
    {
      "id": "8kdt",
      "order_date": "2024-04-19",
      "items": 1,
      "customer_id": "3mys",
      "book_id": [
        "5rzn"
      ],
      "subtotal": "9.99",
      "tax": "0.89",
      "total": "10.88"
    }
    ```

## What to do next

Now that you know how to manage customers and orders, proceed with your integration or read other topics to learn more about the Bookstore Management API.

* [Update a store](update-store.md)
* [Get store inventory](get-store-inventory.md)
* [Get orders by customer or date](tutorials/orders-customer-date.md)
