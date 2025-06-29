# Middleware_Example

A minimal ASP.NET Core application demonstrating how to build and use custom middleware to handle login logic. This project is ideal for learning how middleware can intercept HTTP requests and process them without relying on MVC controllers or Razor pages.

---

## 📌 Overview

This application uses a custom `LoginMiddleware` class to handle `POST` requests to `/`. It checks for hardcoded credentials (`admin@example.com` / `admin1234`) and returns appropriate HTTP status codes and responses.

It also returns helpful validation messages when required inputs are missing, and handles `GET` requests with a friendly welcome message.

---

## 🚀 Getting Started

### Prerequisites

- [.NET 8 SDK](https://dotnet.microsoft.com/en-us/download)
- Any REST client (e.g. [Postman](https://www.postman.com/), `curl`, or browser)

### Run the App

```bash
git clone https://github.com/NamCap99/Middleware_Example.git
cd Middleware_Example
dotnet run

app.Urls.Add("http://localhost:5000");

📮 Usage Examples
✅ Valid Login
Request:
email=admin@example.com&password=admin1234
Response:
200 OK
Login successful

❌ Invalid Credentials
Request:
email=wrong@example.com&password=wrongpass
Response:
400 Bad Request
Invalid credentials

❌ Missing Body
Request:
(no body)
Response:
400 Bad Request
Invalid input for 'email'
Invalid input for 'password'

✅ GET Request
Request:
GET /

Response:
http
Copy
Edit
200 OK
Welcome! Please use POST to log in

📁 Folder Structure
MiddlewareExample/
├── CustomMiddleware/
│   └── LoginMiddleware.cs
├── Program.cs
└── README.md


---

### ✅ This README includes:
- A **professional intro**
- `git clone` & `dotnet run` setup
- Full usage examples
- Real-world structure and tone
- License section (you can create a `LICENSE` file if needed)

Let me know if you want to:
- Add badges (build passing, .NET version, etc.)
- Include screenshots
- Add CI/CD setup or Docker support

I'm happy to help make it even more like a real-world open-source project.
