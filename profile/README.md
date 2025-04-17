## Hi there 👋

# 🧱 Microservices System Architecture (Java + React)

This project consists of multiple microservices built using **Java Spring Boot**, **ReactJS**, and **Terraform**. Each service is developed and versioned in its own GitHub repository, but they can be organized locally in this folder structure for ease of development and deployment.

## 📦 Services

|No.| Repo Name                   | Description                                      |
|---|-----------------------------|--------------------------------------------------|
| 1 | `spring-gateway`            | API Gateway (Spring Cloud Gateway)               |
| 2 | `spring-discovery`          | Eureka Discovery Server                          |
| 3 | `spring-grpc-user-service`  | User Service with REST + gRPC, MongoDB           |
| 4 | `spring-grpc-stock-service` | Stock Service with REST + gRPC, MongoDB          |
| 5 | `spring-grpc-meet-service`  | Real-time Meet Service with WebSocket            |
| 6 | `stock-portal-frontend`     | Frontend in ReactJS                              |
| 7 | `jitsi-deployment`          | Jitsi Meet setup (standalone)                    |
| 8 | `keycloak-auth-server`      | Identity provider using Keycloak + PostgreSQL    |
| 9 | `infra`                     | Terraform/Terragrunt scripts for AWS deployment  |

## Links:
- https://github.com/spring-microservices-app/spring-gateway
- https://github.com/spring-microservices-app/spring-disco
- https://github.com/spring-microservices-app/spring-grpc-user-service
- https://github.com/spring-microservices-app/spring-grpc-stock-service
- https://github.com/spring-microservices-app/spring-grpc-meet-service
- https://github.com/spring-microservices-app/stock-portal-frontend
- https://github.com/spring-microservices-app/jitsi-deployment
- https://github.com/spring-microservices-app/keycloak-auth-server
- https://github.com/spring-microservices-app/infra

## 🔧 How to Set Up Locally

1. Clone this folder structure
2. Clone each repo inside it
3. Run services individually

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
