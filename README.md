# ✅ To-Do List Application

A production-ready RESTful API built using **Java Spring Boot** that demonstrates modern backend development practices including CRUD operations, data persistence with JPA/Hibernate, validation, and RESTful service design.

This project is ideal for learning and showcasing Spring Boot fundamentals, database integration, and API development skills.

---

## 🚀 Features

* ✅ Create, Read, Update, and Delete (CRUD) tasks
* ✅ Mark tasks as **Pending** or **Completed**
* ✅ Input validation to prevent empty task creation
* ✅ RESTful API architecture following industry standards
* ✅ H2 in-memory database for rapid development and testing
* ✅ Spring Data JPA integration with Hibernate ORM
* ✅ Clean layered architecture (Controller → Service → Repository)
* ✅ Easy-to-use H2 Console for database inspection

---

## 🛠️ Tech Stack

| Technology      | Purpose                     |
| --------------- | --------------------------- |
| Java 17         | Programming Language        |
| Spring Boot 3.x | Backend Framework           |
| Spring Data JPA | Data Access Layer           |
| Hibernate       | ORM Framework               |
| H2 Database     | In-Memory Database          |
| Maven           | Dependency Management       |
| Lombok          | Boilerplate Code Reduction  |
| REST API        | Client-Server Communication |

---

## 📂 Project Structure

```text
src
├── main
│   ├── java
│   │   └── com.example.todo
│   │       ├── controller
│   │       ├── service
│   │       ├── repository
│   │       ├── entity
│   │       └── TodoApplication
│   └── resources
│       └── application.properties
└── test
```

---

## 📋 Prerequisites

Before running the application, ensure you have:

* JDK 17 or higher
* Maven 3.6+
* IntelliJ IDEA / Eclipse / VS Code

---

## ⚙️ Installation & Setup

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/todo-list-springboot.git
cd todo-list-springboot
```

### 2. Build the Project

```bash
mvn clean install
```

### 3. Run the Application

```bash
mvn spring-boot:run
```

The application will start on:

```text
http://localhost:8080
```

---

## 🗄️ H2 Database Console

Access the H2 Console:

```text
http://localhost:8080/h2-console
```

Use the following credentials:

| Property | Value              |
| -------- | ------------------ |
| JDBC URL | jdbc:h2:mem:testdb |
| Username | sa                 |
| Password | (leave blank)      |

---

## 📡 API Endpoints

### Base URL

```text
/api/todos
```

| Method | Endpoint        | Description             |
| ------ | --------------- | ----------------------- |
| GET    | /api/todos      | Get all tasks           |
| GET    | /api/todos/{id} | Get task by ID          |
| POST   | /api/todos      | Create a new task       |
| PUT    | /api/todos/{id} | Update an existing task |
| DELETE | /api/todos/{id} | Delete a task           |

---

## 📥 Sample Request & Response

### Create Task

**POST** `/api/todos`

Request Body:

```json
{
  "task": "Study Spring Boot",
  "completed": false
}
```

Response:

```json
{
  "id": 1,
  "task": "Study Spring Boot",
  "completed": false
}
```

---

### Update Task

**PUT** `/api/todos/1`

```json
{
  "task": "Study Spring Boot and JPA",
  "completed": true
}
```

---

## 🧪 Testing with cURL

### Create Task

```bash
curl -X POST http://localhost:8080/api/todos \
-H "Content-Type: application/json" \
-d '{"task":"Finish README","completed":false}'
```

### Get All Tasks

```bash
curl http://localhost:8080/api/todos
```

### Delete Task

```bash
curl -X DELETE http://localhost:8080/api/todos/1
```

---

## 🎯 Learning Outcomes

This project demonstrates:

* REST API Development
* Spring Boot Fundamentals
* Spring Data JPA & Hibernate
* Database Integration
* Validation Handling
* Maven Project Management
* Clean Code Practices
* Layered Architecture

---

## 🔮 Future Enhancements

* User Authentication & Authorization (Spring Security + JWT)
* MySQL/PostgreSQL Integration
* Pagination & Sorting
* Swagger/OpenAPI Documentation
* Docker Containerization
* Unit & Integration Testing
* Frontend Integration (React/Angular)

---

## 👨‍💻 Author

**Navi**

Java Full Stack Developer | Spring Boot Enthusiast

---

## 📜 License

This project is licensed under the MIT License.
