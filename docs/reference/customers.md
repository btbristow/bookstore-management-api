# Customers endpoint

Use the `customers` endpoint to build customer management features. For example, add a button that opens a form to add a new customer. Or, build in the ability to edit current customer information via `PATCH` request.

## Request

To call the `customers` endpoint in cURL, use `curl -X GET {server_url}:{port}/customers`.

## Response

The following sections contain an example response from the `customers` endpoint, along with property definitions.

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
| `last_name`   | string   | Indicates a customer's last name.         |
| `first_name`  | string   | Indicates a customer's last name.         |
| `telephone`   | number   | Indicates a customer's phone number.      |
| `email`       | string   | Indicates a customer's email address.     |
| `customer_id` | number   | Indicates a customer's unique identifier. |

## Methods

The `customers` endpoint supports the following methods:

- [GET customers](get-customers.md)
- [POST customers](post-customers.md)
- [PATCH customers](patch-customers.md)

## Related topics

To learn how to create customers and manage orders, see the following tutorials.

- [Work with customers](../tutorials/work-with-customers.md)
- [Manage customers and orders](../tutorials/customers-and-orders.md)
