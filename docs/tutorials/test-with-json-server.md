---
layout: page
---
# Test with JSON Server

This tutorial takes about 20 minutes to complete and explains how to test the Bookstore Management API on your local computer.

You will use [JSON Server](https://www.npmjs.com/package/json-server), which simulates a REST API by substituting the database in your environment with a local JSON file.

## Prerequisites

To complete this tutorial, you need the following:

* A Windows, Mac, or Linux computer.
* Access to [curl](https://curl.se/download.html) on the command line.
* A current or long-term support (LTS) version of [Node.js](https://nodejs.org/en/download/package-manager).

    > **Tip:**
    > You will install JSON Server with Node Package Manager (npm). To run npm from any directory, add it to your system path after you install Node.js.

* *(Optional)* A GitHub account and a Git client.

## Install and run JSON Server

To install and run JSON Server:

1. On the command line, to install JSON Server, type `npm i json-server`.

1. On GitHub, use Git to clone the [Bookstore Management API repository](https://github.com/btbristow/bookstore-management-api). Or, simply download the repository.

1. On the command line, browse to `/path/to/bookstore-management-api-main/api`.

1. Do one of the following:

    a. **Windows** — Type `bookstore-management.bat`.

    b. **macOS or Linux** — Make the script to run executable by entering `chmod +x bookstore-management.sh`. Then, enter `./bookstore-management.sh`.

    JSON Server starts in your terminal emulator and listens for API requests. Open a new terminal window to send them.

## Troubleshooting

If JSON Server fails to run, confirm that port 3000 is available on your network.

To change the port, add `-p {port}` to the script file. For example, in `start-server.sh`:

```bash
#!/bin/bash
json-server -p 3001 bookstore-management.json
```

## Related topics

* [Get store inventory](get-store-inventory.md)
* [Create an order](create-an-order.md)
