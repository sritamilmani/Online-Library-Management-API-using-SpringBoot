# Online Library Management API using Spring Boot

## Overview
The **Online Library Management API** is a RESTful web service built using Spring Boot that allows users to manage a digital library. This system enables users to perform operations like adding, updating, deleting, borrowing, and returning books. It uses Spring Boot for backend logic, JPA for database interactions, and MySQL as the database.

## Features
- **Book Management**: Add, update, view, and delete books.
- **User Management**: Register and manage users.
- **Borrow & Return Books**: Users can borrow available books and return them after use.
- **Database Integration**: Uses MySQL with Spring Data JPA.
- **RESTful API**: Provides endpoints to interact with the system using HTTP requests.

## Technologies Used
- **Java 17+**
- **Spring Boot**
- **Spring Data JPA**
- **MySQL**
- **Hibernate**
- **Postman (for API testing)**
- **IntelliJ IDEA** (for development)
- **GitHub** (for version control)

## Installation & Setup
### Prerequisites
Ensure you have the following installed:
- Java 17+
- MySQL Database
- IntelliJ IDEA or any Java IDE
- Postman (for testing APIs)
- Git (for version control)

### Clone the Repository
```bash
git clone https://github.com/sritamilmani/Online-Library-Management-API-using-SpringBoot.git
cd Online-Library-Management-API-using-SpringBoot
```

### Configure Database
Update **`application.properties`** in **`src/main/resources/`**:
```properties
spring.datasource.url=jdbc:mysql://localhost:3306/banking_app
spring.datasource.username=root
spring.datasource.password=yourpassword
spring.jpa.hibernate.ddl-auto=update
```

### Build and Run the Application
```bash
mvn clean install
mvn spring-boot:run
```
The API will start at **http://localhost:8080**

## API Endpoints

### Book Management
| Method | Endpoint            | Description               |
|--------|---------------------|---------------------------|
| GET    | `/api/books`        | Get all books            |
| GET    | `/api/books/{id}`   | Get book by ID           |
| POST   | `/api/books`        | Add a new book           |
| PUT    | `/api/books/{id}`   | Update book details      |
| DELETE | `/api/books/{id}`   | Delete a book            |

### Borrow & Return Books
| Method | Endpoint                              | Description            |
|--------|--------------------------------------|------------------------|
| POST   | `/api/books/{bookId}/borrow/{userId}` | Borrow a book         |
| POST   | `/api/books/{bookId}/return`         | Return a borrowed book |

## Testing with Postman
- Use Postman to send HTTP requests to the API.
- Test `GET`, `POST`, `PUT`, and `DELETE` requests to verify functionality.



