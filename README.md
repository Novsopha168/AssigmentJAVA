
# Library Management System

## Overview

This Library Management System (LMS) is designed to manage the operations of a library efficiently. It includes features for managing categories, authors, publishers, books, members, and book transactions like issuing and returning books.

## Features

- Category Management: Add, update, and delete book categories.
- Author Management: Add, update, and delete authors.
- Publisher Management: Add, update, and delete publishers.
- Book Management: Add, update, and delete books.
- Member Management: Add, update, and delete library members.
- Issue Book: Issue books to library members.
- Return Book: Manage the return of books issued to members.

## API Endpoints

### Category
- GET /categories: Get all categories
- POST /categories: Create a new category
- PUT /categories/:id: Update a category
- DELETE /categories/:id: Delete a category

### Author
- GET /authors: Get all authors
- POST /authors: Create a new author
- PUT /authors/:id: Update an author
- DELETE /authors/:id: Delete an author

### Publisher
- GET /publishers: Get all publishers
- POST /publishers: Create a new publisher
- PUT /publishers/:id: Update a publisher
- DELETE /publishers/:id: Delete a publisher

### Book
- GET /books: Get all books
- POST /books: Create a new book
- PUT /books/:id: Update a book
- DELETE /books/:id: Delete a book

### Member
- GET /members: Get all members
- POST /members: Create a new member
- PUT /members/:id: Update a member
- DELETE /members/:id: Delete a member

### Issue Book
- POST /issues: Issue a book to a member

### Return Book
- POST /returns: Return a book issued to a member

## Database Schema

### Category
- id: Integer, Primary Key
- name: String

### Author
- id: Integer, Primary Key
- name: String

### Publisher
- id: Integer, Primary Key
- name: String

### Book
- id: Integer, Primary Key
- title: String
- category_id: Integer, Foreign Key
- author_id: Integer, Foreign Key
- publisher_id: Integer, Foreign Key
- available_copies: Integer

### Member
- id: Integer, Primary Key
- name: String
- email: String

### Issue
- id: Integer, Primary Key
- book_id: Integer, Foreign Key
- member_id: Integer, Foreign Key
- issue_date: Date

### Return
- id: Integer, Primary Key
- book_id: Integer, Foreign Key
- member_id: Integer, Foreign Key
- return_date: Date

## Contributing

Contributions are welcome! Please create a pull request or open an issue to discuss what you would like to change.

## License

This project is licensed under the MIT License.

