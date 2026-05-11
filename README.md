# To-Do List Application (Spring Boot)

A production-ready RESTful web service built with the **Java Spring Boot** stack. This project serves as a foundation for learning CRUD operations, JPA persistence, and REST API design patterns.

## 🚀 Features
- **Full CRUD Support:** Create, Read, Update, and Delete tasks.
- **Status Management:** Toggle tasks between 'Pending' and 'Completed'.
- **Validation:** Ensures tasks are not empty before saving.
- **H2 Console Access:** View your database tables in real-time via a web browser.
- **Auto-Documentation:** Built with industry-standard naming conventions.

## 🛠️ Tech Stack
- **Language:** Java 17+
- **Framework:** Spring Boot 3.x
- **Persistence:** Spring Data JPA / Hibernate
- **Database:** H2 (In-memory for development)
- **Build Tool:** Maven
- **Boilerplate:** Lombok

## 📋 Prerequisites
- **JDK 17** or higher
- **Maven 3.6+**
- **IDE** (IntelliJ IDEA recommended)

## ⚙️ Installation & Setup
1. **Clone the repository:**
   ```bash
   git clone https://github.com
   cd todo-list-springboot
   ```

2. **Configure Database (Optional):**
   By default, it uses an H2 in-memory database. To view it, start the app and go to:
   `http://localhost:8080/h2-console`
   - **JDBC URL:** `jdbc:h2:mem:testdb`
   - **User:** `sa`
   - **Password:** (leave blank)

3. **Run the Application:**
   ```bash
   mvn spring-boot:run
   ```
   The application will be available at `http://localhost:8080`.

## 🛣️ API Documentation

### Base URL: `/api/todos`


| Method | Endpoint | Description | Sample Request Body |
| :--- | :--- | :--- | :--- |
| **GET** | `/` | Get all tasks | N/A |
| **POST** | `/` | Create a task | `{"task": "Study JPA", "completed": false}` |
| **GET** | `/{id}` | Get task by ID | N/A |
| **PUT** | `/{id}` | Update task | `{"task": "Study JPA", "completed": true}` |
| **DELETE**| `/{id}` | Delete task | N/A |

## 🧪 Testing with cURL
You can test the API directly from your terminal:

**Create a task:**
```bash
curl -X POST http://localhost:8080/api/todos -H "Content-Type: application/json" -d '{"task": "Finish Readme", "completed": false}'
```

**Get all tasks:**
```bash
curl http://localhost:8080/api/todos
```

## 📝 License
Distributed under the MIT License. See `LICENSE` for more information.
