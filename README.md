# 📚 BookHive API Documentation

This API documentation project was developed to showcase best practices in technical writing — including clarity, organization, and consistency in developer documentation.

***

### 📖 Contents at a Glance

This documentation covers:

* 🧭 Overview
* 🔐 Authentication
* 📘 Endpoints
* ⚠️ Error Codes
* 💬 Example Use Case
* 🧠 Notes for Reviewers
* 👩‍💻 Author

***

### 🧭 Overview

The **BookHive API** allows users to access, add, update, and manage books and authors in the BookHive digital library system. It enables integration with reading apps, inventory dashboards, or recommendation systems.

***

### 🌐 Base URL

```
https://api.bookhive.com/v1
```

***

### 🔐 Authentication

All endpoints require an API key for authentication.

Include the key in the request header as follows:

```
plain text

Authorization: Bearer YOUR_API_KEY
```

**Example:**

```bash
bash

curl -H "Authorization: Bearer abc123xyz" https://api.bookhive.com/v1/books
```

***

### 📘 Endpoints

#### 1️⃣ Get All Books

**Endpoint:** `GET /books`\
Retrieve a list of all available books.

**Example Request:**

```bash
bash

curl -X GET "https://api.bookhive.com/v1/books" \
-H "Authorization: Bearer YOUR_API_KEY"
```

**Response:**

```json
json

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
```

***

#### 2️⃣ Get a Book by ID

**Endpoint:** `GET /books/{id}`\
Retrieve detailed information for a single book.

**Example Request:**

```bash
bash

curl -X GET "https://api.bookhive.com/v1/books/101" \
-H "Authorization: Bearer YOUR_API_KEY"
```

**Response:**

```json
json

{
  "id": 101,
  "title": "The Silent Reader",
  "author": "Jane Foster",
  "genre": "Fiction",
  "published_year": 2021,
  "summary": "A touching story about solitude and imagination."
}
```

***

#### 3️⃣ Add a New Book

**Endpoint:** `POST /books`\
Add a new book to the database.

**Request Body:**

<pre class="language-json"><code class="lang-json"><strong>json
</strong><strong>
</strong><strong>{
</strong>  "title": "The Cloud Whisperer",
  "author": "Liam Brooks",
  "genre": "Fantasy",
  "published_year": 2023
}
</code></pre>

**Response:**

```json
json

{
  "message": "Book added successfully.",
  "book_id": 103
}
```

***

#### 4️⃣ Update Book Details

**Endpoint:** `PUT /books/{id}`\
Update an existing book’s information.

**Example Request:**

```bash
bash

curl -X PUT "https://api.bookhive.com/v1/books/103" \
-H "Authorization: Bearer YOUR_API_KEY" \
-d '{
  "genre": "Science Fiction",
  "published_year": 2024
}'
```

**Response:**

```json
json

{
  "message": "Book details updated successfully."
}
```

***

#### 5️⃣ Delete a Book

**Endpoint:** `DELETE /books/{id}`\
Remove a book from the database.

**Example Request:**

```bash
bash

curl -X DELETE "https://api.bookhive.com/v1/books/103" \
-H "Authorization: Bearer YOUR_API_KEY"
```

**Response:**

```json
json

{
  "message": "Book deleted successfully."
}
```

***

### ⚠️ Error Codes

| Status Code | Meaning      | Description                        |
| ----------- | ------------ | ---------------------------------- |
| 200         | OK           | Request was successful.            |
| 201         | Created      | New resource created successfully. |
| 400         | Bad Request  | Missing or invalid parameters.     |
| 401         | Unauthorized | Invalid or missing API key.        |
| 404         | Not Found    | Resource does not exist.           |
| 500         | Server Error | Problem with the BookHive server.  |

***

### 💬 Example Use Case

A content strategist working with a reading app could use the BookHive API to:

* Auto-update book collections from BookHive’s database
* Generate book recommendation lists dynamically
* Manage author profiles and their published works

***

### 🧾 Versioning

The current version of the API is **v1**.\
Future updates will follow this format:

```
https://api.bookhive.com/v2
```

***

### 🧠 Notes for Documentation Reviewers

This project demonstrates:

* Clear structure of API documentation
* Consistent formatting and code samples
* Concise explanations for each endpoint
* Professional presentation suitable for portfolios

***

### 👩‍💻 Author

**Stuti Sanghvi**\
Content Strategist & Technical Writer

Combining a strong background in content strategy and hands-on technical writing, Stuti focuses on delivering documentation that bridges the gap between complex technology and user understanding.

Her professional interests include:

* API documentation and SDK guides
* Release notes and product updates
* User manuals and knowledge base articles
* Content design and UX writing for technical products

This **BookHive API Documentation** project was created to demonstrate best practices in technical writing — including logical structuring, consistency in style, and clear code examples — as part of her professional documentation portfolio.

#### **Connect with the Author:**

💼 [LinkedIn](https://linkedin.com/in/stuti-sanghvi)\
💌 [Email](mailto:stutisanghvi7@gmail.in)\
🌐 [Notion Profile](https://www.notion.so/Stuti-Sanghvi-Content-Strategist-Technical-Writer-29cf34655bbd809589e7d360b8e98ed1)\
🔗 [GitHub](https://github.com/Stuti-ContentStrategist)
