---
layout: single
title: orders
toc: true
toc_sticky: true
sidebar:
  nav: "docs"
---
Use the `orders` endpoint to build order management features. The `orders` endpoint contains information about the other endpoints and is designed for custom requests. For example, get a list of books [ordered by a certain customer](get-orders.md).

## Request

To call the `orders` endpoint using curl, enter `curl -X GET {server_url}/orders` with your server and port.

## Response

The following sections contain an example response and property definitions.

### Response Example

```json
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
```

### Response Properties

| **Property**  | **Type** | **Description**                                                     |
|---------------|----------|---------------------------------------------------------------------|
| `id`    | string   | Indicates the order's unique identifier.                            |
| `order_date`  | string   | Indicates the order date in [ISO 8601](https://www.iso.org/iso-8601-date-and-time-format.html) format.                 |
| `items`       | number   | Indicates the number of books ordered.                              |
| `customer_id` | string   | Indicates the customer's unique identifier. |
| `book_id`     | array    | In an array of strings, indicates the unique identifier(s) for the book(s) purchased.                                    |
| `subtotal` | string   | Indicates the order subtotal in USD using dollars and cents, for example *8.70* or *25.02*. |
| `tax` | string   | Indicates the sales tax in USD. The Bookstore Management API's test version applies 2024 [New York State sales tax](https://www.nyc.gov/site/finance/business/business-nys-sales-tax.page) of 8.875%, but you can pass in any percentage, calculated against the order `subtotal` property.   |
| `subtotal` | string   | Indicates the order total in USD. |

## Methods

The `orders` endpoint supports the following methods:

* [POST orders](reference/post-orders.md)
* [PATCH orders](reference/patch-orders.md)
* [DELETE orders](reference/delete-orders.md)
