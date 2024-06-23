---
layout: page
---
# Bookstore Management API

The Bookstore Management API connects to your custom bookstore application's back end and is designed for bookseller workflows. Use it to customize your application for any store: new or used, specialty or general, online or off.

The Bookstore Management API has the following features:

* Comprehensive book inventory management based on the ISBN-10 standard.
* CRUD operation support for your inventory and order databases.
* Integration with your point-of-sale systems.

## Get Started

This documentation contains everything you need to test and implement the Bookstore Management API. To get started, see the following topics:

* [Test with JSON Server](tutorials/test-with-json-server.md) — Install JSON Server to test the API locally.
* [Get store inventory](tutorials/get-store-inventory.md) — Using curl, list an example store inventory.

## Tutorials

The following tutorials outline common bookseller use cases. Refer to them when designing a user-centric application for any store:

* [Create an order](tutorials/create-an-order.md) — Get a book title, add a customer, and create a new order.
* [Update a store](tutorials/update-store.md) — Update the books in stock, customer contact information, and order details.
* [Get orders by customer or date](tutorials/orders-customer-date.md) — With query parameters, get orders by customer or order date.

## Reference

The Bookstore Management API has three endpoints. The following topics contain reference information:

### Books endpoint

The **[Books endpoint](reference/books.md)** connects your user interface to your inventory database. It supports the following methods:

* [POST books](reference/post-books.md)
* [PATCH books](reference/patch-books.md)
* [DELETE books](reference/delete-books.md)

### Customers endpoint

The **[Customers endpoint](reference/customers.md)** sends customer details to your customer database and supports the following methods:

* [POST customers](reference/post-customers.md)
* [PATCH customers](reference/patch-customers.md)
* [DELETE customers](delete-customers.md)

### Orders endpoint

The **[Orders endpoint](reference/orders.md)** supports your order management and point-of-sale systems through the following methods:

* [GET orders by customer](reference/get-orders.md)
* [POST orders](reference/post-orders.md)
* [PATCH orders](reference/patch-orders.md)
* [DELETE orders](reference/delete-orders.md)
