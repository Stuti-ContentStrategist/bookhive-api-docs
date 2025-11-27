# Data Models

## Book Object

{
  "id": 101,
  "title": "The Silent Reader",
  "author": "Jane Foster",
  "genre": "Mystery",
  "year": 2021
}

Fields:
id       number    Unique identifier  
title    string    Title of the book  
author   string    Author name  
genre    string    Category  
year     number    Publication year  

------------------------------------------------------------

## Author Object

{
  "id": 11,
  "name": "Jane Foster",
  "books": [101, 105, 108]
}
