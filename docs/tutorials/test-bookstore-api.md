---
layout: page
---
# Test the Bookstore Management API

This topic outlines how to use json-server to test the Bookstore Management API wth no integration required.

The json-server package is built on Node.js, and simulates a REST API with a mock database file. It supports standard API methods such as `GET`, `POST`, `PUT`, and `DELETE`, and custom queries.

## Prerequisites

To complete these steps, you need a Windows, Mac, or Linux development machine with cURL on the command line to make API requests.

## Install and use json-server

To install and use json-server:

1. Download and install a current or LTS version of [Node.js](https://nodejs.org/en/download/package-manager). For the best results, add Node.js to your `PATH`.

1. Download and install [json-server](https://www.npmjs.com/package/json-server). For example, on MacOS with Node Package Manager (`npm`), use `npm install -g json-server`.

    > **Note:**
    > To run json-server, port 3000 must be available on your network.

1. Download the [API folder](https://github.com/btbristow/bookstore-management-api/tree/4227e30164eb37172b024df7f1dd5400c6e454b2/api) from our GitHub repository or clone it with your Git client.

1. On the command line, browse to the downloaded folder or repo.

1. Do one of the following:

    a. **Windows** — To run json-server against our mock database, type `bookstore-management.bat`.

    b. **MacOS or Linux** — Make the script executable with `chmod +x bookstore-management.sh`. Then, run the script: `./bookstore-management.sh`.

    json-server appears in your terminal emulator window and listens for API requests.

## Related topics

- [Get Started with the Boookstore Management API](tutorials/get-started.md)
- [Work with customers and orders](tutorials/customers-and-orders.md)
- [Authentication](reference/authentication.md)