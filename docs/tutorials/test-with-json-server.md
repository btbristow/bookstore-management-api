---
layout: single
title: Test with JSON Server
toc: true
toc_sticky: true
sidebar:
  nav: "docs"
---
This tutorial takes about 20 minutes to complete and explains how to test the Bookstore Management API locally.

You will use [JSON Server](https://www.npmjs.com/package/json-server), which simulates a REST API through a mock database in a JSON file.

## Prerequisites

To complete this tutorial, you need:

* A Windows, Mac, or Linux computer.
* Access to [curl](https://curl.se/download.html) on the command line.
* A current or long-term support (LTS) version of [Node.js](https://nodejs.org/en/download/package-manager).
* (Optional) A [GitHub](https://github.com/) account and a Git client.

**Tip:** After you install Node.js, add `npm` to your system path so you can run it from any directory.
{: .notice--success}

## Install and run JSON Server

To install and run JSON Server:

1. On the command line, to install JSON Server, type `npm i json-server`.

1. On GitHub, use Git to clone the [Bookstore Management API repository](https://github.com/btbristow/bookstore-management-api). Or, simply download the repository.

1. On the command line, browse to `/path/to/bookstore-management-api-main/api`.

1. Do one of the following:

    * **Windows** — Type `bookstore-management.bat`.

    * **macOS or Linux** — Type `chmod +x bookstore-management.sh`. Then, type `./bookstore-management.sh`.

    JSON Server starts in your terminal emulator and listens for API requests. Open a new terminal window to send them.

## Troubleshooting

If JSON Server fails to run, confirm that port 3000 is available on your network.

To change the port, add `-p {port}` to the script. For example, in `start-server.sh`:

```bash
#!/bin/bash
json-server -p 3001 bookstore-management.json
```

## Related topics

* [Get store inventory](get-store-inventory.md)
* [Create an order](create-an-order.md)
* [Get orders by customer or date](tutorials/orders-customer-date.md)
