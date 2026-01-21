🛒 Spring Boot eCommerce Microservices Application
📖 Overview
This repository hosts a production-grade eCommerce backend system built using a Microservices Architecture. It is designed to demonstrate high scalability, fault tolerance, and loose coupling between services. The system utilizes Spring Boot for core services, Docker for containerization, and implements both synchronous (REST) and asynchronous (RabbitMQ/Kafka) communication patterns.

This project serves as a comprehensive proof-of-concept for building cloud-native distributed systems handling complex business flows like order management, inventory updates, and notification dispatching.

🏗 System Architecture
The application is decomposed into independent, deployable microservices organized by business domain:
Service,            Description,Port
Api Gateway,        Entry point for all client traffic; handles routing and load balancing.,8080
Eureka Server,      Service Discovery server (Netflix Eureka) for dynamic service registration.,8761
Config Server,      Centralized configuration management for all microservices.,8888
Product Service,    "Manages product inventory, catalog data, and stock checks.",8081
Order Service,       Handles order placement and transactions.,8082
User Service,        Manages user profiles and authentication data.,8083
Notification-Service,"Listens for events (e.g., OrderPlaced) and triggers emails/alerts.",8084

🚀 Key Features
Microservices Architecture: Decoupled services utilizing Spring Cloud for coordination.


Event-Driven Communication: Implemented Apache Kafka and RabbitMQ for asynchronous messaging (e.g., sending notifications after order placement).


Centralized Security: Secured with Keycloak (OAuth2/OpenID Connect) for robust identity management and role-based access control (RBAC).


Service Discovery: Dynamic registration of services using Netflix Eureka.

API Gateway: Spring Cloud Gateway acting as a single edge service for routing, filtering, and cross-cutting concerns.


Resiliency: Implemented Circuit Breakers (Resilience4j) to handle cascading failures and ensure system uptime.


Observability Stack: Integrated distributed tracing and metrics using Zipkin/Jaeger, Prometheus, and Grafana for real-time monitoring.


Containerization: Fully dockerized services with docker-compose for one-click deployment.

🛠️ Technology Stack
Languages: Java 17+, JavaScript

Frameworks: Spring Boot 3.x, Spring Cloud (Gateway, Config, Stream, OpenFeign)

Databases (Polyglot Persistence): PostgreSQL, MongoDB, MySQL

Message Brokers: Apache Kafka, RabbitMQ

Containerization: Docker, Docker Compose

Security: Keycloak (OAuth2 resource server)

Build Tool: Maven

⚡ Getting Started
Prerequisites
Java 17 or higher

Docker & Docker Compose

Maven


👨‍💻 Author
Swapnaneel Chatterjee

GitHub: Swapnaneel1616

LinkedIn: Swapnaneel Chatterjee
