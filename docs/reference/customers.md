# Customers endpoint

Use the `customers` endpoint to build customer management features. For example, add a button that opens a form to add a new customer. Or, build in the ability to edit current customer information via `PATCH` request.

## Base endpoint

The `Customers` endpoint is located at `{server_url}/customers`.

## Response properties

The following sections contain an example response from the `customers` endpoint, along with property definitions.

### Example

```json
    {
      "last_name": "Jones",
      "first_name": "Jenny",
      "telephone": 7187451673,
      "email": "jjones@proton.me",
      "customer_id": 2,
    }
```

### Properties

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

To learn more about managing customers and adding them to orders, see the following tutorials.

- [Manage customers](../tutorials/manage-customers.md)
- [Work with orders](../tutorials/work-with-orders.md)
