# Spring Boot Microservice Template

## Overview

This template generates a production-ready Spring Boot microservice following **Hexagonal Architecture** (Ports and Adapters) principles. It provides a solid foundation for building scalable, maintainable, and testable microservices.

## Key Features

- ✅ **Hexagonal Architecture** - Clean separation of concerns
- ✅ **Spring Boot 3.2.5** - Latest stable version with Java 21
- ✅ **Complete CRUD operations** - Ready-to-use REST endpoints
- ✅ **Database integration** - PostgreSQL with JPA/Hibernate
- ✅ **Docker support** - Multi-stage Dockerfile and docker-compose
- ✅ **CI/CD workflows** - GitHub Actions with automated testing
- ✅ **Test coverage** - 85% threshold with JaCoCo
- ✅ **API documentation** - SpringDoc OpenAPI 3 (Swagger)
- ✅ **Code quality** - MapStruct, Lombok, and best practices
- ✅ **Multiple environments** - Local, develop, test, staging, production

## What You Get

When you use this template, you'll get a complete microservice with:

### 🏗️ Architecture Components
- **Domain Layer**: Business logic and entities
- **Application Layer**: Use cases, DTOs, and service interfaces
- **Infrastructure Layer**: Controllers, repositories, and configurations

### 🛠️ Development Tools
- Maven build configuration
- JUnit 5 testing framework
- JaCoCo code coverage
- MapStruct for object mapping
- Lombok for reducing boilerplate

### 🚀 DevOps Ready
- GitHub Actions CI/CD pipeline
- Docker containerization
- Multi-environment configuration
- Health checks and monitoring

### 📚 Documentation
- Comprehensive README
- API documentation with Swagger
- Architecture decision records

## Quick Start

1. **Use the template** in Backstage to generate your microservice
2. **Configure** your database connection
3. **Run locally** with `mvn spring-boot:run`
4. **Access Swagger UI** at `http://localhost:8080/swagger-ui.html`
5. **Start developing** your business logic in the domain layer

## Next Steps

- [Architecture Overview](architecture.md) - Understand the hexagonal architecture
- [Technology Stack](technology-stack.md) - Learn about the technologies used
- [Development Guide](development-guide.md) - Start developing your microservice