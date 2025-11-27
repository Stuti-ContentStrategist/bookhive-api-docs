# Example Use Cases

## Search Books by Genre

curl -X GET "https://api.bookhive.com/v1/books?genre=Mystery" \
-H "Authorization: Bearer YOUR_API_KEY"

------------------------------------------------------------

## Add and Retrieve a Book

1. Add a book using POST /books  
2. Retrieve it using GET /books/{id}
