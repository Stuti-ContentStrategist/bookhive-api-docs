# Books Endpoints

## Get All Books
GET /books

Retrieves all available books.

Example:

curl -X GET "https://api.bookhive.com/v1/books" \
-H "Authorization: Bearer YOUR_API_KEY"

Sample response:

[
  {
    "id": 101,
    "title": "The Silent Reader",
    "author": "Jane Foster",
    "genre": "Mystery",
    "year": 2021
  }
]

------------------------------------------------------------

## Get Book by ID
GET /books/{id}

Retrieves a specific book by its ID.

Example:

curl -X GET "https://api.bookhive.com/v1/books/101" \
-H "Authorization: Bearer YOUR_API_KEY"

------------------------------------------------------------

## Add a New Book
POST /books

Required fields:
- title (string)
- author (string)

Optional fields:
- year (number)
- genre (string)

Example:

curl -X POST "https://api.bookhive.com/v1/books" \
-H "Authorization: Bearer YOUR_API_KEY" \
-H "Content-Type: application/json" \
-d '{
  "title": "Hidden Voices",
  "author": "Max Turner",
  "year": 2024,
  "genre": "Drama"
}'
