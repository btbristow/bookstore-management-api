# Work with Customers and Orders

This tutorial presents a complete customer and order management workflow for the Bookstore Management API. It guides you through obtaining a list of books in stock, creating a customer, and creating an order that references the customer and the books purchased.

Expect this tutorial to take about 20 minutes to complete.

## Prerequisites

To complete the tasks in this tutorial, you must have command line access to cURL and access to the Bookstore Management API endpoints, either integrated with your test environment or running on your local machine via [json-server](https://www.npmjs.com/package/json-server).

To use the mock endpoint method, install json-server and download the [API folder](https://github.com/btbristow/bookstore-management-api/tree/4227e30164eb37172b024df7f1dd5400c6e454b2/api) from our repository. On the command line, run the appropriate script for your system: `start-server.bat` on Windows or `start-server.sh` on Mac or Linux.

For example, on Mac, run `./json-server.sh`. 

> [!NOTE]  
> When running json-server on your local machine, port 3000 must be available.

## Get your book inventory

Before you can add a book to an order, you must know the `book_id`, so start with a `GET` request to the `/books` endpoint to list the books in stock.

#### To list the books in stock:

On the command line, enter `curl -X GET {server_url}:{port}/books`.

The Bookstore Management API returns a `200 OK` along with a JSON response body in the following format. For property definitions, see [Books endpoint](../reference/books.md#response-example).

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
    "book_id": 5, # Note for use in the order
}
```

## Create a customer

When creating an order, you must specify a customer. We will use the `POST` method with `/customers` to create a new customer who has not visited the store.

#### To create a customer:

On the command line, enter the following cURL request:

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

The Bookstore Management API returns a `201 Created`, along with the following response body:

```json
{
    "status": "PASS",
    "message": "Customer created",
    "customer_id": 4 # Note for use in the order
}
```

## Create an order

Now that you know the book to purchase and the customer who will purchase it, create an order using `POST orders`.

On the command line, enter the following cURL:

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

The Bookstore Management API returns a `201 Created`, along with the following response body:

```json
{
    "status": "PASS",
    "message": "Order created",
    "order_id": 3
}
```


> [!TIP]  
> To add multiple books to an order, pass them in an array. For example, use `[2, 5]`.

## What to do next

Now that you have used the Bookstore Management API to create books, customers, and orders, you can proceed with your integration or learn more about the service. The following topics provide next steps.

* [Update your store inventory](update-store-inventory.md)
* [Work with customers](work-with-customers.md)