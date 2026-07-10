# 🚀 RelayCore

A production-inspired **Distributed Job Scheduling Platform** built with **FastAPI**, **React**, and **PostgreSQL**. The project demonstrates modern backend engineering practices, scalable architecture, concurrent job execution, and a monitoring dashboard.

> **Goal:** Build an industry-inspired distributed job scheduler that showcases software engineering skills rather than simply implementing features.

---

## 📌 Overview

The Distributed Job Scheduler enables organizations to:

* Create and manage multiple projects
* Organize work into queues
* Schedule asynchronous jobs
* Execute jobs using background workers
* Automatically retry failed jobs
* Move permanently failed jobs to a Dead Letter Queue
* Monitor workers, jobs, queues, and system health through a web dashboard

The project is inspired by production systems such as:

* BullMQ
* Sidekiq
* Celery
* AWS SQS
* RabbitMQ Workers

---

# ✨ Features

## Authentication

* User Registration
* User Login
* JWT Authentication
* Password Hashing (bcrypt)

## Project Management

* Multiple Projects
* Project Isolation

## Queue Management

* Queue Priorities
* Configurable Concurrency
* Retry Policies
* Pause / Resume Queues
* Queue Statistics

## Job Scheduling

Supports multiple job types:

* Immediate Jobs
* Delayed Jobs
* Scheduled Jobs
* Recurring Jobs
* Batch Jobs

## Worker Engine

* Background Worker Processes
* Concurrent Job Execution
* Atomic Job Claiming
* Worker Heartbeats
* Graceful Shutdown

## Retry System

* Fixed Delay
* Linear Backoff
* Exponential Backoff

## Dead Letter Queue

Jobs exceeding retry limits are automatically transferred to a Dead Letter Queue.

## Monitoring

Track:

* Job Status
* Worker Status
* Execution History
* Retry History
* Execution Time
* Error Logs
* Queue Health
* Metrics Dashboard

---

# 🏗️ System Architecture

```
                 React Dashboard
                        │
                        ▼
               FastAPI REST API
                        │
                        ▼
                 PostgreSQL Database
                        │
        ┌───────────────┴───────────────┐
        ▼                               ▼
 Scheduler Service               Worker Pool
        │                               │
        └───────────────┬───────────────┘
                        ▼
                 Job Execution Engine
```

---

# 🛠️ Tech Stack

## Frontend

* React
* TypeScript
* Tailwind CSS
* React Query
* Chart.js

## Backend

* FastAPI
* SQLAlchemy
* JWT Authentication
* bcrypt

## Database

* PostgreSQL

## Worker

* Python AsyncIO

## DevOps

* Docker
* Docker Compose

---

# 📁 Project Structure

```
distributed-job-scheduler/

├── backend/
│   ├── api/
│   ├── auth/
│   ├── middleware/
│   ├── models/
│   ├── repositories/
│   ├── scheduler/
│   ├── services/
│   ├── utils/
│   └── workers/
│
├── frontend/
│
├── database/
│
├── tests/
│
├── docs/
│
├── docker/
│
├── docker-compose.yml
├── README.md
└── .gitignore
```

---

# 🚀 Getting Started

## Prerequisites

* Python 3.11+
* Node.js 20+
* PostgreSQL
* Docker (optional)

---

## Clone Repository

```bash
git clone https://github.com/<your-username>/distributed-job-scheduler.git

cd distributed-job-scheduler
```

---

## Backend Setup

```bash
cd backend

python -m venv venv

# Windows
venv\Scripts\activate

# Linux / macOS
source venv/bin/activate

pip install -r requirements.txt
```

Create a `.env` file:

```env
DATABASE_URL=postgresql://username:password@localhost:5432/job_scheduler

SECRET_KEY=your-secret-key

ALGORITHM=HS256

ACCESS_TOKEN_EXPIRE_MINUTES=60
```

Run the backend:

```bash
uvicorn app.main:app --reload
```

---

## Frontend Setup

```bash
cd frontend

npm install

npm run dev
```

---

## Docker

```bash
docker compose up --build
```

---

# 📚 API Documentation

After starting the backend:

Swagger UI

```
http://localhost:8000/docs
```

ReDoc

```
http://localhost:8000/redoc
```

---

# 🗂️ Development Roadmap

* ✅ Authentication
* ✅ Project Management
* ✅ Queue Management
* ✅ Job Scheduling
* ✅ Worker Engine
* ✅ Retry System
* ✅ Dead Letter Queue
* ✅ Monitoring Dashboard
* ✅ Testing
* ✅ Documentation

---

# 🧪 Testing

Run backend tests:

```bash
pytest
```

Future test coverage includes:

* Unit Tests
* API Tests
* Worker Tests
* Concurrency Tests
* Failure Recovery Tests

---

# 📖 Documentation

Project documentation includes:

* Software Architecture
* ER Diagram
* API Documentation
* Sequence Diagrams
* Design Decisions
* Database Schema
* Testing Strategy
* Deployment Guide

---

# 🎯 Engineering Goals

This project emphasizes:

* Clean Architecture
* Modular Design
* Scalability
* Maintainability
* Reliability
* Production-inspired Engineering Practices

The objective is to demonstrate strong software engineering principles suitable for backend and full-stack software engineering roles.

---

# 🤝 Contributing

Contributions, suggestions, and improvements are welcome.

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push the branch
5. Open a Pull Request

---

# 📄 License

This project is intended for educational and portfolio purposes.

---

## 👨‍💻 Author

**Arnav Amrit**

B.Tech Computer Science Engineering
SRM Institute of Science and Technology

---

⭐ If you found this project interesting, consider giving it a star on GitHub!
# RelayCore
