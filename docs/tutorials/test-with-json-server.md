---
layout: single
title: Test with JSON Server
toc: true
toc_sticky: true
sidebar:
  nav: "docs"
---
This tutorial takes about 20 minutes to complete and explains how to test the Bookstore Management API locally.

You will use [JSON Server](https://www.npmjs.com/package/json-server), <i class="fa-solid fa-arrow-up-right-from-square fa-xs"></i> which simulates a REST API through a mock database in a JSON file.

## Prerequisites

To complete this tutorial, you need:

* A Windows, Mac, or Linux computer.
* Access to [curl](https://curl.se/download.html) <i class="fa-solid fa-arrow-up-right-from-square fa-xs"></i> on the command line.
* A current or long-term support (LTS) version of [Node.js](https://nodejs.org/en/download/package-manager). <i class="fa-solid fa-arrow-up-right-from-square fa-xs"></i>
* (Optional) A [GitHub](https://github.com/) <i class="fa-solid fa-arrow-up-right-from-square fa-xs"></i> account and a Git client.

**Tip:** After you install Node.js, add `npm` to your system path so you can run it from any directory.
{: .notice--success}

## Install and run JSON Server

To install and run JSON Server:

1. On the command line, to install JSON Server, type `npm i json-server`.

1. On GitHub, use Git to clone the [Bookstore Management API repository](https://github.com/btbristow/bookstore-management-api). Or, download the repository as a ZIP file.

1. On the command line, browse to `/path/to/bookstore-management-api-main/api`.

1. Do one of the following:

    * **Windows** — Type `bookstore-management.bat`.

    * **macOS or Linux** — Type `chmod +x bookstore-management.sh`. Then, type `./bookstore-management.sh`.

    JSON Server starts in your terminal emulator and listens for API requests. Open a new terminal window to send them.

## Send requests with curl

This site's request examples use curl.

If testing locally with JSON Server, use the format `{server_url}:{port}`. For example, in a `GET` request, `curl -X GET localhost:3000/customers`.

**Note:** When testing with JSON Server, you do not use authentication in requests.
{: .notice--warning}

## Troubleshooting

If JSON Server fails to run, confirm that port 3000 is available on your network and change the port if necessary.

To change the port, add `-p {port}` to the script. For example, in `start-server.sh`:

```bash
#!/bin/bash
json-server -p 3001 bookstore-management.json
```

## Related topics

* [Get store inventory](get-store-inventory.md)
* [Create an order](create-an-order.md)
* [Get orders by customer or date](orders-customer-date.md)
