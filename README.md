
<h1 align="center">🏥 Enterprise Patient Management System</h1>

<p align="center">
Production-Grade Microservices Architecture with Spring Boot, Kafka, gRPC, Docker & AWS
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Java-21-orange?logo=openjdk" />
  <img src="https://img.shields.io/badge/SpringBoot-3.x-brightgreen?logo=springboot" />
  <img src="https://img.shields.io/badge/Kafka-2.8-black?logo=apachekafka" />
  <img src="https://img.shields.io/badge/Docker-Containerized-blue?logo=docker" />
  <img src="https://img.shields.io/badge/AWS-CDK-orange?logo=amazonaws" />
  <img src="https://img.shields.io/badge/PostgreSQL-Database-blue?logo=postgresql" />
  <img src="https://img.shields.io/badge/License-MIT-green" />
</p>

---

## 📌 Project Overview

The **Enterprise Patient Management System** is a real-world, cloud-native microservices application built using modern backend engineering standards.

It demonstrates:

- ✅ Distributed microservices architecture  
- ✅ Secure JWT-based authentication  
- ✅ Event-driven communication using Kafka  
- ✅ High-performance service-to-service communication via gRPC  
- ✅ API Gateway implementation  
- ✅ Docker containerization  
- ✅ Infrastructure as Code using AWS CDK  
- ✅ Cloud simulation using LocalStack  
- ✅ Automated integration testing  

---

# 🏗 System Architecture

<p align="center">
  <img src="https://miro.medium.com/max/1400/1*9JqkQ7K2BEm90LkAMPxQYg.png" width="800"/>
</p>

### 🔹 Core Components

- Patient Service  
- Authentication Service  
- Billing Service (gRPC)  
- Analytics Service (Kafka Consumer)  
- API Gateway  
- PostgreSQL  
- Kafka Event Bus  
- AWS Infrastructure (LocalStack simulation)  

---

# 🧩 Microservices Breakdown

## 1️⃣ Patient Service

- CRUD operations
- Layered Architecture (Controller → Service → Repository → DTO)
- Kafka event publishing
- gRPC communication with Billing Service

---

## 2️⃣ Authentication Service

- User registration & login
- JWT token generation
- Token validation endpoint
- PostgreSQL user storage
- OAuth2-style security

---

## 3️⃣ API Gateway

- Built with Spring Cloud Gateway
- Centralized routing
- JWT validation filter
- Secured endpoints
- Request forwarding

---

## 4️⃣ Billing Service (gRPC)

- Protocol Buffers
- gRPC server/client
- High-performance internal communication

---

## 5️⃣ Analytics Service

- Kafka consumer
- Listens to Patient Created events
- Asynchronous event processing

---

# 🔐 Security Architecture

<p align="center">
  <img src="https://miro.medium.com/max/1400/1*6sYfXGgAvFp8Z_HKbjrKMg.png" width="700"/>
</p>

- JWT authentication
- Token issued by Auth Service
- API Gateway validates token
- 401 for unauthorized requests

---

# 🔄 Communication Patterns

| Type | Technology | Purpose |
|------|------------|----------|
| Client → Service | REST | External API access |
| Service → Service | gRPC | High-speed internal calls |
| Async Communication | Kafka | Event-driven decoupling |

---

# 🐳 Dockerized Environment

<p align="center">
  <img src="https://www.docker.com/wp-content/uploads/2022/03/Moby-logo.png" width="120"/>
</p>

- Each microservice has its own Dockerfile  
- Runs inside isolated containers  
- Ready for ECS deployment  
- Consistent runtime environment  

---

# ☁️ Infrastructure as Code (AWS CDK)

<p align="center">
  <img src="https://cdn.worldvectorlogo.com/logos/aws-2.svg" width="120"/>
</p>

Provisioned Resources:

- VPC  
- ECS Cluster  
- RDS (PostgreSQL)  
- MSK (Kafka)  
- Application Load Balancer  

Deployment:

- LocalStack (AWS simulation)
- CloudFormation auto-generated via CDK

---

# 🧪 Testing Strategy

<p align="center">
  <img src="https://junit.org/junit5/assets/img/junit5-logo.png" width="120"/>
</p>

### Tools Used

- JUnit 5  
- RestAssured  

### Coverage

✔ Successful login  
✔ Invalid login → 401  
✔ Protected endpoint access  
✔ JWT validation flow  

---

# 🛠 Tech Stack

| Layer | Technology |
|-------|------------|
| Language | Java 21 |
| Framework | Spring Boot 3.x |
| API Gateway | Spring Cloud Gateway |
| Database | PostgreSQL |
| Messaging | Apache Kafka |
| RPC | gRPC |
| Containerization | Docker |
| IaC | AWS CDK |
| Cloud Simulation | LocalStack |
| Testing | JUnit, RestAssured |

---

# 📦 Project Structure

```
enterprise-patient-management/
│
├── patient-service/
├── auth-service/
├── billing-service/
├── analytics-service/
├── api-gateway/
├── infrastructure-cdk/
├── docker-compose.yml
└── README.md
```

---

# 📊 System Flow

1. User logs in → JWT generated  
2. Client calls API Gateway  
3. Gateway validates token  
4. Request routed to Patient Service  
5. Patient Service:
   - Stores in PostgreSQL  
   - Calls Billing via gRPC  
   - Publishes Kafka event  
6. Analytics consumes event  

---

# 🎯 What This Project Demonstrates

- Enterprise-level microservices
- Secure distributed systems
- Event-driven architecture
- Cloud-native deployment
- Infrastructure automation
- Production-ready testing

---

# 👨‍💻 Author

**Anwar Sha**  
Full Stack Java Developer  
Spring Boot | Kafka | AWS | Docker | Microservices  

---

<p align="center">
⭐ If you found this project useful, please consider giving it a star!
</p>

