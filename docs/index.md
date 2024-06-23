---
layout: page
---
# Bookstore Management API

The Bookstore Management API is the back end for your custom bookstore application. Connect your interface to a REST API that sends and receives pure JSON and is designed for the workflows that booksellers need. Customize your integration for any store: new or used, specialty or general, online or off.

The Bookstore Management API supports the following features in your application:

* Comprehensive inventory management based on the ISBN-10 standard.
* Customer and order management operations for SQL databases.
* Integration with your point-of-sale systems.

## Get Started

This documentation site contains everything you need to test and implement the Bookstore Management API. To get started, see the following topics:

* [Test with JSON Server](tutorials/test-with-json-server.md) — Install JSON Server to test the API locally.
* [Get store inventory](tutorials/get-store-inventory.md) — Using curl, list an example store inventory.

## Tutorials

The following tutorials outline common bookseller use cases. Use them to design a user-centric application for any bookstore.

* [Create an order](tutorials/create-an-order.md) — Add a customer and create a new order.
* [Update a store](tutorials/update-store.md) — Update common store items, including the books in stock, customer contact information, and order details. *Coming soon*
* [Build custom order queries](tutorials/custom-order-queries.md) — Use query parameters to view orders by customer email, or phone number.  *Coming soon*

## Reference

The Bookstore Management API has three endpoints. The following topics contain a complete reverence, including sample requests and responses.

### Books endpoint

The **[Books endpoint](reference/books.md)** connects your inventory database to your application's interface. It supports the following methods:

* [POST books](reference/post-books.md)
* [PATCH books](reference/patch-books.md)

### Customers endpoint

The **[Customers endpoint](reference/customers.md)** is designed to send customer details to your customer database. It supports the following methods:

* [POST customers](reference/post-customers.md)
* [PATCH customers](reference/patch-customers.md)
* [DELETE customers](delete-customers.md)

### Orders endpoint

The **[Orders endpoint](reference/orders.md)** supports your order managment and point-of-sale systems. It supports the following methods:

* [GET orders by customer](reference/get-orders.md)
* [POST orders](reference/post-orders.md)
* [PATCH orders](reference/patch-orders.md)
* [DELETE orders](reference/delete-orders.md)
