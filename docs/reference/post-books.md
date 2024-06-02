# POST books

Use `POST` with the `books` endpoint to create new books in a store's inventory. You can add one or more complete books to the request body.

> ℹ️ Use the `POST` method to add books with a unique `ISBN-10` that the store has not previously carried. To update the number of *existing* books, use [PATCH books](patch-books.md) with the `in_stock` property instead.

## Request

To create a book with the `POST books` method, use the following cURL request.

```bash
curl -X POST '{server_url}:{port}/customers' \
--header 'Content-Type: application/json' \
--data '{
    "title": "The Power Broker: Robert Moses and the Fall of New York",
    "author_last_name": "Caro",
    "author_first_name": "Robert A.",
    "publisher": "Knopf Doubleday Publishing Group",
    "year_published": 1974,
    "ISBN-10": 9780394480763,
    "genre": "non-fiction",
    "format": "paperback",
    "in_stock": 1,
    "book_id": 4
}'
```

## Response

The following sections contain an example success response, along with error response codes.

### Success response code

When your `POST` request is successful, the Bookstore Management API returns a `201 Created`, along with the following response body.

```json
{
    "status": "PASS",
    "message": "Book created",
    "book_id": 2
}
```

### Error response codes

When your `POST` request is unsuccessful, The Bookstore Management API returns one of the following error response codes.

| Response Code | Description                                      |
|---------------|--------------------------------------------------|
| 400           | Bad Request  |
| 401           | Unauthorized  |
| 503           | Service Unavailable |

## Related Topics

- [Books endpoint](books.md)
- [PATCH books](patch-books.md)
