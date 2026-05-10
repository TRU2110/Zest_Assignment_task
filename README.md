# Student Management System API

A secure ASP.NET Core Web API project for managing student records using CRUD operations, JWT Authentication, SQL Server, Swagger, Serilog Logging, and Layered Architecture.


# Features
* Get All Students
* Add Student
* Update Student
* Delete Student
* JWT Authentication
* Global Exception Handling Middleware
* Serilog Logging
* Swagger API Documentation
* Layered Architecture


# Technologies Used
* ASP.NET Core Web API
* Entity Framework Core
* SQL Server
* JWT Authentication
* Swagger
* Serilog



# Project Structure
```text

StudentAPI
│
|-- Controllers
|-- Services
|-- Repositories
|-- Models
|-- Data
|-- Middleware
|-- appsettings.json
|-- Program.cs
```

# Database Setup

1. Open SQL Server Management Studio (SSMS)
2. Create a database named:

```sql
CREATE DATABASE StudentDB;
```
3. Update connection string in `appsettings.json`
4. Run the project


# Project Setup Steps

## 1. Clone Repository

```bash
git clone https://github.com/TRU2110/Zest_Assignment_task.git
```


## 2. Open Project

Open project folder in Visual Studio or VS Code.


## 3. Install Required Packages

```bash
dotnet add package Microsoft.EntityFrameworkCore.SqlServer

dotnet add package Microsoft.EntityFrameworkCore.Tools

dotnet add package Microsoft.AspNetCore.Authentication.JwtBearer

dotnet add package Serilog.AspNetCore
```


## 4. Configure Connection String
Update `appsettings.json`:

```json
"ConnectionStrings": {
  "DefaultConnection": "Server=YOUR_SERVER_NAME;Database=StudentDB;Trusted_Connection=True;TrustServerCertificate=True;"
}
```


## 5. Run Project
```bash
dotnet run
```

# JWT Authentication

1. Open Swagger:
   http://localhost:5017/swagger/index.html
2. Execute the login API:
```text
POST /api/auth/login
```
3. Copy the generated JWT token
4. Click the "Authorize" button in Swagger
5. Enter token in below format:
```text
Bearer YOUR_TOKEN
```
6. Now you can access secured Student APIs


# API Endpoints

The following APIs are available in this project:

- `POST    /api/auth/login` → Generate JWT token
- `GET     /api/students` → Retrieve all student records
- `POST    /api/students` → Add a new student
- `PUT     /api/students/{id}` → Update student details
- `DELETE  /api/students/{id}` → Delete a student record
  

# Logging

Serilog is used for logging application errors and activities.


# Exception Handling

Global Exception Middleware is implemented for centralized error handling.



