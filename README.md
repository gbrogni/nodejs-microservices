📄 Overview

This repository contains a study project that demonstrates a microservices architecture built with Node.js. The goal was to experiment with a modular, decoupled system design — composing multiple services that communicate loosely, each responsible for a specific domain. The project is not production-ready, but it serves as a learning ground to explore best practices, service separation, containerization, and inter-service communication patterns.

🧰 Stack & Technologies

TypeScript — core language for type safety and improved developer experience.

Docker + Docker Compose — for containerization and orchestration of services and infrastructure.

API Gateway (via Kong) — centralizes routing for microservices.

Modular service structure: each service in its own folder (e.g. app-orders, app-invoices).

Contracts for inter-service communication (contracts/messages).

📂 Project Structure

/app-orders              # Service responsible for the Orders domain
/app-invoices            # Service responsible for the Invoices domain
/contracts/messages      # Shared message and API contracts
/docker/                 # Gateway and infrastructure configuration
/docker-compose.yml      # Local orchestration for all services
/infra                   # Infrastructure-related configs and support files

Each microservice implements its own domain logic while staying isolated from the others, following essential microservices principles such as loose coupling and clear boundaries.

🎯 Goals & Learnings

This project helped explore and practice:

✔️ Service Decomposition

Understanding how to break down a system into small, independent units that each handle a specific bounded context.

✔️ Loose Coupling & Clear Contracts

Services communicate through shared message definitions, reducing direct dependencies and encouraging decoupled design.

✔️ Docker-Based Orchestration

Using Docker Compose to simulate a multi-service environment locally, including gateway + microservices + infrastructure components.

✔️ API Gateway Pattern

Centralizing routing, request forwarding, and cross-cutting concerns behind a gateway.

✔️ Modular & Maintainable Structure

Organizing the codebase in a way that allows each service to evolve independently.