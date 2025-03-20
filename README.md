# Library Management System

## Overview
This project is a **Library Management System** backend built using **Node.js**, **Express.js**, and **MongoDB**. It provides RESTful APIs for managing books, users, and borrowing/returning books.

## Features
- Add books to the library.
- Retrieve all available books or a specific book.
- Register users and handle user authentication.
- Borrow and return books.
- Fetch a user's borrowed books.
- Input validation and error handling.
- Secure authentication and authorization.

## Technologies Used
- **Node.js** - Server-side runtime.
- **Express.js** - Web framework for building RESTful APIs.
- **MongoDB** - NoSQL database for storing books and users.
- **Mongoose** - ODM for MongoDB.
- **bcrypt** - For password hashing.
- **jsonwebtoken (JWT)** - For secure authentication.
- **dotenv** - To manage environment variables.

## API Endpoints
### Book Management
```sh
POST /api/books       # Add a new book
GET /api/books        # Get a list of all books
GET /api/books/:id    # Get details of a specific book
```

### User Management
```sh
POST /api/users       # Register a new user
POST /api/users/login # User login
```

### Borrowing & Returning Books
```sh
POST /api/borrow/:bookId/:userId   # Borrow a book
POST /api/return/:bookId/:userId   # Return a book
GET /api/users/:userId/books       # Get all books borrowed by a user
```

## Installation & Setup
### Backend
```sh
# Clone the Repository
git clone https://github.com/sanjeevkumarray/Backend.git
cd Backend

# Install Dependencies
npm install

# Set Up Environment Variables
echo "PORT=5000" >> .env
echo "MONGO_URI=<Your MongoDB URI>" >> .env
echo "JWT_SECRET=<Your JWT Secret>" >> .env

# Start the Backend Server
npm start
```

### Frontend
```sh
# Clone the Repository
git clone https://github.com/sanjeevkumarray/Library-system.git
cd Library-system

# Install Dependencies
npm install

# Set Up Environment Variables
echo "REACT_APP_API_URL=http://localhost:5000/api" >> .env

# Start the Frontend Server
npm start
```

## Live Demo
Access the live application here:
[Library System Management](https://library-system-managment.netlify.app/login)

## Testing the API
Use **Postman** or **cURL** to test the endpoints.

Example request to add a book:
```sh
curl -X POST http://localhost:5000/api/books \
     -H "Content-Type: application/json" \
     -d '{"title": "Book Title", "author": "Author Name", "ISBN": "123456789", "quantity": 5}'
```

## Code Structure
```sh
📦 library-management-system
 ┣ 📂 controllers   # Handles API logic
 ┣ 📂 models        # Database schemas
 ┣ 📂 routes        # API routes
 ┣ 📂 middleware    # Authentication & validation middleware
 ┣ 📜 server.js     # Entry point of the application
 ┣ 📜 .env.example  # Example environment variables
 ┗ 📜 README.md     # Project documentation
```

## Security Measures
- Passwords are hashed using **bcrypt**.
- JWT authentication is used for secure user login.
- Proper validation and error handling are implemented.

## License
This project is open-source and available under the [MIT License](LICENSE).

## Contact
For any queries, contact **your-email@example.com** or visit [GitHub](https://github.com/sanjeevkumarray).

