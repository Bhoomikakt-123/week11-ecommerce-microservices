# 🚀 E-Commerce Microservices Platform

## 📌 Project Overview

This project implements a **scalable microservices-based e-commerce system** using Spring Boot and modern cloud-native technologies.
It demonstrates **service decomposition, event-driven architecture, and distributed system design**.

---

## 🎯 Objectives

* Design a **microservices architecture**
* Implement **service discovery using Eureka**
* Build an **API Gateway**
* Use **Kafka for event-driven communication**
* Handle **distributed transactions using Saga pattern**
* Deploy using **Docker (and optionally Kubernetes)**

---

## 🏗️ Architecture

```
Client
   ↓
API Gateway (Spring Cloud Gateway)
   ↓
----------------------------------------
|  Product Service   |  Order Service  |
|  Payment Service   |  User Service   |
|  Inventory Service| Notification Svc|
----------------------------------------
   ↓
Kafka (Event Streaming)
   ↓
Databases (Each service has its own DB)
```

---

## 🧩 Microservices

| Service                    | Description                    |
| -------------------------- | ------------------------------ |
| API Gateway                | Entry point, routing, security |
| Service Discovery (Eureka) | Registers all services         |
| Product Service            | Manages product catalog        |
| Order Service              | Handles order creation         |
| Payment Service            | Processes payments             |
| User Service               | Manages users                  |
| Inventory Service          | Tracks stock                   |
| Notification Service       | Sends alerts                   |

---

## ⚙️ Technology Stack

* Java 17
* Spring Boot
* Spring Cloud (Gateway, Eureka)
* Apache Kafka
* PostgreSQL
* Docker
* Kubernetes (optional)
* Prometheus + Grafana (monitoring)

---

## 🔄 Event-Driven Communication

Kafka is used for async communication:

* `OrderCreated`
* `PaymentCompleted`
* `InventoryReserved`
* `NotificationSent`

---

## 🔁 Saga Pattern

Used for **distributed transactions**:

1. Order Created
2. Payment Initiated
3. Inventory Reserved
4. If failure → Compensation triggered

---

## 🔐 API Gateway

* Central entry point
* Routing requests
* Authentication & security
* Rate limiting

---

## 📊 Monitoring & Logging

* Prometheus → Metrics
* Grafana → Visualization
* ELK Stack → Logging

---

## 🐳 Docker Setup

```bash
docker-compose up -d
```

---

## ▶️ How to Run

### Step 1: Start Infrastructure

```bash
docker-compose up -d
```

### Step 2: Run Services

Run each Spring Boot service:

```bash
mvn spring-boot:run
```

---

## 🌐 Ports

| Service         | Port |
| --------------- | ---- |
| API Gateway     | 8080 |
| Eureka Server   | 8761 |
| Product Service | 8081 |
| Order Service   | 8082 |
| Payment Service | 8083 |

---

## 📡 Sample API

### Create Order

```http
POST /api/orders
```

```json
{
  "productId": 1,
  "quantity": 2
}
```

---

## 📂 Project Structure

```
week11-ecommerce-microservices/
│── api-gateway/
│── service-discovery/
│── product-service/
│── order-service/
│── payment-service/
│── infrastructure/
│── README.md
```

---

## 📈 Key Features

✔ Microservices architecture
✔ Service discovery (Eureka)
✔ API Gateway routing
✔ Event-driven system (Kafka)
✔ Distributed transactions (Saga)
✔ Docker containerization

---

## 🧪 Testing

* Unit testing using JUnit
* API testing using Postman
* Integration testing (optional)

---

## 📄 Documentation

* 📘 Project Report (PDF included)
* 📊 Architecture explanation
* 🔄 Event flow design

---

## ✅ Conclusion

This project demonstrates a **real-world enterprise microservices system** with scalability, resilience, and modular design.
It is suitable for modern cloud-native applications.

---

## 👩‍💻 Author

**Bhoomika K T**
CSE Student | Microservices & AI Enthusiast

---

## ⭐ Tips for Evaluation

* Explain **Saga pattern clearly**
* Show **architecture diagram**
* Mention **Kafka event flow**
* Highlight **independent services**

---
