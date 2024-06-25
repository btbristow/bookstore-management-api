---
layout: single
title: Bookstore Management API
toc: true
toc_sticky: true
sidebar:
  nav: "docs"
---
The Bookstore Management API brings bookseller workflows to your bookstore app. Use it to build custom apps for any store: new or used, general or specialty, online or off.

This documentation contains everything you need to test and implement the Bookstore Management API.

**The Bookstore Management API supports:**

* Comprehensive book inventory management.
* CRUD operations on your inventory, customer, and order databases.
* Integration with point-of-sale systems.

## Get Started

Start by using a mock API service to send your first request.

* [Test with JSON Server](tutorials/test-with-json-server.md) — Test locally with no integration.
* [Get store inventory](tutorials/get-store-inventory.md) — Get an example list of books in stock.

## Tutorials

Review common workflows before building them into your app.

* [Create an order](tutorials/create-an-order.md) — Get a book and create a customer; use them in a new order.
* [Update a store](tutorials/update-store.md) — Update the books in stock; edit customer and order details.
* [Get orders by customer or date](tutorials/orders-customer-date.md) — Use query parameters to list orders by different criteria.

## Reference

Review reference topics for the Bookstore Management API's three endpoints.

### Books endpoint

The **[books endpoint](reference/books.md)** connects to your inventory database.

* [POST books](reference/post-books.md)
* [PATCH books](reference/patch-books.md)
* [DELETE books](reference/delete-books.md)

### Customers endpoint

The **[customers endpoint](reference/customers.md)** connects to your customer database.

* [POST customers](reference/post-customers.md)
* [PATCH customers](reference/patch-customers.md)
* [DELETE customers](delete-customers.md)

### Orders endpoint

The **[Orders endpoint](reference/orders.md)** supports your order management and point-of-sale systems.

* [POST orders](reference/post-orders.md)
* [PATCH orders](reference/patch-orders.md)
* [DELETE orders](reference/delete-orders.md)
