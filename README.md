# Alcodist Hub Backend

A high-performance Go backend built with **Gin** and **MongoDB Atlas**, powering a personal blogging platform.

![Language](https://img.shields.io/badge/Language-Go_1.22+-00ADD8?style=flat-square&logo=go)
![Framework](https://img.shields.io/badge/Framework-Gin-000000?style=flat-square&logo=gin)
![Database](https://img.shields.io/badge/Database-MongoDB-47A248?style=flat-square&logo=mongodb)
![CI/CD](https://img.shields.io/badge/CI%2FCD-GitHub_Actions-2088FF?style=flat-square&logo=github-actions)

---

## 🏗️ Architecture & Project Structure

The project follows a clean, modular Go layout, decoupling transport handlers, business logic, domain models, and database access:

```text
.
├── api/              # REST handlers, middleware, & router setup
├── cmd/              # Application entry points (main.go)
├── configs/          # Configuration loaders
├── internal/         # Private application and domain logic
│   ├── database/     # DB connections (MongoDB)
│   ├── models/       # Domain data models (Author, Blog, etc.)
│   └── repository/   # Data access layer & interfaces
├── migrations/       # Database schema evolution scripts
├── swagger/          # OpenAPI/Swagger documentation specs
├── Dockerfile
├── docker-compose.yml
└── go.mod
```

---

## 📋 Prerequisites

Ensure you have the following installed on your machine:

- [Go (v1.22 or higher)](https://golang.org/)
- [Air](https://github.com/cosmtrek/air) (Optional, for hot-reloading)
- [Docker & Docker Compose](https://www.docker.com/) (Optional, for containerized execution)

---

## ⚙️ Configuration (.env)

1. Copy the example environment file:
   ```bash
   cp .env.example .env
   ```
2. Populate the required environment variables in your `.env` file.

---

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/Victormuthomi/alcodist-hub-backend.git
cd alcodist-hub-backend
```

### 2. Install Dependencies

```bash
go mod download
```

### 3. Run the Application

- **With Hot-Reload (Development):**
  ```bash
  air
  ```
- **Directly via Go:**
  ```bash
  go run cmd/main.go
  ```
- **Via Docker Compose:**
  ```bash
  docker-compose up --build
  ```

---

## 🧪 Testing

The repository includes handler unit and integration tests under the `api/handler` package to verify route behaviors and data handling.

Execute the test suite using:

```bash
# Run API handler tests verbosely
go test -v ./api/handler

```

---

## 🔄 CI/CD Pipeline

This project leverages **GitHub Actions** to automate workflows:

- **Automated Testing:** Every pull request and push to main triggers automated test execution against handlers to catch regressions early.
- **Build Verification:** Ensures compilation stability and code quality before deployment.

---

## 📊 API Documentation

Interactive Swagger documentation is available locally once the server is running:

- **URL:** `http://localhost:8080/swagger/index.html`

---

## 📄 License

© 2026 Alcodist Labs. All rights reserved.
