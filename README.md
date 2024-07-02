# InShorts-like Platform API

This project implements an API for an InShorts-like platform using Spring Boot, allowing users to register, login, manage shorts (news/articles/posts), and filter them based on various criteria.

## Technologies Used

- **Spring Boot**: Framework for building robust Java applications.
- **Spring Data JPA**: Simplifies data access with Hibernate as the JPA provider.
- **MySQL**: Database to store user information.

## Setup

### Prerequisites

- Java Development Kit (JDK) installed.
- MySQL installed and running locally or accessible.
- IDE (Eclipse, IntelliJ IDEA, etc.) with Spring Boot support.

### Steps to Run

1. **Clone the repository**:

   ```bash
   git clone <repository-url>
Configure MySQL:

Create a MySQL database and update application.properties with your database credentials:

properties
Copy code
spring.datasource.url=jdbc:mysql://localhost:3306/your_database_name
spring.datasource.username=your_username
spring.datasource.password=your_password
Run the Application:

Navigate to the project directory and run the application using Maven:

bash
Copy code
cd inshorts-like-api
./mvnw spring-boot:run
Alternatively, import the project into your IDE and run the main class Application.java.

Access the API:

The API will be available at http://localhost:8080.
API Endpoints
User Management
POST /api/users: Register a new user.

json
Copy code
{
  "username": "example_user",
  "password": "example_password",
  "email": "user@example.com"
}
GET /api/users/{id}: Get user by ID.

PUT /api/users/{id}: Update user details.

json
Copy code
{
  "username": "updated_user",
  "password": "updated_password",
  "email": "updated_email@example.com"
}
DELETE /api/users/{id}: Delete user by ID.
