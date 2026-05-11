To-Do List Application (Spring Boot)A RESTful web service built with Java and Spring Boot that allows users to manage their daily tasks. This project demonstrates the implementation of a standard 3-tier architecture (Controller, Service, Repository).🚀 FeaturesCreate Tasks: Add new items to your list.Read Tasks: View all tasks or search for a specific one by ID.Update Tasks: Mark tasks as completed or edit the description.Delete Tasks: Remove tasks once they are no longer needed.Persistence: Data is stored in an H2/MySQL database (choose based on your config).🛠️ Tech StackBackend: Java 17/21, Spring Boot 3.xData Access: Spring Data JPA, HibernateDatabase: H2 (In-Memory) / MySQLBuild Tool: MavenUtilities: Lombok (to reduce boilerplate)📋 PrerequisitesBefore running this project, ensure you have:JDK 17 or higher installed.Maven installed.An IDE (IntelliJ IDEA, Eclipse, or VS Code).⚙️ Installation & SetupClone the repository:bashgit clone https://github.com
cd todo-list-springboot
Use code with caution.Build the project:bashmvn clean install
Use code with caution.Run the application:bashmvn spring-boot:run
Use code with caution.The server will start at http://localhost:8080.🛣️ API EndpointsMethodEndpointDescriptionGET/api/todosFetch all tasksPOST/api/todosCreate a new taskGET/api/todos/{id}Get task by IDPUT/api/todos/{id}Update an existing taskDELETE/api/todos/{id}Delete a task🧪 Testing with PostmanOpen Postman.Set the method to POST.Use the URL: http://localhost:8080/api/todos.In the Body tab, select raw and JSON, then paste:json{
  "task": "Learn Spring Boot Security",
  "completed": false
}
Use code with caution.
