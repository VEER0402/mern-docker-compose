# MERN Stack Application using Docker & Docker Compose

This repository demonstrates how to containerize a complete MERN stack
application (Frontend, Backend, and MongoDB) using Docker and then orchestrate
all services using Docker Compose.

The purpose of this project is to understand real-world DevOps practices such as:
- Service isolation
- Container networking
- Environment-based configuration
- Transition from manual Docker commands to Docker Compose

---

## 🧱 Tech Stack

- Frontend: React (Vite)
- Backend: Node.js + Express
- Database: MongoDB
- Containerization: Docker
- Orchestration: Docker Compose

---

## 🚀 Phase 1: Manual Docker Setup (Learning Phase)

Initially, the application was set up using **manual Docker commands** to deeply
understand Docker fundamentals.

### Steps followed:

1. Created Dockerfile for frontend
2. Built frontend image and ran container
3. Created a custom Docker bridge network
4. Ran MongoDB container on the same network
5. Created Dockerfile for backend
6. Built backend image and ran container
7. Verified communication:
   - Frontend → Backend
   - Backend → MongoDB

### Key learnings:
- Difference between images and containers
- Custom Docker networks
- Container DNS (service-name based communication)
- Use of environment variables inside containers

---

## 🧹 Cleanup

After successful testing of the manual setup:
- All containers were stopped
- Images and containers were removed

This cleanup was done to move towards a cleaner and more maintainable setup.

---

## 🚀 Phase 2: Docker Compose Setup

The same MERN stack was then reimplemented using **Docker Compose** to replace
multiple manual Docker commands with a single declarative configuration.

### Services defined in `docker-compose.yml`:

- **frontend** – React application
- **backend** – Node.js + Express API
- **mongodb** – MongoDB database

### Features of Docker Compose setup:
- Single command startup
- Shared custom bridge network
- Service name based communication
- MongoDB data persistence using Docker volumes
- Environment variable based configuration

---

## ▶️ How to Run the Application

### Prerequisites
- Docker
- Docker Compose

### Start all services
```bash
docker compose up --build
