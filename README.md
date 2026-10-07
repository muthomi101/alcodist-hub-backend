# Alcodist Hub Backend

A high-performance Go backend built with **Gin** and **MongoDB Atlas**, powering a personal blogging platform.

![Language](https://img.shields.io/badge/Language-Go_1.22+-00ADD8?style=flat-square&logo=go)
![Framework](https://img.shields.io/badge/Framework-Gin-000000?style=flat-square&logo=gin)
![Database](https://img.shields.io/badge/Database-MongoDB-47A248?style=flat-square&logo=mongodb)

---

## 🏗️ Architecture & Project Structure

The project follows the standard Go project layout, cleanly decoupling transport routing, business logic, and database operations using an encapsulated `internal/` structure.

```text
.
├── api/              # RESTful API handlers & router setup
├── cmd/              # Application entry points (main.go)
├── internal/         # Core domain logic, services, and repositories
├── migrations/       # Database initialization & schema scripts
├── .air.toml         # Hot-reload configuration for local development
└── docker-compose.yml
```

---

## 📋 Prerequisites

Ensure you have the following installed on your machine:

- [Go (v1.22 or higher)](https://golang.org/)
- [Air](https://github.com/cosmtrek/air) (Optional, for hot-reloading)
- [Docker & Docker Compose](https://www.docker.com/) (Optional, for containerized execution)

---

## ⚙️ Configuration (.env)

Create a `.env` file in the root directory and configure the following environment variables:

```env
PORT=8080
MONGODB_URI=your_mongodb_atlas_connection_string
JWT_SECRET=your_secret_key
```

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

## 📊 API Documentation

Interactive Swagger documentation is available locally once the server is running:

- **URL:** `http://localhost:8080/swagger/index.html`

---

## 📄 License

© 2026 Alcodist Labs. All rights reserved.
