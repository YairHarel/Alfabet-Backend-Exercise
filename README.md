# Backend API Documentation

This project implements a RESTful API using FastAPI in Python for managing events with rate limiting and authentication.

## Architecture Overview

### Components:
- **MAIN:** Defines API routes, rate limiting middleware, and exception handling.
- **AUTH:** Handles user authentication and token generation.
- **EVENTS:** Manages CRUD operations for events.
- **DB_CONNECTOR:** Establishes the database connection and creates the event table.
- **EVENT:** Contains the Pydantic model for Event objects.
- **RATE_LIMIT:** Implements the RateLimiter class for controlling API requests.
- **USER:** Holds the Pydantic model for User objects.

### Technologies Used:
- **FastAPI:** Framework for building APIs with Python.
- **SQLAlchemy:** ORM for database operations.
- **JWT:** Authentication using JSON Web Tokens.
- **Pandas:** For CSV data handling.

## Setup Instructions

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/YairHarel/Alfabet-Backend-Exercise.git
   cd Alfabet-Backend-Exercise
Install Dependencies:
```
pip install -r requirements.txt
```
Set Up Database:

1. Ensure SQLite is installed.

2. Run the DB_CONNECTOR script to create the events table and populate it with data from the CSV.

3. Run the API Server:  ```uvicorn main:app --reload```
   
The API will run on http://127.0.0.1:8000 by default.

## Performance Optimizations
- **Rate Limiting:** Implemented using the RateLimiter class to restrict API requests and prevent abuse.
- **Background Tasks:** Event reminder functionality runs as a background task for efficiency.
- **Additional Notes**
- **Exception Handling:** Middleware catches exceptions to provide meaningful error responses.
- **API Endpoints:** Detailed endpoint documentation and functionality are provided in the code comments.
- **Security:** JWT-based authentication is used for securing API endpoints.
- **Database Handling:** SQLAlchemy ORM facilitates easy database interactions with SQLite.
