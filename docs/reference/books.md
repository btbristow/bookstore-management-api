---
layout: page
---
# Books

Use the `books` endpoint when building inventory management features. For example, add a menu item that returns a [list of books](../tutorials/get-store-inventory.md) in stock or a form where booksellers add new books from deliveries.

## Request

To call the `books` endpoint using curl, enter `curl -X GET {server_url}{port}/books`.

## Response

The following sections contain an example response with a complete book object. They also list property definitions.

### Response Example

```json
    {
      "id": "9hne",
      "title": "The Mysteries of Pittsburgh",
      "author_last_name": "Chabon",
      "author_first_name": "Michael",
      "publisher": "Open Road Media",
      "year_published": 2011,
      "ISBN-10": 9781453234099,
      "genre": "fiction",
      "format": "hardcover",
      "condition": "new",
      "price": "24.99",
      "in_stock": 2
    }
```

### Response Properties

| **Property**        | **Type** | **Description**                                                                                 |
|---------------------|----------|-------------------------------------------------------------------------------------------------|
| `id`                | string   | Indicates the book's unique identifier.                                                         |
| `title`             | string   | Indicates the book title, which can differ by `ISBN-10` for the same title.                                        |
| `author_last_name`  | string   | Indicates the author's last name.                                                               |
| `author_first_name` | string   | Indicates the author's first name.                                                              |
| `publisher`         | string   | Indicates the book publisher.                                                                   |
| `year_published`    | string   | Indicates the year the edition was published.                                                   |
| `ISBN-10`           | number   | Indicates the ISBN-10 number. ISBN-13 is not supported.                                         |
| `genre`             | string   | Indicates the book genre, for example, **nonfiction**.                                           |
| `format`            | string   | Indicates the book format as **paperback** or **hardcover**.                                    |
| `condition`         | string   | Indicates if the book is **new** or **used**.                                           |
| `price`             | string   | Indicates the book price in USD using dollars and cents, for example *9.99* or *24.99*                                            |
| `in_stock`          | number   | Indicates the number of copies of the book in stock.                                                |

## Methods

The `books` endpoint supports the following methods:

* [POST books](post-books.md)
* [PATCH books](patch-books.md)
* [DELETE books](reference/delete-books.md)
