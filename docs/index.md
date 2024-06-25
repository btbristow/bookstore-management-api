---
layout: single
title: Bookstore Management API
toc: true
toc_sticky: true
sidebar:
  nav: "docs"
---
The Bookstore Management API connects your bookstore app's user interface to its back end and is designed for bookseller workflows. Use it to build an app for any store: new or used, general or specialty, online or off.

This documentation contains everything you need to test and implement the Bookstore Management API.

**The Bookstore Management API supports:**

* Comprehensive book inventory management.
* CRUD operations on your inventory, customer, and order databases.
* Integration with point-of-sale systems.

## Get Started

Start by using a mock API service to make your first request.

* [Test with JSON Server](tutorials/test-with-json-server.md) — Test locally with no integration.
* [Get store inventory](tutorials/get-store-inventory.md) — Get an example list of books in stock.

## Tutorials

Review common bookseller workflows and use them to build a user-centric app for any store.

* [Create an order](tutorials/create-an-order.md) — Get a book title, add a customer, and create a new order.
* [Update a store](tutorials/update-store.md) — Update the books in stock, then edit customer and order details.
* [Get orders by customer or date](tutorials/orders-customer-date.md) — Use query parameters to list orders by different criteria.

## Reference

The following topics contain reference content for the three endpoints in the Bookstore Management API.

### Books endpoint

The **[books endpoint](reference/books.md)** connects to your inventory database and supports the following methods:

* [POST books](reference/post-books.md)
* [PATCH books](reference/patch-books.md)
* [DELETE books](reference/delete-books.md)

### Customers endpoint

The **[Customers endpoint](reference/customers.md)** sends customer details to your customer database and supports the following methods:

* [POST customers](reference/post-customers.md)
* [PATCH customers](reference/patch-customers.md)
* [DELETE customers](delete-customers.md)

### Orders endpoint

The **[Orders endpoint](reference/orders.md)** supports order management and point-of-sale systems through the following methods:

* [POST orders](reference/post-orders.md)
* [PATCH orders](reference/patch-orders.md)
* [DELETE orders](reference/delete-orders.md)
