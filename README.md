# Full Stack CRUD MySQL Web App

A simple web app built with **Node.js**, **Express.js**, and **MySQL** to manage user records. It allows you to **create**, **read**, and **delete** user information.

## Table of Contents

- [Features](#features)
- [Technologies Used](#technologies-used)
- [Installation](#installation)
- [Usage](#usage)
- [Contributing](#contributing)

## Features

- Allows creating a new user with **name**, **email**, and **age**.
- Retrieve and view all user records stored in the **MySQL database**.
- Delete a user record based on the **user ID**.
  
## Technologies Used

- **Node.js** - JavaScript runtime to build the server.
- **Express.js** - Web framework for handling HTTP requests and routes.
- **MySQL** - Relational database for storing user records.
- **JavaScript** - Used for creating server-side logic.

## Installation

1. **Clone the repository**:

    ```bash
    git clone https://github.com/rabumaabraham/Full-Stack-CRUD-MySQL-App.git
    ```

2. **Navigate into the project directory**:

    ```bash
    cd full-stack-crud-mysql-app
    ```

3. **Install dependencies**:

    Make sure you have Node.js installed. Then, run:

    ```bash
    npm install
    ```

4. **Create a `.env` file**:

    In the project root, create a `.env` file with the following content:

    ```env
    DB_HOST=localhost
    DB_USER=root
    DB_PASSWORD=your_mysql_password
    DB_NAME=user_management
    ```

    Replace `your_mysql_password` with your actual MySQL root password.

5. **Start the server**:

    Run the following command to start the server:

    ```bash
    node server.js
    ```

    The server will start on **http://localhost:3000**.

## Usage

1. **Get all users**:

    ```bash
    GET http://localhost:3000/users
    ```

    This will retrieve all user records stored in the database.

2. **Add a new user**:

    Send a **POST** request to add a new user:

    ```bash
    POST http://localhost:3000/users
    Content-Type: application/json
    {
        "name": "John Doe",
        "email": "john@example.com",
        "age": 30
    }
    ```

    This will add a new user to the `user_management` MySQL database.

3. **Delete a user**:

    Send a **DELETE** request to remove a user:

    ```bash
    DELETE http://localhost:3000/users/{userId}
    ```

    Replace `{userId}` with the ID of the user you want to delete.

## Contributing

Contributions are welcome! If you would like to improve this project, follow these steps:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Make your changes.
4. Commit the changes (`git commit -m 'Add some feature'`).
5. Push to the branch (`git push origin feature-branch`).
6. Create a pull request.
