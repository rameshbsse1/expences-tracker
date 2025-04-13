## 🚀 Scalability & System Design

This project is built with scalability and resilience in mind. Here are some key design decisions:

### ✅ Stateless Microservices
- Services are built using **Spring Boot** and follow a **stateless architecture**.
- Enables horizontal scaling behind **AWS EC2 Auto Scaling Groups**.

### ⚡ Asynchronous Event-Driven Architecture
- Integrated with **Apache Kafka** to decouple services and handle high-throughput data flows.
- Kafka consumers can be scaled independently based on workload.

### 🧠 Caching & Database Optimization
- Frequently accessed data is cached using **Redis**.
- **Read replicas** used for SQL Server to distribute read-heavy workloads.

### 🔐 Resilience & Rate Limiting
- Circuit breaker pattern implemented using **Resilience4j**.
- **Rate limiting** configured at the API Gateway level to protect critical services.

### 📈 Monitoring & Auto-scaling
- Used **Amazon CloudWatch** with custom metrics and alarms.
- Auto-scaling rules trigger based on CPU, memory, and queue length metrics.

### 📦 Cloud Infrastructure
- Hosted on AWS with components like EC2, S3, Lambda, and RDS.
- CI/CD pipeline automates deployment and scaling.

> 🧪 Load tested using JMeter to validate performance under simulated spikes.
