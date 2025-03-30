# FastAPI Todo List Backend

A simple todo list backend API built with FastAPI for personal understanding and learning purposes.

## Project Overview

This project is a RESTful API for managing todo items. It includes user authentication, database integration, and CRUD (Create, Read, Update, Delete) operations for todo items.

## Project Structure

```
BACKENDFASTAPI/
├── __pycache__/
├── auth.py             # Authentication handlers and JWT implementation
├── create_db.py        # Database initialization script
├── crud.py             # CRUD operations for the todo items
├── database.py         # Database connection and session management
├── main.py             # Main application entry point
├── main1.py            # Alternative main file
├── models.py           # SQLAlchemy ORM models
├── schemas.py          # Pydantic schemas for request/response validation
└── todos.db            # SQLite database file
```

## Features

- User registration and authentication
- JWT-based authentication
- Todo item management (create, read, update, delete)
- Data validation using Pydantic schemas
- SQLite database integration with SQLAlchemy ORM

## Prerequisites

- Python 3.6+
- FastAPI
- SQLAlchemy
- Pydantic
- python-jose (for JWT)
- passlib (for password hashing)

## Installation

1. Clone the repository or download the source files

2. Install the required dependencies:
   ```
   pip install fastapi uvicorn sqlalchemy pydantic python-jose[cryptography] passlib[bcrypt]
   ```

3. Initialize the database:
   ```
   python create_db.py
   ```

## Usage

1. Start the FastAPI server:
   ```
   uvicorn main:app --reload
   ```

2. Access the API documentation:
   - Swagger UI: http://localhost:8000/docs
   - ReDoc: http://localhost:8000/redoc

## API Endpoints

- **Authentication**
  - `POST /token` - Get access token
  - `POST /users/` - Register new user

- **Todo Operations**
  - `GET /todos/` - List all todos
  - `POST /todos/` - Create a new todo
  - `GET /todos/{todo_id}` - Get a specific todo
  - `PUT /todos/{todo_id}` - Update a todo
  - `DELETE /todos/{todo_id}` - Delete a todo

## Learning Purpose

This project was created for personal understanding and learning of FastAPI, SQLAlchemy, and authentication in Python web applications.
