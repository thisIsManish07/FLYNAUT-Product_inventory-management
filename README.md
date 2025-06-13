# FLYNAUT-Product_inventory-management
A clean and well-structured Spring Boot REST API to manage products and inventory with full CRUD operations, input validation, and custom exceptions — built without Lombok.spring-boot · rest-api · inventory-management · product-management · java · backend · dto · exception-handling
## 🚀 Tech Stack
- **Java 17**
- **Spring Boot**
- **Spring Web**
- **Spring Data JPA**
- **MySQL**
- **DTOs**
- **Validation** (`javax.validation`)
- **Manual Getter/Setter, Constructors**
- **Exception Handling**
- **Postman** (for API testing)
# 🛒 Product & Inventory Management API
This is a Spring Boot RESTful API developed to manage **Products** and their **Inventory** as part of the **MilkFirst backend ecosystem**. The application is designed with clean code principles using **DTOs**, **validation**, and **custom exception handling** — implemented **without Lombok**.
# Project Structure 📂
src/
├── main/
│   ├── java/
│   │   └── com/yourpackage/
│   │       ├── config/       # Configuration classes
│   │       ├── controller/   # REST controllers
│   │       ├── model/        # Entity classes
│   │       ├── repository/   # JPA repositories
│   │       ├── service/      # Business logic
│   │       └── ProductAndInventoryManagementApplication.java
│   └── resources/
│       ├── application.properties # Config file
│       └── static/           # Static files (if any)
## ✅ Features
- 🧾 **CRUD APIs** for both Product and Inventory
- 🧩 **DTO-based request/response**
- ✅ **Input validation** using `@NotNull`, `@Size`, `@Min`, etc.
- 🚫 Custom exception handling:
  - `ProductNotFoundException`
  - `InventoryNotFoundException`
  - `ProductDeletionException`
- 🔒 **No Lombok**: Getters, setters, and constructors are written manually
- 🧪 Tested with **Postman**
## Open in IntelliJ IDEA or any Maven-compatible IDE
Configure H2 database in application.properties
spring.datasource.url=jdbc:h2:mem:ProductInventoryDB
spring.datasource.username=sa
spring.datasource.password=pring.h2.console.enabled=true
spring.h2.console.path=/h2-console

spring.jpa.database-platform=org.hibernate.dialect.H2Dialect
spring.jpa.hibernate.ddl-auto=update


# H2 Console
spring.h2.console.enabled=true
spring.h2.console.path=/h2-console

# JPA
spring.jpa.database-platform=org.hibernate.dialect.H2Dialect
spring.jpa.hibernate.ddl-auto=update
Run the application
Run ProductAndInventoryManagementApplication.java as a Java application

## Test with Postman
Base URL: http://localhost:8080

# 🔗 POSTMAN API ENDPOINTS
**✅ Product APIs**
HTTP Method	Endpoint	Description
POST	/products	Add a new product
GET	/products	Get all products
GET	/products/{id}	Get product by ID
PUT	/products/{id}	Update product by ID
DELETE	/products/{id}	Delete product by ID

**📦 Inventory APIs**
HTTP Method	Endpoint	Description
POST	/inventory	Add a new inventory item
GET	/inventory	Get all inventory items
GET	/inventory/{id}	Get inventory item by ID
PUT	/inventory/{id}	Update inventory item by ID
DELETE	/inventory/{id}	Delete inventory item by ID
