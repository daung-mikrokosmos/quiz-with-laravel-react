# Quiz Game

A full-stack web application for creating and playing quizzes, built with Laravel for the backend and React for the frontend.

## Table of Contents

- [Features](#features)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Backend Setup (Laravel)](#backend-setup-laravel)
- [Frontend Setup (React)](#frontend-setup-react)
- [Usage](#usage)
- [API Endpoints](#api-endpoints)
- [User Roles and Permissions](#user-roles-and-permissions)
- [Contributing](#contributing)
- [License](#license)

## Features

- User authentication and role management
- Create and manage quizzes with multiple-choice questions
- Different levels for quizzes
- Real-time quiz play
- Responsive design

## Prerequisites

- PHP (latest version)
- Composer
- Node.js and npm (or yarn)
- MySQL or another supported database

## Installation

### Backend Setup (Laravel)

1. Clone the repository:
    ```bash
    git clone https://github.com/yourusername/quiz-game.git
    cd quiz-game
    ```

2. Install dependencies:
    ```bash
    composer install
    ```

3. Set up the environment file:
    ```bash
    cp .env.example .env
    ```

4. Configure your database in the `.env` file:
    ```dotenv
    DB_CONNECTION=mysql
    DB_HOST=127.0.0.1
    DB_PORT=3306
    DB_DATABASE=your_database_name
    DB_USERNAME=your_database_username
    DB_PASSWORD=your_database_password
    ```

5. Generate an application key:
    ```bash
    php artisan key:generate
    ```

6. Run the migrations:
    ```bash
    php artisan migrate
    ```

7. Seed the database with initial data (optional):
    ```bash
    php artisan db:seed
    ```

8. Start the development server:
    ```bash
    php artisan serve
    ```

### Frontend Setup (React)

1. Navigate to the frontend directory:
    ```bash
    cd frontend
    ```

2. Install dependencies:
    ```bash
    npm install
    ```

3. Start the development server:
    ```bash
    npm start
    ```

## Usage

1. Register or log in as a user.
2. Depending on your role, create quizzes with multiple-choice questions.
3. Assign levels to quizzes.
4. Play quizzes and see your results.

## API Endpoints

- **Authentication**
  - `POST /api/register` - Register a new user
  - `POST /api/login` - Log in a user

- **Quizzes**
  - `GET /api/quizzes` - Get all quizzes
  - `POST /api/quizzes` - Create a new quiz
  - `GET /api/quizzes/{id}` - Get a specific quiz
  - `PUT /api/quizzes/{id}` - Update a specific quiz
  - `DELETE /api/quizzes/{id}` - Delete a specific quiz

- **Questions**
  - `GET /api/quizzes/{quiz_id}/questions` - Get all questions for a quiz
  - `POST /api/quizzes/{quiz_id}/questions` - Create a new question for a quiz
  - `GET /api/questions/{id}` - Get a specific question
  - `PUT /api/questions/{id}` - Update a specific question
  - `DELETE /api/questions/{id}` - Delete a specific question

- **Levels**
  - `GET /api/levels` - Get all levels
  - `POST /api/levels` - Create a new level
  - `GET /api/levels/{id}` - Get a specific level
  - `PUT /api/levels/{id}` - Update a specific level
  - `DELETE /api/levels/{id}` - Delete a specific level

## User Roles and Permissions

- **Admin**
  - Can manage all quizzes, questions, and levels
  - Can manage users and their roles

- **Editor**
  - Can create and manage quizzes and questions

- **User**
  - Can play quizzes and view results

## Contributing

1. Fork the repository.
2. Create a new branch.
3. Make your changes.
4. Submit a pull request.

## License

This project is licensed under the MIT License.
