# microservice-patterns
This repository contains my Research & implementation notes on Microservice Architecture patterns
--
## 1. Decomposition Patterns
How to split a large monolith into small services.
 - By Business Capability: Each service represents a specific business function.
 - By Subdomain (DDD): Divide based on domain-driven design boundaries.
   *Ex:- Order Service, Payment Service, Inventory Service.

--
## 2.Communication Patterns
How microservices talk to each other.

 - Synchronous: REST, gRPC
 - Asynchronous: Event-driven using Kafka or RabbitMQ
 - API Gateway: Acts as a single entry point for all services
   *Ex:- Build two Spring Boot services communicating via REST or Kafka.

## 3. Data Management Patterns
Managing data in a distributed setup.

 - Database per serice: Each microservice has its own database.
 - Saga Pttern: Ensures consistency across services.
 - CQRS (Command Query Responsibility Segregation):Separate read and write models.
   *Ex:- Simulate order + payment transactions with Saga.

--
## 4. Observabillity & Deployment Patterns
How to monitor,scale, and manage microservices.

 - Service Discovery: Eureka,Consul
 - Circuit Breaker: Resilience4J or Hystrix
 - Centralized Logging: ELK Stack, Zipkin
 - Containerization: Docker + Kubernetes

--
## 5. Security Patterns
Securing microservices and APIs.

 - JWT Authentication
 - OAuth2 / Keycloak for centralized identity management
 - API Gateway + Token Validation.
