## Hi there 👋

# 🧱 Microservices System Architecture (Java + React)

This project consists of multiple microservices built using **Java Spring Boot**, **ReactJS**, and **Terraform**. Each service is developed and versioned in its own GitHub repository, but they can be organized locally in this folder structure for ease of development and deployment.

## 📦 Services

| Repo Name                    | Description                                      |
|-----------------------------|--------------------------------------------------|
| `spring-gateway`            | API Gateway (Spring Cloud Gateway)              |
| `spring-discovery`          | Eureka Discovery Server                          |
| `spring-grpc-user-service`  | User Service with REST + gRPC, MongoDB           |
| `spring-grpc-stock-service` | Stock Service with REST + gRPC, MongoDB          |
| `spring-grpc-meet-service`  | Real-time Meet Service with WebSocket            |
| `stock-portal-frontend`     | Frontend in ReactJS                              |
| `jitsi-deployment`          | Jitsi Meet setup (standalone)                    |
| `keycloak-auth-server`      | Identity provider using Keycloak + PostgreSQL    |
| `infra`                     | Terraform/Terragrunt scripts for AWS deployment  |

## 🔧 How to Set Up Locally

1. Clone this folder structure
2. Clone each repo inside it
3. Run with Docker Compose or run services individually

## 🗺️ Architecture Overview

```plaintext
          +-----------+           +----------------+
          |  Frontend | <--->     |  API Gateway   |
          +-----------+           +----------------+
                                     |
  +--------------+------------------+-------------------+
  |              |                  |                   |
+----+     +----------------+  +----------------+   +---------------+
|User| --> | User-Service    |  | Stock-Service  |   | Meet-Service  |
| DB |     | (REST + gRPC)   |  | (REST + gRPC)  |   | (WebSocket)   |
+----+     +----------------+  +----------------+   +---------------+
```
Eureka, Keycloak, MongoDB Atlas, and PostgreSQL via KeyDB Cloud
