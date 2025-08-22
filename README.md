# Exam Portal

A full-stack exam portal built with React, Express, MongoDB, and JWT authentication.

## Features

- User registration and login (JWT-based authentication)
- Randomized exam questions
- Answer submission and scoring
- Protected API routes
- MongoDB Atlas integration

## Technologies

- Frontend: React
- Backend: Node.js, Express
- Database: MongoDB (Atlas)
- Authentication: JWT

## Getting Started

### Prerequisites

- Node.js & npm
- MongoDB Atlas account

### Installation

1. **Clone the repository**
   ```
   git clone <git remote add origin https://github.com/Madhumanu891/Exam-portal.git>
   cd Exam-Portal
   ```

2. **Backend Setup**
   - Go to the `backend` folder:
     ```
     cd backend
     ```
   - Install dependencies:
     ```
     npm install
     ```
   - Create a `.env` file:
     ```
     MONGO_URI=<your_mongodb_atlas_uri>
     JWT_SECRET=<your_jwt_secret>
     PORT=5000
     ```

   - Start the backend server:
     ```
     npm start
     ```

3. **Frontend Setup**
   - Go to the `frontend` folder:
     ```
     cd ../frontend
     ```
   - Install dependencies:
     ```
     npm install
     ```
   - Start the frontend:
     ```
     npm run dev
     ```

## API Endpoints

### Auth

- `POST /api/auth/register`  
  Register a new user  
  **Body:** `{ "name": "...", "email": "...", "password": "..." }`

- `POST /api/auth/login`  
  Login  
  **Body:** `{ "email": "...", "password": "..." }`

### Exam

- `GET /api/exam/questions`  
  Get 10 random questions (protected, requires `x-auth-token` header)

  ```

## Importing Questions

- Use MongoDB Compass or `mongoimport` to import a JSON file of questions.
- Example format:
  ```json
  [
    {
      "questionText": "What is the capital of France?",
      "options": ["Berlin", "London", "Paris", "Madrid"],
      "correctAnswer": "Paris"
    }
  ]
  ```

## License

MIT

## Author

Dhanaveni Madhu
