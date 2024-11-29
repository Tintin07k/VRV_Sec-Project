# Full-Stack JWT Authentication Project
This is a project for authentication and authorization using JWT Token


This project demonstrates a full-stack implementation of JWT (JSON Web Token) authentication using a React frontend and a Spring Boot backend. The project is structured into two main folders: UI and API.

Table of Contents

- Project Structure
- High-Level Design
- Getting Started
  - Prerequisites
  - Installation
- Usage
- API Endpoints
- Contributing
- License

Project Structure

The project is organized as follows:

/root
│
├── UI/
│   └── jwt-login/
│       ├── public/
│       ├── src/
│       ├── package.json
│       ├── README.md
│       └── ...
│
├── API/
│   └── jwt-api/
│       ├── src/
│       │   ├── main/
│       │   │   ├── java/
│       │   │   │   └── com/
│       │   │   │       └── authdemo/
│       │   │   │           ...
│       │   │   └── resources/
│       │   │       └── application.properties
│       │   └── test/
│       ├── pom.xml
│       ├── README.md
│       └── ...
│
├── README.md
└── ...

High-Level Design

The high-level design of the project includes the following components:

1. UI (React App):
   - The React app handles user registration, login, and interaction with the backend API.
   - It uses JWT tokens for authentication and authorization.
   - The app is located in the UI/jwt-login/ directory.

2. API (Spring Boot App):
   - The Spring Boot app provides the backend services, including user management, JWT token generation, and validation.
   - It exposes RESTful endpoints for the frontend to interact with.
   - The app is located in the API/jwt-api/ directory.

Getting Started

Prerequisites

- Node.js and npm (for the React app)
- Java Development Kit (JDK) 11 or higher (for the Spring Boot app)
- Maven (for building the Spring Boot app)
- MySQL or any other supported database

Installation

1. Clone the repository:

   git clone https://github.com/your-username/full-stack-jwt-auth.git
   cd full-stack-jwt-auth

2. Set up the UI (React App):

   cd UI/jwt-login
   npm install

3. Set up the API (Spring Boot App):

   cd ../API/jwt-api
   Update the application.properties file with your database configuration:

   mvn clean install

Usage

1. Start the API (Spring Boot App):

   cd API/jwt-api
   mvn spring-boot:run

2. Start the UI (React App):

   cd UI/jwt-login
   npm start

3. Access the application:

   Open your browser and navigate to http://localhost:3000 to view the React app.

API Endpoints

- POST /api/auth/signup: Register a new user.
- POST /api/auth/signin: Login and get JWT token.
- POST /api/auth/signout: Logout after removing JWT token from cookie.
- GET /api/test/all: Public endpoint, accessible without authentication.
- GET /api/test/user: Secured endpoint, accessible with user role.
- GET /api/test/mod: Secured endpoint, accessible with moderator role.
- GET /api/test/admin: Secured endpoint, accessible with admin role.
