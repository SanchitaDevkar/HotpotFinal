# Hotpot
Spring Backend Project 

Presentation and Output Document link : https://drive.google.com/drive/folders/1eaEwXzZmfYZP3aEgQLXmJq1oOBZNv5wI?usp=sharing
Vedio Explanation Link: 


HotBite V2 is a comprehensive multi-role food ordering platform built using Spring Boot and MySQL, designed to streamline food ordering and management for Users, Restaurants, and Admins.  
The application supports menu browsing, order placement, cart management, and real-time order tracking.

## 📌 Features

### 👤 User
- 🔐 Register and Login with **JWT-based authentication**
- 🍽️ Browse categorized menu *(Breakfast, Lunch, Dinner, Pizza, Arabian, etc.)*
- 🔎 Search and filter by **category, veg/non-veg, price**
- 📋 View detailed dish info *(ingredients, cooking time, nutrition)*
- 🛒 Add/remove/update items in cart
- 💳 Place orders with **address and payment details**
- 📧 Receive **email notifications** (order confirmation, delivery status)
- 🧾 View order history

---

### 🍴Restaurant
- 🔐 Secure login
- 🍲 Add/update/delete dishes with category, availability, dietary info, etc.
- 📦 View placed orders with **live status**
- 🔄 Update order status *(Processing, Out for Delivery, Delivered)*
- 📊 View **menu performance** and order history

---

### 🛠️ Admin
- 🔐 Secure login with **role-based access**
- 🧑‍🍳 Manage restaurants *(add/delete)*
- 👥 Manage users *(view/delete)*
- 🧾 Modify menu items, prices, and categories globally

---

## 🛠️ Tech Stack

| Layer             | Technology                               |
|-------------------|------------------------------------------|
| **Backend**       | Java, Spring Boot, Spring Security       |
| **Authentication**| JWT (JSON Web Token)                     |
| **Database**      | MySQL with Spring Data JPA (Hibernate)   |
| **API Docs**      | Swagger (Springdoc OpenAPI)              |
| **Frontend**      | Angular / React (your choice)            |
| **Build Tool**    | Maven                                    |

---

## 🔐 Authentication & Security

- Role-based login system (**USER**, **RESTAURANT**, **ADMIN**)
- JWT tokens for **secure session handling**
- Passwords encrypted using **BCrypt**
- Secure REST endpoints with **token-based access control**

---

## 🔗 REST API Endpoints (Sample)

| **Endpoint**                | **Method** | **Role**      | **Description**                       |
|----------------------------|------------|---------------|--------------------------------------- |
| `/auth/register`           | POST       | All           | Register as user or restaurant         |
| `/auth/login`              | POST       | All           | Login and receive JWT token            |
| `/menus`                   | GET        | User          | Browse menu items                      |
| `/cart`                    | GET/POST/PUT/DELETE | User | Manage cart                            |
| `/orders/checkout`         | POST       | User          | Place an order                         |
| `/restaurant/menus`        | CRUD       | Restaurant    | Manage own menu                        |
| `/admin/users`             | GET/DELETE | Admin         | Manage user accounts                   |
| `/admin/restaurants`       | CRUD       | Admin         | Manage restaurants                     |

> 🔗 Swagger UI: [http://localhost:8080/swagger-ui/index.html](http://localhost:8080/swagger-ui/index.html)

---

## 📁 Project Structure

```bash
src/
 ├── main/
 │   ├── java/com/hotbytev2
 │   │   ├── config/         # Security and JWT configuration
 │   │   ├── controller/     # REST controllers (User, Admin, Restaurant)
 │   │   ├── dto/            # Request/Response DTOs
 │   │   ├── model/          # JPA Entities
 │   │   ├── repository/     # JPA Repositories
 │   │   ├── service/        # Business Logic
 │   │   └── util/           # Helper classes (e.g., email, JWT)
 │   └── resources/
 │       ├── application.properties
 │       └── schema.sql / data.sql (optional)
 └── test/
     └── Unit & integration tests
📦 Getting Started
🔧 Prerequisites
☕ Java 17+

🧰 Maven

🐬 MySQL

🚀 Run the Backend

git clone https://github.com/your-username/hotbyte-v2.git
cd hotbyte-v2
mvn spring-boot:run

💾 Configure Database in application.properties


spring.datasource.url=jdbc:mysql://localhost:3306/hotbytev2
spring.datasource.username=root
spring.datasource.password=Satara@123

spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true

jwt.secret=your_base64_encoded_secret


👩‍💻 Author
Sanchita Devkar
📧 Email: sanchita.devkar21@pccoepune.org







