# Orders endpoint

Use the `orders` endpoint to build and manage order resources that contain the customer name, the books which were ordered, and the order number. The `orders` endpoint is the only endpoint that contains information about the other two endpoints in the Bookstore API, so it is frequently used to make custom requests, such as a list of books ordered by a customer. 

## Base endpoint

The `orders` endpoint is located at `{server_url}/orders`.

## Response properties

The following sections contain an example response from the `orders` endpoint, along with property definitions.

### Example

```json
    {
      "order_id": 3,
      "order_date": "2023-12-20",
      "items": 2,
      "customer_id": 4, 
      "book_id": [2,4]
    }
```

### Properties

| **Property**  | **Type** | **Description**                                                     |
|---------------|----------|---------------------------------------------------------------------|
| `order_id`    | number   | Indicates the order's unique identifier.                            |
| `order_date`  | string   | Indicates the order date in ISO 8601 format.                 |
| `items`       | number   | Indicates the number of books ordered.                              |
| `customer_id` | number   | Indicates the customer's unique identifier. |
| `book_id`     | array    | Indicates the book(s) purchased.                                    |

## Methods

The `orders` endpoint supports the following methods:

- [GET orders](get-orders.md)
- [POST orders](post-orders.md)
- [PATCH orders](patch-orders.md)
- [DELETE orders](delete-orders.md)

## Related topics

To learn more about working with orders, see the following topics.

- [Work with orders](../tutorials/work-with-orders.md)
- [Manage customers](../tutorials/manage-customers.md)
