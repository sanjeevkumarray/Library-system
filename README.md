Library Management System

Overview

This project is a Library Management System backend built using Node.js, Express.js, and MongoDB. It provides RESTful APIs for managing books, users, and borrowing/returning books.

Features

Add books to the library.

Retrieve all available books or a specific book.

Register users and handle user authentication.

Borrow and return books.

Fetch a user's borrowed books.

Input validation and error handling.

Secure authentication and authorization.

Technologies Used

Node.js - Server-side runtime.

Express.js - Web framework for building RESTful APIs.

MongoDB - NoSQL database for storing books and users.

Mongoose - ODM for MongoDB.

bcrypt - For password hashing.

jsonwebtoken (JWT) - For secure authentication.

dotenv - To manage environment variables.

API Endpoints

Book Management

POST /api/books - Add a new book.

GET /api/books - Get a list of all books.

GET /api/books/:id - Get details of a specific book.

User Management

POST /api/users - Register a new user.

POST /api/users/login - User login.

Borrowing & Returning Books

POST /api/borrow/:bookId/:userId - Borrow a book.

POST /api/return/:bookId/:userId - Return a book.

GET /api/users/:userId/books - Get all books borrowed by a user.

Installation & Setup

Backend

Clone the Repository

Install Dependencies

Set Up Environment Variables
Create a .env file in the backend directory and add the following:

Start the Backend Server

Frontend

Clone the Repository

Install Dependencies

Set Up Environment Variables
Create a .env file in the frontend directory and add the following:

Start the Frontend Server

Live Demo

Access the live application here:
Library System Management

Testing the API

Use Postman or cURL to test the endpoints.

Example request to add a book:

Code Structure

Security Measures

Passwords are hashed using bcrypt.

JWT authentication is used for secure user login.

Proper validation and error handling are implemented.

License

This project is open-source and available under the MIT License.

Contact

For any queries, contact your-email@example.com or visit GitHub.
