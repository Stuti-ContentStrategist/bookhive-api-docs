# BookHive API Documentation

The BookHive API allows applications to retrieve, search, and manage book data. It is designed for developers building catalog apps, reading platforms, or systems that require structured book information.

## Overview

The API provides access to:
- Book information (title, author, genre, publication year)
- Searching and filtering capabilities
- Metadata and basic catalog functions

This documentation includes authentication details, endpoint references, example use cases, error codes, and data models.

## Base URL

https://api.bookhive.com/v1

## Authentication

All requests require an API key included in the header:

Authorization: Bearer YOUR_API_KEY

## Quick Start

Example request to fetch all books:

curl -X GET "https://api.bookhive.com/v1/books" \
-H "Authorization: Bearer YOUR_API_KEY"

Expected response:

[
  {
    "id": 101,
    "title": "The Silent Reader",
    "author": "Jane Foster",
    "year": 2021
  }
]

## Documentation Structure

authentication.md  
models.md  
errors.md  
examples.md  
changelog.md  
endpoints/books.md  
endpoints/authors.md  
