# Student REST API — Spring Boot

A REST API built with Java and Spring Boot that performs full **CRUD operations** (Create, Read, Update, Delete) on student data using an in-memory H2 database.

---

## Tech Stack

| Technology | Purpose |
|---|---|
| Java 21 | Programming language |
| Spring Boot 3.4.5 | Backend framework |
| Spring Data JPA | Database interaction via ORM |
| Hibernate | JPA implementation |
| H2 Database | In-memory database |
| Gradle | Build tool |
| Tomcat (embedded) | Web server |

---

## Project Structure

```
SpringBootApps/
├── build.gradle
└── src/main/java/com/example/SpringBootApps/
    ├── SpringBootAppsApplication.java   ← Entry point
    ├── model/
    │   └── Student.java                 ← Entity / data model
    ├── repository/
    │   └── StudentRepository.java       ← Database operations
    └── controller/
        └── StudentController.java       ← REST endpoints
```

---

## API Endpoints

| Method | Endpoint | Description |
|---|---|---|
| GET | `/api/students` | Get all students |
| GET | `/api/students/{id}` | Get student by ID |
| POST | `/api/students` | Create a new student |
| PUT | `/api/students/{id}` | Update an existing student |
| DELETE | `/api/students/{id}` | Delete a student |

---

## Sample Request & Response

**POST** `/api/students`

Request body:
```json
{
  "name": "Shanya Jaidwal",
  "email": "shanya@example.com",
  "course": "Computer Science"
}
```

Response:
```json
{
  "id": 1,
  "name": "Shanya Jaidwal",
  "email": "shanya@example.com",
  "course": "Computer Science"
}
```

---

## How to Run Locally

**Prerequisites:**
- Java 21 installed
- VS Code with Extension Pack for Java

**Steps:**

1. Clone the repository
```bash
git clone https://github.com/24repos/REST.git
```

2. Open the project folder in VS Code

3. Run the app
```bash
./gradlew bootRun
```

4. Server starts at `http://localhost:8080`

---

## Testing the API

Use **Thunder Client** (VS Code extension) or **Postman** to test the endpoints.

You can also view the database at:
```
http://localhost:8080/h2-console
```
JDBC URL: `jdbc:h2:mem:studentdb`

---

## What I Learned

- Building REST APIs using Spring Boot
- Structuring a project using MVC architecture (Model, Repository, Controller)
- Using Spring Data JPA to interact with a database without writing SQL
- Dependency Injection with `@Autowired`
- Testing APIs using Thunder Client
- Version control with Git and GitHub

