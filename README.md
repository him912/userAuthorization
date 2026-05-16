# Authentication API

A Node.js authentication system using JWT Bearer Token.

## Features

- User Registration
- User Login
- JWT Authentication
- Protected Routes

## Tech Stack

- Node.js
- Express.js
- MongoDB
- Mongoose
- JWT

📬 Postman Documentation

🌐 API Base URL

https://userauthorization.onrender.com/

1.Register User

📮 API Endpoints 
/api/auth/register

Request Body

Plain Text

{  "username": "Himanshu",  "email": "himanshu@gmail.com",  "password": "123456"}

Success Response

Plain Text

{ "success": true,  "message": "User registered successfully"}

2.Login User

📮 API Endpoints 
POST
/api/auth/login
Request Body

Plain Text

{ "email": "himanshu@gmail.com",  "password": "123456"}

Success Response

Plain Text

{  "success": true,  "message": "Login successful",  "token": "jwt_token_here"}


3.Profile User

📮 API Endpoints 
GET
/api/auth/profile

Get User Profile
Headers


Plain Text

Authorization: Bearer jwt_token_here

Success Response

Plain Text

{  "success": true,  "data": {    "_id": "6825abc123",    "username": "Himanshu",    "email": "himanshu@gmail.com"  }}

❌ Error Responses

Invalid Token


Plain Text

{  "success": false,  "message": "Not authorized, token failed"}

No Token

Plain Text

{  "success": false,  "message": "No token provided"}

