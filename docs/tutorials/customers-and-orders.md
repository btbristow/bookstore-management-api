---
layout: page
---
# Manage Customers and Orders

This tutorial presents a complete customer and order management workflow for the Bookstore Management API. It guides you through obtaining a list of books in stock, creating a customer, and then creating an order that references both the customer you created and the books they purchased.

This tutorial takes about 20 minutes to complete.

## Prerequisites

To complete these steps, you must have command line access to cURL and access to the Bookstore Management API endpoints, either integrated with your test environment or running locally as a mock server.

For more information, see [Test the Bookstore Management API](tutorials/test-bookstore-api.md).

## Step 1: Get your book inventory

Before you can add a book to an order, you must know the `book_id` of the book being purchased. We will use the `GET` method with `/books` to obtain a list of books.

To list the books in stock, on the command line, enter `curl -X GET {server_url}:{port}/books`.

The Bookstore Management API returns a `200 OK` along with a response body in the following format:

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

Note the `book_id` for use in the order you will create.

## Step 2: Create a customer

When creating an order, you must also specify a customer. We will use the `POST` method with `/customers` to create a new customer who has not yet visited the store.

To create a customer, on the command line, enter the following cURL request:

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

The Bookstore Management API returns a `201 Created`, along with a response body like the following:

```json
{
    "status": "PASS",
    "message": "Customer created",
    "customer_id": 4
}
```

Note the `customer_id` for use in the order.

## Step 3: Create an order

Now that you know the book to purchase and the customer who will purchase it, you can create a new order by using the `POST` method with `/orders`.

> **Note:**  
> In the sample, note that `book_id` is an array which supports multiple values. For example, to add multiple books, you might use: `[2, 5]`.

To create a new order, on the command line, enter the following cURL request:

```bash
curl -X POST '{server_url}:{port}/orders' \
--header 'Content-Type: application/json' \
--data `{
    "order_date": "2024-02-22",
    "number_of_items": 1,
    "customer_id": 3,
    "book_id": [2]
    }'
```

The Bookstore Management API returns a `201 Created`, along with a response body like the following:

```json
{
    "status": "PASS",
    "message": "Order created",
    "order_id": 3
}
```

## What to do next

Now that you have completed this tutorial, either proceed with your integration or read other topics to learn more about the Bookstore Management API.

* [Update your store inventory](update-store-inventory.md)
* [Work with customers](work-with-customers.md)