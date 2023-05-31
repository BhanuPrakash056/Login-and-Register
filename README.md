# Login-and-Register

This is a backend implementation for a login and signup REST API with security/web tokens using an H2 database.

# Technologies Used
Java
Spring Boot
Spring Data JPA
H2 Database
Spring Security
JSON Web Tokens (JWT)
# Prerequisites
Make sure you have the following prerequisites installed:

Java
Maven
Getting Started
Clone the repository:
bash
git clone https://github.com/your-username/login-api-backend.git
Build the project using Maven:
bash
cd login-api-backend
mvn clean install
Run the application:
bash
mvn spring-boot:run
The backend server will start running at http://localhost:8080.

# Database
The application uses an H2 in-memory database, which is automatically created and populated with sample data when the application starts.

# Endpoints
# Signup
URL: /auth/signup

Method: POST



'''json Request Body:
{
  "username": "john_doe",
  "password": "password123"
}
Response:

'''json Copy code

{
  "message": "User created successfully"
}

# Login
URL: /auth/login

Method: POST

# Request Body:

'''json
{
  "username": "john_doe",
  "password": "password123"
}
Response:

'''json
{
  "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9..."
}
The login endpoint returns a JWT token that can be used for authentication in subsequent API requests.

Configuration
The application can be configured through the application.properties file, located in the src/main/resources directory. You can modify the database connection settings, JWT secret, and other properties in this file.

