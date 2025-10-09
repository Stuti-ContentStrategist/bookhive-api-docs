# 📚 BookHive API Documentation
*A sample API documentation project developed as part of my content strategy and technical writing portfolio.*

---

## 📑 Table of Contents

1. [🧭 Overview](#%F0%9F%A7%AD-overview)
2. [🌐 Base URL](#%F0%9F%8C%90-base-url)
3. [🔐 Authentication](#%F0%9F%94%90-authentication)
4. [📘 Endpoints](#%F0%9F%93%98-endpoints)
   - [Get All Books](#get-all-books)
   - [Get a Book by ID](#get-a-book-by-id)
   - [Add a New Book](#add-a-new-book)
   - [Update Book Details](#update-book-details)
   - [Delete a Book](#delete-a-book)
5. [⚠️ Error Codes](#%E2%9A%A0%EF%B8%8F-error-codes)
6. [💬 Example Use Case](#%F0%9F%92%AC-example-use-case)
7. [🧾 Versioning](#%F0%9F%A7%BE-versioning)
8. [🧠 Notes for Documentation Reviewers](#%F0%9F%A7%A0-notes-for-documentation-reviewers)
9. [👩‍💻 Author](#%F0%9F%91%A9%E2%80%8D%F0%9F%92%BB-author)


---

## 🧭 Overview {#overview}
The **BookHive API** allows users to access, add, update, and manage books and authors in the BookHive digital library system.  
It enables integration with reading apps, inventory dashboards, or recommendation systems.

---

## 🌐 Base URL {#base-url}

[https://api.bookhive.com/v1](https://api.bookhive.com/v1)

---
## 🔐 Authentication {#authentication}

All endpoints require an **API key** for authentication.  

Include the key in the request header as follows:

Authorization: Bearer YOUR_API_KEY

curl -H "Authorization: Bearer abc123xyz" https://api.bookhive.com/v1/books

---

## 📘 Endpoints {#endpoints}


### 1. Get All Books {#get-all-books}

Retrieve a list of all available books.

#### Endpoint:

GET /books

#### Example Request:

curl -X GET "https://api.bookhive.com/v1/books" \
-H "Authorization: Bearer YOUR_API_KEY"

#### Response:

[
  {
    "id": 101,
    "title": "The Silent Reader",
    "author": "Jane Foster",
    "genre": "Fiction",
    "published_year": 2021
  },
  {
    "id": 102,
    "title": "API Design for Writers",
    "author": "Alan Kent",
    "genre": "Technology",
    "published_year": 2024
  }
]


### 2. Get a Book by ID {#get-a-book-by-id}

Retrieve detailed information for a single book.

#### Endpoint:

GET /books/{id}

#### Example Request:

GET /books/101

#### Response:

{"id": 101,
  
  "title": "The Silent Reader",
  
  "author": "Jane Foster",
  
  "genre": "Fiction",
  
  "published_year": 2021,
  
  "summary": "A touching story about solitude and imagination."}

### 3. Add a New Book {#add-a-new-book}

Add a new book to the database.

#### Endpoint:

POST /books

#### Request Body:

{"title": "The Cloud Whisperer",
  
  "author": "Liam Brooks",
  
  "genre": "Fantasy",
  
  "published_year": 2023}

#### Response:
{"message": "Book added successfully.",
  
  "book_id": 103}

### 4. Update Book Details {#update-book-details}

Update an existing book’s information.

#### Endpoint:

PUT /books/{id}

#### Example Request:

PUT /books/103

#### Request Body:

{"genre": "Science Fiction",
 
 "published_year": 2024}

#### Response:

{"message": "Book details updated successfully."}

### 5. Delete a Book {#delete-a-book}

Remove a book from the database.

#### Endpoint:

DELETE /books/{id}

#### Example Request:

DELETE /books/103

Authorization: Bearer YOUR_API_KEY

#### Response:

{ "message": "Book deleted successfully." }

---

## ⚠️ Error Codes {#error-codes}

| Status Code | Meaning      | Description                       |
|-------------|-------------|------------------------------------|
| **200**     | OK          | Request was successful.            |
| **201**     | Created     | New resource created successfully. |
| **400**     | Bad Request | Missing or invalid parameters.     |
| **401**     | Unauthorized| Invalid or missing API key.        |
| **404**     | Not Found   | Resource does not exist.           |
| **500**     | Server Error| Problem with the BookHive server.  |

---



## 💬 Example Use Case {#example-use-case}

A content strategist working with a reading app could use the BookHive API to:
Auto-update book collections from BookHive’s database
Generate book recommendation lists dynamically
Manage author profiles and their published works

---

## 🧾 Versioning {#versioning}

The current version of the API is v1.
Future updates will follow the format:

https://api.bookhive.com/v2

---

## 🧠 Notes for Documentation Reviewers {#notes-for-documentation-reviewers}
This project demonstrates:

Clear structure of API documentation
Consistent formatting and code samples
Concise explanations for each endpoint
Professional presentation suitable for portfolios

---

## 👩‍💻 Author {#author}

Stuti Sanghvi – Content Strategist & Technical Writer
[GitHub Profile](https://github.com/Stuti-ContentStrategist)


