---
layout: page
---
# Customers

Use the `customers` endpoint to build customer management features. For example, add a form to enter new customer details. Or, edit existing customer details.

## Request

To call the `customers` endpoint with curl, use `curl -X GET {server_url}:{port}/customers`.

## Response

The following sections contain an example response with a complete customer object. They also list property definitions.

### Response Example

```json
    {
      "id": "8zsx",
      "last_name": "Jones",
      "first_name": "Jenny",
      "telephone": 7187451673,
      "email": "jjones@proton.me"
    }
```

### Response Properties

| **Property**  | **Type** | **Description**                             |
|---------------|----------|---------------------------------------------|
| `id` | string   | Indicates the customer's unique identifier. |
| `last_name`   | string   | Indicates the customer's last name.         |
| `first_name`  | string   | Indicates the customer's last name.         |
| `telephone`   | number   | Indicates the customer's phone number.      |
| `email`       | string   | Indicates the customer's email address.     |

## Methods

The `customers` endpoint supports the following methods:

* [POST customers](post-customers.md)
* [PATCH customers](patch-customers.md)
* [DELETE customers](delete-customers.md)
