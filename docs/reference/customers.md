---
layout: page
---
# Customers endpoint

Use the `customers` endpoint to build customer management features. For example, add a form to enter new customer details. Or, use `PATCH` to edit existing customer information.

## Request

To call the `customers` endpoint with cURL, use `curl -X GET {server_url}:{port}/customers`.

## Response

The following sections contain an example response with a complete customer object. They also list property definitions.

### Response Example

```json
    {
      "last_name": "Jones",
      "first_name": "Jenny",
      "telephone": 7187451673,
      "email": "jjones@proton.me",
      "customer_id": 2,
    }
```

### Response Properties

| **Property**  | **Type** | **Description**                             |
|---------------|----------|---------------------------------------------|
| `last_name`   | string   | Indicates the customer's last name.         |
| `first_name`  | string   | Indicates the customer's last name.         |
| `telephone`   | number   | Indicates the customer's phone number.      |
| `email`       | string   | Indicates the customer's email address.     |
| `customer_id` | number   | Indicates the customer's unique identifier. |

## Methods

The `customers` endpoint supports the following methods:

- [GET customers](get-customers.md)
- [POST customers](post-customers.md)
- [PATCH customers](patch-customers.md)

## Related topics

To learn how to create customers and manage orders, see the following tutorials.

- [Work with customers](../tutorials/work-with-customers.md)
- [Manage customers and orders](../tutorials/customers-and-orders.md)
