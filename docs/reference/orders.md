---
layout: page
---
# Orders

Use the `orders` endpoint to build order management features. The `orders` endpoint is the only endpoint in the Bookstore Management API with information about the other endpoints, so it is designed for custom requests. For example, you might request a list of books ordered by a specific customer, as described in [GET orders by customer](get-orders.md)

## Request

To call the `orders` endpoint with curl, use `curl -X GET {server_url}/orders`.

## Response

The following sections contain an example response with a complete orders object. They also define object properties.

### Response Example

```json
    {
      "id": "8hgf",
      "order_date": "2023-12-20",
      "items": 2,
      "customer_id": "3mys", 
      "book_id": ["8kdt", "5mdz"]
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

## Methods

The `orders` endpoint supports the following methods:

* [GET orders by customer](reference/get-orders.md)
* [POST orders](reference/post-orders.md)
* [PATCH orders](reference/patch-orders.md)
* [DELETE orders](reference/delete-orders.md)
