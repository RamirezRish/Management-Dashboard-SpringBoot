# Management Dashboard - REST API 🎓🤖

A robust backend REST API for a **Student Management Application** designed to facilitate research and continuous learning. By integrating study methodologies and Artificial Intelligence, this application aims to boost productivity, organization, and knowledge retention for students and researchers.

## Technologies Used

- **Backend Framework:** Spring Boot 3.2.x
- **Language:** Java 17
- **Database:** MySQL
- **Security:** Spring Security & JWT (JSON Web Tokens)
- **Frontend Integration:** Ready for consumption by **Angular** client applications.

## Key Features

### 1. AI Assistant Integration (`AssistantController`)

Features an integrated AI assistant to aid students in their research and learning workflows, allowing for smart queries and automated assistance directly within the dashboard.

### 2. Study Methodologies

- **Tasks Management (`TaskController`, `Task` model):** Keep track of assignments, deadlines, and project milestones.
- **Flashcards (`FlashCard` model):** Active recall methodology integration to help students memorize concepts effectively.
- **Headlines / Subjects (`HeadlineController`, `Headline` model):** Organize study materials into topics and subjects for better structural overview.

### 3. Security & User Management (`AuthenticationController`, `UserController`)

- Built-in Role-based access control (`Roles`, `Permission` models).
- Secure authentication using state-of-the-art JWT implementation.
- User profile management.

## Project Structure

```
src/main/java/com/managementDashboard/RestAPI
├── config/           # Application and Security configuration (JWT Token Validation)
├── controller/       # Exposes REST endpoints (Auth, Assistant, Tasks, Headlines, Users)
│   └── dto/          # Data Transfer Objects for inputs and outputs (e.g., AssistantRequest, AuthLoginRequest)
├── enums/            # System enumerations (e.g., RoleEnum)
├── model/            # JPA Entities (User, Task, FlashCard, Headline, Roles, Permission)
├── repository/       # Data Access Layer interfaces extending JpaRepository
├── service/          # Business logic layer (TaskService, AssistantService, JwtUtils)
└── util/             # Utility classes and helpers
```

## Getting Started

### Prerequisites

- JDK 17 or higher
- MySQL Server installed and running
- Maven or Gradle (wrapper included in project)

### Installation & Setup

1. **Clone the repository:**
   Ensure you have the latest version of the code.

2. **Configure Database:**
   Update your `application.properties` or `application.yml` file located in `src/main/resources` with your MySQL credentials:

   ```properties
   spring.datasource.url=jdbc:mysql://localhost:3306/your_database_name
   spring.datasource.username=your_mysql_username
   spring.datasource.password=your_mysql_password
   spring.jpa.hibernate.ddl-auto=update
   ```

3. **Provide API Keys (If applicable):**
   If the AI Assistant requires a third-party key (e.g., OpenAI API Key), ensure it is configured in your environments or properties file.

4. **Run the Application:**
   Using Gradle wrapper:

   ```bash
   ./gradlew bootRun
   ```

5. **API Documentation (Optional):**
   If Swagger/OpenAPI is configured, navigate to `http://localhost:8080/swagger-ui.html` following a successful build to interact with the endpoints.

## API Endpoints Overview

- **`POST /auth/login`**: Authenticate specific user and receive JWT.
- **`POST /auth/register`**: Register a new user.
- **`GET /api/tasks`**: Retrieve all user-specific study tasks.
- **`POST /api/assistant/...`**: Engage with the AI model for research or questions.
- _(More specific endpoints mapping can be visualized in the corresponding controllers)_.

## Contributing

Contributions, issues, and feature requests are welcome! Feel free to check the issues page.

---

_Developed with ❤️ to empower education and student workflows._
