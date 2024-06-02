# Books endpoint

Use the `books` endpoint when building UI components that enable users to manage their store inventories. For example, build a featuire that gets a list of books in stock. Or, add a form where users add new books from a delivery.

## Base endpoint

The `books` endpoint is located at `{server_url}/books`.

## Response properties

The following sections contain an example response from the `books` endpoint, along with property definitions.

### Example

```json
    {
      "title": "The Mysteries of Pittsburgh",
      "author_last_name": "Chabon",
      "author_first_name": "Michael",
      "publisher": "Open Road Media",
      "year_published": 2011,
      "ISBN-10": 9781453234099,
      "genre": "fiction",
      "book_id": 1
    }
```

### Properties

| **Property**        | **Type** | **Description**                                                                                 |
|---------------------|----------|-------------------------------------------------------------------------------------------------|
| `title`             | string   | Indicates the book title, which can differ by `ISBN-10`.                                        |
| `author_last_name`  | string   | Indicates the author's last name.                                                               |
| `author_first_name` | string   | Indicates the author's first name.                                                              |
| `publisher`         | string   | Indicates the book publisher.                                                                   |
| `year_published`    | string   | Indicates the year the edition was published.                                                   |
| `ISBN-10`           | number   | Indicates the ISBN-13 number. ISBN-10 is not supported.                                         |
| `genre`             | string   | Indicates the book genre, for example **nonfiction**.                                           |
| `format`            | string   | Indicates the book format as **paperback** or **hardcover**.                                    |
| `in_stock`          | number   | Lists the number of copies of the book in stock.                                                |
| `id`                | number   | Indicates the book's unique identifier.                                                         |

## Methods

The `books` endpoint supports the following methods:

- [GET books](get-books.md)
- [POST books](post-books.md)
- [PATCH books](patch-books.md)
- [DELETE books](delete-books.md)

## Related topics

To learn more about managing store inventory with the 'books' endpoint, see the following tutorials.

- [Get store inventory](../tutorials/get-store-inventory.md)
- [Update store inventory](../tutorials/update-store-inventory.md)
