# User Management API

> 📅 Developed in 2024 | Migrated to GitHub 2025

RESTful API for user management with Node.js and Express.

## Tech Stack

- Node.js 18+
- Express 4.18
- MongoDB (with Mongoose)
- JWT Authentication
- bcrypt

## Installation

```bash
npm install
```

## Environment Variables

Create a `.env` file:

```
PORT=3000
MONGODB_URI=mongodb://localhost:27017/usersdb
JWT_SECRET=your_secret_key
```

## Running

```bash
npm start
```

Development mode:

```bash
npm run dev
```

## API Endpoints

### Authentication
- POST /api/auth/register - Register new user
- POST /api/auth/login - Login user

### Users (Protected)
- GET /api/users - Get all users
- GET /api/users/:id - Get user by ID
- PUT /api/users/:id - Update user
- DELETE /api/users/:id - Delete user
