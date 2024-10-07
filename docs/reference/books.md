---
layout: single
title: books
toc: true
toc_sticky: true
sidebar:
  nav: "docs"
---
Use the `books` endpoint when building inventory management features. For example, add a form where booksellers enter newly delivered books.

## Request

To call the `books` endpoint, enter `curl -X GET {server_url}{port}/books` with your server and port.

## Response

The following sections contain an example response and property definitions.

### Response Example

```json
   {
      "id": "099c",
      "title": "American Gods",
      "author_last_name": "Gaiman",
      "author_first_name": "Neil",
      "publisher": "Harper Collins",
      "year_published": 2002,
      "ISBN-10": 9780380789030,
      "genre": "fiction",
      "format": "paperback",
      "condition": "new",
      "price": "15.99",
      "in_stock": 5
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
| `ISBN-10`           | integer   | Indicates the ISBN-10 number. ISBN-13 is not supported.                                         |
| `genre`             | string   | Indicates the book genre, for example, **nonfiction**.                                           |
| `format`            | string   | Indicates the book format as **paperback** or **hardcover**.                                    |
| `condition`         | string   | Indicates if the book is **new** or **used**.                                           |
| `price`             | string   | Indicates the book price in USD using dollars and cents, for example *9.99* or *24.99*                                            |
| `in_stock`          | integer   | Indicates the number of copies in stock. Note that books with `0` copies appear in `GET` requests.                          |

## Methods

The `books` endpoint supports the following methods:

* [POST books](post-books.md)
* [PATCH books](patch-books.md)
* [DELETE books](delete-books.md)
