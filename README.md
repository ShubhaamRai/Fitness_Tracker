# 🏋️ Fitness Tracker – Spring Boot Backend

## 📌 Project Overview

**Fitness Tracker** is a production-ready RESTful backend API built using **Spring Boot 4** and **Java 21**.  
It allows users to track workouts, monitor calorie burn, and receive fitness recommendations.

The application is secured using **Spring Security with JWT (Access + Refresh Tokens)** and follows a clean **Controller → Service → Repository** layered architecture.


---
🔗 Live Backend  Swagger URL
https://fitness-tracker-js7g.onrender.com/swagger-ui/index.html
## 🚀 Tech Stack

- Java 21
- Spring Boot 4
- Spring Security
- JWT Authentication (Access & Refresh Tokens)
- MySQL 
- Maven
- Docker
- BCrypt Password Encryption
- Global Exception Handling
- DTO Pattern
- Role-Based Authorization

---

## 🏗 Architecture

The project follows a clean layered architecture:

Controller → Service → Repository → Database

### ✔ Design Practices Implemented

- DTO-based request and response handling
- Global exception handling
- Validation using `@Valid`
- Role-based access control (Admin & User)
- BCrypt password encryption
- Environment-based configuration
- Docker container deployment
- Refresh token implementation

---

## 🔐 Authentication & Security

Security is implemented using:

- Spring Security
- JWT Access Token
- JWT Refresh Token
- Role-based authorization
- BCrypt password hashing

### 🔑 Authentication Endpoints
POST /api/auth/register
POST /api/auth/login

---

## 📊 Features

### 👤 User Features

- User Registration & Login
- JWT Authentication
- Add Workout Activity
- Track Calories
- View All Activities
- View Activities by User
- View Specific Activity
- Generate Workout Recommendations

### 👑 Admin Features

- Role-based access control
- Manage user activities

---

## 📦 API Endpoints

### 🔹 Authentication
POST /api/auth/register
POST /api/auth/login

### 🔹 Activities

GET /api/activities
POST /api/activities
GET /api/activities/user/{userId}
GET /api/activities/activity/{activityId}

### 🔹 Recommendation
POST /api/recommendation/generate

---

## 🗄 Database

- PostgreSQL hosted on Neon Cloud
- Secure cloud connection
- Environment variable configuration

### 🌱 Entities

- User
- UserRole
- Activity
- ActivityType
- Recommendation

---

## ⚙️ Environment Variables

The application uses environment-based configuration:

---

## 🗄 Database

- PostgreSQL hosted on Neon Cloud
- Secure cloud connection
- Environment variable configuration

### 🌱 Entities

- User
- UserRole
- Activity
- ActivityType
- Recommendation

---

## ⚙️ Environment Variables

The application uses environment-based configuration:

DB_URL=
DB_USER=
DB_PASS=

These variables are configured in the Docker deployment environment on Render.

---

## 🐳 Docker Deployment

The application is containerized using Docker and deployed to Render using a Docker image.

### 🔧 Build Docker Image

```bash
docker build -t fitness-tracker .
▶ Run Container Locally
docker run -p 8080:8080 \
-e DB_URL=your_database_url \
-e DB_USER=your_database_user \
-e DB_PASS=your_database_password \
fitness-tracker
☁ Deployment

Dockerized backend

Deployed on Render using container deployment

Connected to Neon PostgreSQL cloud database

🔗 Live API:
https://fitness-app-ak5n.onrender.com
🛡 Error Handling

Centralized Global Exception Handler

Custom error responses

Validation error handling with field-specific messages
📁 Project Structure
fitness-tracker/
│
├── src/
│   ├── main/
│   │   ├── java/com/project/fitness/
│   │   │   ├── controller/        # REST Controllers
│   │   │   ├── dto/               # Request & Response DTOs
│   │   │   ├── exceptions/        # Global Exception Handling
│   │   │   ├── model/             # JPA Entities
│   │   │   ├── repository/        # Spring Data JPA Repositories
│   │   │   ├── security/          # JWT & Security Configuration
│   │   │   ├── service/           # Business Logic Layer
│   │   │   └── FitnessApplication.java
│   │   │
│   │   └── resources/
│   │       ├── application.properties
│   │       ├── static/
│   │       └── templates/
│   │
│   └── test/
│
├── Dockerfile
├── pom.xml
├── mvnw
├── mvnw.cmd
└── .gitignore
