# Node.js + MySQL Docker Compose Project

## 📌 Project Overview

This project demonstrates how to containerize a Node.js Express application and a MySQL database using Docker and Docker Compose.

The application and database run in separate containers and communicate through Docker Compose networking. MySQL data is stored in a Docker volume to ensure persistence even if the containers are removed.

---

## 🛠 Technologies Used

* Node.js
* Express.js
* MySQL 8
* Docker
* Docker Compose

---

## 📁 Project Structure

```text
.
├── app/
├── server.js
├── package.json
├── package-lock.json
├── Dockerfile
├── docker-compose.yml
├── .dockerignore
├── .env
└── README.md
```

---

## 🏗 Architecture

```text
Browser
    │
localhost:8080
    │
    ▼
Node.js (Express)
    │
Docker Network
    │
    ▼
MySQL 8
    │
Docker Volume
```

---

## ⚙ Environment Variables

Create a `.env` file in the project root.

```env
DB_HOST=mysql
DB_USER=root
DB_PASSWORD=123456
DB_NAME=dbtest

MYSQL_ROOT_PASSWORD=123456
MYSQL_DATABASE=dbtest
```

---

## 🚀 Run the Project

### Build and Start Containers

```bash
docker compose up --build
```

### Run in Background

```bash
docker compose up -d
```

### Stop Containers

```bash
docker compose down
```

---

## 🌐 Access the Application

```
http://localhost:8080
```

> Note: If the project does not define a `/` route, a `404 Not Found` response is expected. Use the API endpoints implemented by the project.

---

## 💾 Persistent Storage

A Docker named volume is used to persist MySQL data.

```yaml
volumes:
  - db_data:/var/lib/mysql
```

This ensures database data remains available even after containers are recreated.

---

## 📚 Docker Concepts Practiced

* Dockerfile
* Single-stage build
* Docker Compose
* Docker Networking
* Environment Variables
* `.env`
* `depends_on`
* Named Volumes
* Port Mapping
* MySQL Container
* Node.js Container Communication

---

## 📖 Learning Outcome

Through this project, I learned how to:

* Analyze a backend repository
* Write a Dockerfile
* Create a Docker Compose configuration
* Connect a Node.js application to MySQL using Docker networking
* Use environment variables for application configuration
* Persist database data with Docker volumes
* Debug Docker Compose configuration issues

---

## 👨‍💻 Author

**Syed Salman N**

Aspiring DevOps Engineer | AWS | Docker | Kubernetes | CI/CD
