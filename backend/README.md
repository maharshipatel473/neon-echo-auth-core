
# Authentication Backend with MongoDB

This is a backend for authentication using Express and MongoDB.

## Setup Instructions

1. Install dependencies:
   ```
   npm install
   ```

2. Create a `.env` file based on `.env.example` and fill in your MongoDB connection string and JWT secret:
   ```
   PORT=5000
   MONGODB_URI=mongodb://localhost:27017/authentication_db
   JWT_SECRET=your_jwt_secret_here
   JWT_EXPIRE=30d
   ```

3. Start the server:
   ```
   npm run dev
   ```

## API Endpoints

### Authentication
- `POST /api/auth/register` - Register a new user
- `POST /api/auth/login` - Login a user
- `GET /api/auth/me` - Get current user (protected route)

## Request Examples

### Register User
```
POST /api/auth/register
Content-Type: application/json

{
  "name": "John Doe",
  "email": "john@example.com",
  "password": "123456",
  "phone": "1234567890"
}
```

### Login User
```
POST /api/auth/login
Content-Type: application/json

{
  "email": "john@example.com",
  "password": "123456"
}
```

### Get Current User
```
GET /api/auth/me
Authorization: Bearer YOUR_JWT_TOKEN
```
