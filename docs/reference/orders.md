---
layout: single
title: orders
toc: true
toc_sticky: true
sidebar:
  nav: "docs"
---
Use the `orders` endpoint for order management features. The `orders` endpoint contains information about the other endpoints and is designed for custom requests. For example, [get a list of books](../tutorials/orders-customer-date.md#step-1-get-orders-by-customer) purchased by one customer.

## Request

To call the `orders` endpoint, enter `curl -X GET {server_url}/orders` with your server and port.

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
| `id`    | integer   | Indicates the order's unique identifier.                            |
| `order_date`  | integer   | Indicates the order date in [ISO 8601](https://www.iso.org/iso-8601-date-and-time-format.html) format. <i class="fa-solid fa-arrow-up-right-from-square fa-xs"></i>                |
| `items`       | number   | Indicates the number of books ordered.                              |
| `customer_id` | integer   | Indicates the customer's unique identifier. |
| `book_id`     | array of strings    | Indicates the unique identifier(s) for the book(s) purchased.                                    |
| `subtotal` | integer   | Indicates the order subtotal in USD with dollars and cents, for example *8.70* or *25.02*. |
| `tax` | integer   | Indicates the sales tax in USD. The test version of this API uses a [2024 New York State sales tax](https://www.nyc.gov/site/finance/business/business-nys-sales-tax.page) <i class="fa-solid fa-arrow-up-right-from-square fa-xs"></i> of 8.875%, but you can apply any percentage using custom logic.   |
| `subtotal` | integer   | Indicates the order total in USD. |

## Methods

The `orders` endpoint supports the following methods:

* [POST orders](post-orders.md)
* [PATCH orders](patch-orders.md)
* [DELETE orders](delete-orders.md)
