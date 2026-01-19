# 🔐 SecureAuth - Enterprise User Management API

[![Node.js](https://img.shields.io/badge/Node.js-18+-339933?style=for-the-badge&logo=node.js&logoColor=white)](https://nodejs.org/)
[![Express](https://img.shields.io/badge/Express-4.18-000000?style=for-the-badge&logo=express&logoColor=white)](https://expressjs.com/)
[![MongoDB](https://img.shields.io/badge/MongoDB-6.0-47A248?style=for-the-badge&logo=mongodb&logoColor=white)](https://www.mongodb.com/)
[![JWT](https://img.shields.io/badge/JWT-Auth-000000?style=for-the-badge&logo=json-web-tokens&logoColor=white)](https://jwt.io/)

> Enterprise-grade user authentication system with JWT & role-based access control

Professional RESTful API built with Node.js and Express, featuring secure authentication, password hashing with bcrypt, and MongoDB integration for scalable user management.

## ✨ Key Features

- **🔐 Secure Authentication** - JWT-based authentication with token expiration
- **🔒 Password Security** - bcrypt hashing with salt rounds
- **🛡️ Protected Routes** - Middleware-based route protection
- **✅ Input Validation** - Request validation and sanitization
- **⚡ Fast Performance** - Optimized MongoDB queries
- **🚨 Error Handling** - Comprehensive error management
- **📝 Clean Code** - MVC architecture with separation of concerns

## 🛠️ Tech Stack

| Technology | Version | Purpose |
|------------|---------|---------|
| Node.js    | 18+     | Runtime environment |
| Express    | 4.18    | Web framework |
| MongoDB    | 6.0+    | Database |
| Mongoose   | 7.x     | ODM for MongoDB |
| JWT        | 9.x     | Token-based authentication |
| bcrypt     | 5.x     | Password hashing |

## 🚀 Quick Start

### Prerequisites
- Node.js 18 or higher
- MongoDB 6.0 or higher (local or MongoDB Atlas)
- npm or yarn

### Installation

```bash
# Clone the repository
git clone https://github.com/kelvinmendoza59/user-management-api.git
cd user-management-api

# Install dependencies
npm install

# Create environment file
cp .env.example .env
# Edit .env with your configuration
```

### Environment Variables

Create a `.env` file in the root directory:

```env
# Server Configuration
PORT=3000
NODE_ENV=development

# Database
MONGODB_URI=mongodb://localhost:27017/secureauth
# Or use MongoDB Atlas:
# MONGODB_URI=mongodb+srv://username:password@cluster.mongodb.net/secureauth

# JWT Configuration
JWT_SECRET=your_super_secret_key_change_this_in_production
JWT_EXPIRES_IN=7d

# Security
BCRYPT_ROUNDS=10
```

### Running the Application

```bash
# Development mode (with nodemon)
npm run dev

# Production mode
npm start

# The API will be available at http://localhost:3000
```

## 📡 API Endpoints

### Authentication

| Method | Endpoint | Description | Auth Required |
|--------|----------|-------------|---------------|
| POST | `/api/auth/register` | Register new user | ❌ |
| POST | `/api/auth/login` | User login | ❌ |

**Register Example:**
```bash
curl -X POST http://localhost:3000/api/auth/register \
  -H "Content-Type: application/json" \
  -d '{
    "name": "John Doe",
    "email": "john@example.com",
    "password": "SecurePass123!"
  }'
```

**Login Example:**
```bash
curl -X POST http://localhost:3000/api/auth/login \
  -H "Content-Type: application/json" \
  -d '{
    "email": "john@example.com",
    "password": "SecurePass123!"
  }'
```

### User Management (Protected)

| Method | Endpoint | Description | Auth Required |
|--------|----------|-------------|---------------|
| GET | `/api/users` | Get all users | ✅ |
| GET | `/api/users/:id` | Get user by ID | ✅ |
| PUT | `/api/users/:id` | Update user | ✅ |
| DELETE | `/api/users/:id` | Delete user | ✅ |

**Get Users Example:**
```bash
curl -X GET http://localhost:3000/api/users \
  -H "Authorization: Bearer YOUR_JWT_TOKEN"
```

## 📂 Project Structure

```
user-management-api/
├── controllers/        # Request handlers
│   ├── authController.js
│   └── userController.js
├── models/            # Mongoose schemas
│   └── User.js
├── routes/            # API routes
│   ├── auth.js
│   └── users.js
├── middleware/        # Custom middleware
│   └── auth.js
├── utils/             # Helper functions
│   └── errorHandler.js
├── server.js          # App entry point
├── .env.example       # Environment template
└── package.json       # Dependencies
```

## 🔒 Security Features

- ✅ **Password Hashing** - Passwords hashed with bcrypt (10 rounds)
- ✅ **JWT Tokens** - Secure token-based authentication
- ✅ **Protected Routes** - Middleware-based access control
- ✅ **Input Validation** - Request validation and sanitization
- ✅ **Error Handling** - No sensitive data in error responses
- ✅ **CORS Enabled** - Configurable Cross-Origin Resource Sharing

## 🧪 Testing

```bash
# Run tests (if implemented)
npm test

# Test with curl or Postman
# See API Endpoints section for examples
```

## 📈 Roadmap

- [ ] Role-based access control (Admin, User, Guest)
- [ ] Password reset functionality via email
- [ ] Email verification for new users
- [ ] Refresh token mechanism
- [ ] Rate limiting for API endpoints
- [ ] Unit and integration tests
- [ ] API documentation with Swagger
- [ ] Docker containerization

## 🤝 Contributing

This is a personal project showcasing my backend development skills. However, suggestions and feedback are welcome!

## 📧 Contact

**Kelvin Mendoza**
- 🌐 Portfolio: [portfolio-web-kelvin.vercel.app](https://portfolio-web-kelvin.vercel.app)
- 📧 Email: kelvinmendoza309@gmail.com
- 🐙 GitHub: [@kelvinmendoza59](https://github.com/kelvinmendoza59)

## 📝 License

This project is for portfolio demonstration purposes.

---

<p align="center">
  <sub>Built with Node.js and Express 💚 | Part of my Full-stack Portfolio</sub>
</p>
