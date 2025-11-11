# WebFlux Reactive Microservice Template

## Overview

This template generates a production-ready **reactive microservice** using Spring WebFlux and following **Hexagonal Architecture** principles. It's designed for high-throughput, non-blocking applications that can handle thousands of concurrent requests efficiently.

## Key Features

- ✅ **Reactive Programming** - Non-blocking I/O with Project Reactor
- ✅ **Spring WebFlux** - Reactive web framework
- ✅ **Hexagonal Architecture** - Clean separation of concerns
- ✅ **R2DBC** - Reactive database connectivity
- ✅ **Reactive Streams** - Backpressure handling
- ✅ **Complete CRUD operations** - Reactive REST endpoints
- ✅ **Database integration** - PostgreSQL with R2DBC
- ✅ **Docker support** - Optimized for reactive workloads
- ✅ **CI/CD workflows** - GitHub Actions with reactive testing
- ✅ **Test coverage** - 85% threshold with reactive testing
- ✅ **API documentation** - SpringDoc OpenAPI 3 for WebFlux
- ✅ **Reactive monitoring** - Actuator with reactive metrics

## What You Get

When you use this template, you'll get a complete reactive microservice with:

### 🔄 Reactive Components
- **Reactive Controllers**: Non-blocking REST endpoints returning `Mono` and `Flux`
- **Reactive Services**: Asynchronous business logic processing
- **Reactive Repositories**: R2DBC-based data access with reactive streams
- **Reactive Error Handling**: Non-blocking exception management

### 🏗️ Architecture Components
- **Domain Layer**: Reactive business logic and entities
- **Application Layer**: Reactive use cases and DTOs
- **Infrastructure Layer**: WebFlux controllers and R2DBC repositories

### 🛠️ Reactive Development Tools
- Maven build with WebFlux dependencies
- Reactive testing with `WebTestClient`
- JaCoCo code coverage for reactive code
- MapStruct for reactive object mapping
- Lombok for reducing boilerplate

### 🚀 Reactive DevOps
- GitHub Actions CI/CD for reactive applications
- Docker containerization optimized for reactive workloads
- Multi-environment reactive configuration
- Reactive health checks and monitoring

## Reactive Benefits

### ⚡ Performance
- **High Throughput**: Handle thousands of concurrent requests
- **Low Latency**: Non-blocking I/O operations
- **Resource Efficiency**: Better CPU and memory utilization
- **Scalability**: Elastic scaling with reactive streams

### 🔄 Resilience
- **Backpressure**: Automatic flow control
- **Error Recovery**: Reactive error handling strategies
- **Circuit Breakers**: Fault tolerance patterns
- **Timeouts**: Non-blocking timeout handling

### 🌊 Reactive Streams
- **Publisher**: `Mono` (0-1 element) and `Flux` (0-N elements)
- **Subscriber**: Reactive consumers
- **Subscription**: Flow control mechanism
- **Processor**: Transform reactive streams

## Quick Start

1. **Use the template** in Backstage to generate your reactive microservice
2. **Configure** your R2DBC database connection
3. **Run locally** with `mvn spring-boot:run`
4. **Access Swagger UI** at `http://localhost:8080/swagger-ui.html`
5. **Test reactive endpoints** with tools like WebTestClient
6. **Monitor reactive metrics** at `http://localhost:8080/actuator`

## Performance Characteristics

### Traditional vs Reactive

| Aspect | Traditional (Servlet) | Reactive (WebFlux) |
|--------|----------------------|-------------------|
| **Threading Model** | One thread per request | Event loop with few threads |
| **Memory Usage** | High (thread stacks) | Low (shared event loop) |
| **Concurrency** | Limited by thread pool | Virtually unlimited |
| **I/O Operations** | Blocking | Non-blocking |
| **Backpressure** | Manual handling | Built-in support |

### When to Use Reactive

✅ **Good for**:
- High-concurrency applications
- I/O intensive operations
- Streaming data processing
- Microservices with many external calls
- Real-time applications

❌ **Not ideal for**:
- CPU-intensive operations
- Simple CRUD applications with low concurrency
- Teams unfamiliar with reactive programming
- Legacy system integration

## Next Steps

- [Reactive Architecture](reactive-architecture.md) - Understand reactive hexagonal architecture
- [Technology Stack](technology-stack.md) - Learn about reactive technologies
- [Reactive Patterns](reactive-patterns.md) - Common reactive programming patterns
- [Development Guide](development-guide.md) - Start developing reactive microservices