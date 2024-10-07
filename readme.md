# Simple REST API

This is a simple REST API built with PHP and MySQL. It allows you to perform CRUD (Create, Read, Update, Delete) operations on user data.

## Prerequisites

- PHP >= 7.0
- Composer
- MySQL

## Installation

1. **Clone the repository:**
   ```bash
   git clone <repository-url>

2. **Navigate to the project directory:**
   ```bash
   cd simple_rest_api

3. **Install the required dependencies using Composer:**
   ```bash
    composer install
4. **Create a .env file in the project root with the following content:**
   ```bash
    DB_PASS=your_password

5. **Create the shop_test database and the users table in your MySQL database. Here’s a sample SQL command to create the users table:**

   ```bash
    CREATE TABLE users (
        id INT AUTO_INCREMENT PRIMARY KEY,
        name VARCHAR(100) NOT NULL,
        email VARCHAR(100) NOT NULL UNIQUE,
        age INT NOT NULL
    );

## Usage

### Endpoints

- **GET** `/api.php` - Retrieve all users  
- **GET** `/api.php?id=1` - Retrieve a user by ID  
- **POST** `/api.php` - Add a new user  
- **PUT** `/api.php?id=1` - Update a user by ID  
- **DELETE** `/api.php?id=1` - Delete a user by ID  


## Example Requests

- **Retrieve all users:**
   ```bash
   curl -X GET http://localhost/simple_rest_api/api.php

- **Retrieve a user by ID:**
   ```bash
   curl -X GET http://localhost/simple_rest_api/api.php?id=1

- **Add a new user:**
   ```bash
   curl -X POST http://localhost/simple_rest_api/api.php -H "Content-Type: application/json" -d '{"name": "John Doe", "email": "john@example.com", "age": 30}'

- **Update a user:**
   ```bash
   curl -X PUT http://localhost/simple_rest_api/api.php?id=1 -H "Content-Type: application/json" -d '{"name": "Jane Doe", "email": "jane@example.com", "age": 28}'

- **Delete a user:**
   ```bash
   curl -X DELETE http://localhost/simple_rest_api/api.php?id=1
