# Usage Guide

## Creating a New Service

### 1. Access Template
- Navigate to **Create** → **Choose a template** in Backstage
- Select **Spring WebFlux Microservice**

### 2. Component Information
- **Component ID**: Unique identifier (kebab-case, e.g., `user-service-webflux`)
- **Description**: Brief service description
- **Owner**: Team or person responsible
- **Email**: Contact email

### 3. Java Configuration
- **Artifact ID**: Maven artifact identifier
- **Java Version**: 17 or 21
- **Spring Boot Version**: 3.2.5 or 3.3.0

### 4. Repository
- **Repository URL**: GitHub repository location
- Must be under `addon-ai` organization

## Generated Project

### What Gets Created
```
your-service/
├── src/main/java/com/example/userservice/
├── src/test/java/
├── docs/                    # TechDocs documentation
├── .github/workflows/       # CI/CD pipelines
├── docker-compose.yml       # Local development
├── Dockerfile              # Container image
├── pom.xml                 # Maven configuration
├── catalog-info.yml        # Backstage metadata
└── README.md               # Project documentation
```

### Immediate Next Steps
1. **Review generated code structure**
2. **Configure environment variables**
3. **Run tests**: `./mvnw test`
4. **Start application**: `./mvnw spring-boot:run`
5. **Access API docs**: http://localhost:8080/swagger-ui.html

### Development Workflow
1. **Local development**: Use docker-compose for dependencies
2. **Feature development**: Create feature branches
3. **Testing**: Maintain 85% code coverage
4. **Pull requests**: Automatic PR to develop branch
5. **Deployment**: CI/CD handles build and deployment

## Best Practices

### Reactive Programming
- Use `Mono<T>` for single values
- Use `Flux<T>` for multiple values
- Avoid blocking operations
- Chain reactive operations

### Architecture
- Keep domain layer pure (no external dependencies)
- Use ports and adapters pattern
- Implement use cases in application layer
- Configure external integrations in infrastructure layer
