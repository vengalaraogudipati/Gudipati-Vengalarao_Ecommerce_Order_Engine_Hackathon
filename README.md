# Gudipati-Vengalarao_Ecommerce_Order_Engine_Hackathon
# 🛒 Ecommerce Order Engine

## 📌 Project Overview

This project is a Spring Boot-based backend system that simulates an e-commerce order engine.
It handles product management, cart operations, order processing, payment handling, and system reliability features like fraud detection and failure recovery.

---

## 🚀 Features Implemented

* Product Management (Add/View products)
* Cart System (Add items and place orders)
* Order Processing Engine
* Payment Simulation
* Inventory Management (Stock reservation & rollback)
* Idempotency Handling (prevents duplicate orders)
* Fraud Detection (high-value & rapid orders)
* Discount & Coupon System
* Failure Injection (simulate payment/inventory failures)
* AOP Logging for auditing

---

## 🧠 Design Approach

* Layered Architecture: Controller → Service → Repository
* Used Spring Boot for dependency injection and modular design
* JPA with MySQL for persistence
* Services are loosely coupled to simulate microservice behavior
* Implemented rollback mechanism for consistency during failures
* Used AOP for centralized logging

---

## ⚙️ Assumptions

* Cart is stored in memory (not persisted)
* Product prices are static for simplicity
* No authentication or user management
* Single-user simulation (can be extended)
* Failure scenarios are manually triggered via API

---

## ▶️ How to Run the Project

### 1. Clone Repository

```bash
https://github.com/vengalaraogudipati/Gudipati-Vengalarao_Ecommerce_Order_Engine_Hackathon
```

### 2. Configure MySQL

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/ecommerce
spring.datasource.username=root
spring.datasource.password=yourpassword
spring.jpa.hibernate.ddl-auto=update
```

### 3. Run Application

```bash
mvn spring-boot:run
```

### 4. Test APIs

Use Postman or browser:

* POST /products
* GET /products
* POST /orders/place
* GET /orders
