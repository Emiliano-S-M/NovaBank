<p style="text-align: center">
    <img src="docs/assets/NovaBank.png" alt="NovaBank Logo">
</p>

# NovaBank

## ✨ Features

- 🏦 Enterprise Banking Platform
- 🔐 JWT Authentication & Authorization
- 🌐 Microservices Architecture
- ☁️ Spring Cloud Ecosystem
- 🐳 Docker & Docker Compose
- 📖 Comprehensive Documentation
- 🧪 Unit & Integration Testing
- 🚀 CI/CD Ready

![Java](https://img.shields.io/badge/Java-21-orange?logo=openjdk)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-3.x-6DB33F?logo=springboot)
![Spring Cloud](https://img.shields.io/badge/Spring%20Cloud-2025-blue)
![Maven](https://img.shields.io/badge/Maven-3+-C71A36?logo=apachemaven)
![Status](https://img.shields.io/badge/Status-Sprint%201-success)
![License](https://img.shields.io/badge/License-MIT-blue)

> Enterprise Banking Platform built with Java, Spring Boot and Microservices Architecture.

---

## Acerca de

NovaBank es una plataforma bancaria desarrollada como proyecto de portafolio profesional.

El objetivo del proyecto es simular un sistema bancario moderno aplicando arquitecturas utilizadas en la industria, incluyendo microservicios, Spring Cloud, Spring Security y despliegue con Docker.

El proyecto está siendo desarrollado siguiendo buenas prácticas de ingeniería de software, documentación técnica y arquitectura empresarial.

---

## Objetivos

- Construir una plataforma bancaria distribuida.
- Aplicar arquitectura basada en microservicios.
- Implementar autenticación mediante JWT.
- Utilizar Spring Cloud.
- Desplegar con Docker.
- Automatizar procesos con GitHub Actions.
- Documentar decisiones arquitectónicas mediante ADR.

---

## Arquitectura

```text
                    Client
                       │
                       ▼
                 API Gateway
                       │
        ┌──────────────┼──────────────┐
        ▼              ▼              ▼
   Auth Service   Customer Service   Account Service
        │              │              │
        └──────────────┼──────────────┘
                       ▼
              Transaction Service
                       │
              RabbitMQ / Events
             ┌─────────┴─────────┐
             ▼                   ▼
     Notification Service   Audit Service
```

---

## Infraestructura

Actualmente el proyecto incluye:

- ✅ Config Server
- ✅ Eureka Discovery Server
- ✅ API Gateway

Próximamente:

- ⏳ Auth Service
- ⏳ Customer Service
- ⏳ Account Service
- ⏳ Transaction Service
- ⏳ Loan Service
- ⏳ Notification Service
- ⏳ Audit Service

---

## Tecnologías

- Java 21
- Spring Boot
- Spring Cloud
- Spring Security
- Maven
- PostgreSQL
- Docker
- Docker Compose
- RabbitMQ
- Redis
- OpenAPI
- JUnit 5
- Mockito

---

## Estructura del Proyecto

```text
NovaBank/
│
├── infrastructure/
├── services/
├── libraries/
├── docs/
├── docker/
├── scripts/
└── pom.xml
```

---

## Documentación

La documentación técnica de NovaBank está organizada para facilitar la comprensión de la arquitectura, las decisiones de diseño y la evolución del proyecto.

| Documento                                                       | Descripción                                                                                                        |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [System Architecture](docs/architecture/SYSTEM_ARCHITECTURE.md) | Describe la arquitectura general del sistema, los microservicios, la infraestructura y las tecnologías utilizadas. |
| [Domain Model](docs/architecture/DOMAIN_MODEL.md)               | Define el modelo de dominio, las entidades principales, sus relaciones y las reglas de negocio.                    |
| [Architecture Decision Records](docs/adr/)                      | Registro de las decisiones arquitectónicas tomadas durante el desarrollo del proyecto.                             |

---

## Roadmap

### Sprint 1 - Project Foundation
- [x] Maven Parent Project
- [x] Project structure
- [x] Config Server
- [x] Eureka Discovery Server
- [x] API Gateway
- [x] Initial documentation

### Sprint 2 - Authentication & Security
- [ ] Auth Service
- [ ] User registration
- [ ] Login
- [ ] JWT Authentication
- [ ] Refresh Tokens
- [ ] Role-Based Access Control (RBAC)
- [ ] OpenAPI Documentation

### Sprint 3 - Customer Management
- [ ] Customer Service
- [ ] Customer CRUD
- [ ] Address management
- [ ] Contact information

### Sprint 4 - Banking Accounts
- [ ] Account Service
- [ ] Savings accounts
- [ ] Checking accounts
- [ ] Balance management

### Sprint 5 - Transactions
- [ ] Transaction Service
- [ ] Deposits
- [ ] Withdrawals
- [ ] Transfers
- [ ] Transaction history

### Sprint 6 - Notifications
- [ ] Notification Service
- [ ] Email notifications
- [ ] SMS simulation
- [ ] Event-driven notifications

### Sprint 7 - Auditing
- [ ] Audit Service
- [ ] Audit logs
- [ ] Business events
- [ ] Traceability

### Sprint 8 - DevOps
- [ ] Docker Compose
- [ ] GitHub Actions
- [ ] Monitoring
- [ ] Logging
- [ ] Production profiles

### Sprint 9 - Cloud Deployment
- [ ] Kubernetes
- [ ] Helm
- [ ] CI/CD Pipeline
- [ ] Cloud deployment

---

## Estado del Proyecto

Sprint actual:

> Sprint 1 — Infraestructura Base

Estado:

- ☑️Maven Parent Project
- ☑️ Project structure 
- ☑️ Config Server
- ☑️ Eureka Discovery Server
- ☑️ API Gateway
- ☑️ Initial documentation

---

## Autor

Desarrollado por Emiliano Sánchez.