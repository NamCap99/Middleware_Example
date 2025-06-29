# 🧩 Middleware_Example

This project demonstrates how to build custom middleware in **ASP.NET Core** to handle basic login logic without using controllers or Razor pages.

## 🔧 Features

- Custom login middleware handling POST `/` requests
- Returns appropriate HTTP status codes and messages
- Validates email and password (hardcoded for demonstration)
- Handles:
  - ✅ Valid credentials (returns `200 OK`)
  - ❌ Invalid credentials (returns `400 Bad Request`)
  - ❌ Missing input (returns `400 Bad Request` with detailed messages)
  - ✅ GET `/` request returns welcome message

## 📂 Project Structure

MiddlewareExample/
├── CustomMiddleware/
│ └── LoginMiddleware.cs
├── Program.cs
└── README.md


## 📮 Usage

### ✅ POST Request to `/`

Send a `POST` request with form data:

**URL:** `http://localhost:5000/`  
**Body (x-www-form-urlencoded):**
email=admin@example.com
password=admin1234


**Response:**
```http
200 OK
Login successful

✅ GET / Request
Accessing http://localhost:5000/ with a GET request returns a welcome message:

http
Copy
Edit
200 OK
Welcome! Please use POST to log in

🧠 Learning Purpose
This project is ideal for understanding:

The middleware pipeline in ASP.NET Core

How to intercept HTTP requests without controllers

Input validation and status code handling

🛠️ Tech Stack
.NET 8

ASP.NET Core

Custom Middleware

Minimal API

👨‍💻 Author
Nam Cap (@NamCap99)
