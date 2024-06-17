---
layout: page
---
# Books

Use the `books` endpoint when building UI components for store inventory management. For example, build a feature that gets a [list of books](../tutorials/get-store-inventory.md) in stock. Or, add a form where users add new books received in a delivery.

## Request

To call the `books` endpoint with curl, use `curl -X GET {server_url}{port}/books`.

## Response

The following sections contain an example response with a complete book object. They also list property definitions.

### Response Example

```json
    {
      "id": "7dcd",
      "title": "The Mysteries of Pittsburgh",
      "author_last_name": "Chabon",
      "author_first_name": "Michael",
      "publisher": "Open Road Media",
      "year_published": 2011,
      "ISBN-10": 9781453234099,
      "genre": "fiction",
      "format": "hardcover",
      "in_stock": 1,
    }
```

### Response Properties

| **Property**        | **Type** | **Description**                                                                                 |
|---------------------|----------|-------------------------------------------------------------------------------------------------|
| `id`                | string   | Indicates the book's unique identifier.                                                         |
| `title`             | string   | Indicates the book title, which can differ by `ISBN-10` for the same book.                                        |
| `author_last_name`  | string   | Indicates the author's last name.                                                               |
| `author_first_name` | string   | Indicates the author's first name.                                                              |
| `publisher`         | string   | Indicates the book publisher.                                                                   |
| `year_published`    | string   | Indicates the year the edition was published.                                                   |
| `ISBN-10`           | number   | Indicates the ISBN-10 number. ISBN-13 is not supported.                                         |
| `genre`             | string   | Indicates the book genre, for example, **nonfiction**.                                           |
| `format`            | string   | Indicates the book format as **paperback** or **hardcover**.                                    |
| `in_stock`          | number   | Lists the number of copies of the book in stock.                                                |

## Methods

The `books` endpoint supports the following methods:

* [POST books](post-books.md)
* [PATCH books](patch-books.md)
