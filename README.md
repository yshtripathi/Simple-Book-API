# Simple Books API — Functional Testing with Postman & Newman

This repository contains a Postman collection and Newman HTML report used to test the Simple Books API (`https://simple-books-api.click`). The API supports basic operations such as checking status, listing books, managing orders, and client registration.

## API Overview

The Simple Books API supports the following endpoints:

- `GET /status`  
  Checks the health of the API.

- `GET /books`  
  Retrieves a list of books. Supports optional query parameters:  
  - `type` (fiction or non-fiction)  
  - `limit` (1–20)  

- `GET /books/:bookId`  
  Fetches details of a specific book by its ID.

- `POST /orders`  
  Creates a new book order.

[...]

*(Feel free to expand this section with more endpoints, request/response details, or example payloads.)*

## Contents of this Repository

| File                          | Description                                   |
|------------------------------|-----------------------------------------------|
| `Simple_Book_API.json`       | Postman collection containing API workflows   |
| `SimpleBookReport.html`      | Newman-generated HTML report of test results  |
| `README.md`                  | Project overview and usage instructions       |

## How to Run the Tests

1. **Import** the Postman collection (`Simple_Book_API.json`) into Postman.  
2. Optionally, configure environment variables if used.  
3. Use Postman’s Runner to execute the workflow.  

Alternatively, to run via Newman (CLI):

```bash
newman run Simple_Book_API.json -r html
