[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

# 📋 Kanban Board Application

A containerized Kanban Board web app for visualizing and managing tasks, built with Angular, Spring Boot, and PostgreSQL.

## 🚀 Project Overview

Kanban is a workflow visualization tool originally created at Toyota and now ubiquitous in software development. This implementation provides:

- Three columns: **TODO**, **In Progress**, and **Done**  
- Drag-and-drop cards to represent tasks and update statuses in real time  
- A responsive Angular frontend, RESTful Spring Boot API, and PostgreSQL database  

## 🛠️ Technologies Used

| Layer     | Technology                   |
|-----------|------------------------------|
| Frontend  | Angular 16 SPA               |
| Backend   | Spring Boot (Java)           |
| Database  | PostgreSQL                   |
| Container | Docker & Docker Compose      |

## 🗂️ Project Structure

```
kanban-board/
├── docker-compose.yml # Multi-container orchestration
├── kanban-postgres/ # PostgreSQL container config
│ └── Dockerfile
├── kanban-app/ # Spring Boot REST API
│ ├── src/
│ └── Dockerfile
├── kanban-ui/ # Angular frontend
│ ├── src/
│ └── Dockerfile
└── README.md # This file
```

## ⚙️ Getting Started

### Prerequisites

- Docker ≥20.10  
- Docker Compose ≥1.29

### Installation

git clone https://github.com/Shirishreddybandi/Kanban-Board.git
cd Kanban-Board

### Launch the Application

docker-compose up -d

- Frontend: http://localhost:4200/  
- API Docs (Swagger UI): http://localhost:8080/api/swagger-ui.html  

Stop and remove containers:

docker-compose down

## 🔧 Configuration

Environment variables for PostgreSQL are defined in `docker-compose.yml`. By default:

services:
kanban-postgres:
image: postgres:9.6-alpine
environment:
- POSTGRES_DB=kanban
- POSTGRES_USER=kanban
- POSTGRES_PASSWORD=kanban

For production, replace plaintext credentials with a secret store.

## 🎯 Features

- Full CRUD operations on boards and tasks via REST API  
- Real-time drag-and-drop status updates in the UI  
- Modular, containerized architecture for zero-install local setup  
- Swagger UI for interactive API exploration  

## 📝 License

MIT License – see [LICENSE](LICENSE) for details.  

---
Made with ❤️ by Shirishreddybandi  
