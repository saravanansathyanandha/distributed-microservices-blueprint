# Distributed Microservices Blueprint 🚀

Enterprise-grade microservices template built with **NestJS**, **RabbitMQ**, and **PostgreSQL**. This repository demonstrates production-ready patterns for distributed systems.

## 🏗️ Architecture
- **DDD (Domain-Driven Design):** Focused on core business logic.
- **Clean Architecture:** Decoupling infrastructure from business rules.
- **Event-Driven:** Asynchronous communication via RabbitMQ.
- **Observability:** Centralized logging and health checks.

`mermaid
graph TD
    Client -->|REST| Gateway[API Gateway / NestJS]
    Gateway -->|Publish Event| RMQ[RabbitMQ]
    RMQ -->|Consume Event| S1[Service A]
    RMQ -->|Consume Event| S2[Service B]
    Gateway -->|Read/Write| DB[(PostgreSQL)]
`

## 🛠️ Tech Stack
- **Framework:** NestJS (Node.js)
- **Messaging:** RabbitMQ
- **Database:** PostgreSQL with Prisma ORM
- **DevOps:** Docker, Docker Compose, GitHub Actions

## 🚀 Getting Started
1. Clone the repository.
2. Run docker-compose up -d.
3. The API will be available at http://localhost:3000.

## 📦 Features
- [x] Hybrid Application (HTTP + Microservice)
- [x] Event Publishing & Subscribing
- [x] Prisma Integration
- [x] Dockerized Infrastructure