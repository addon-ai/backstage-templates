# 🏗️ Backstage Software Templates Collection

Comprehensive collection of Spring Boot and Spring WebFlux templates following **Hexagonal Architecture (Ports and Adapters)** principles.

## 📚 Available Templates

### Generic Templates (Self-Service)

- **java-springboot**: Spring Boot microservice with JPA/Hibernate
  - Synchronous (Thread-per-request)
  - Spring MVC for REST APIs
  - JPA/Hibernate for persistence
  - Tags: `spring-boot`, `java`, `hexagonal`, `microservice`, `jpa`, `mvc`

- **java-spring-webflux**: Spring WebFlux reactive microservice
  - Reactive (Non-blocking)
  - Spring WebFlux for REST APIs
  - R2DBC for reactive persistence
  - Tags: `spring-webflux`, `java`, `hexagonal`, `microservice`, `r2dbc`, `reactive`

### Project-Specific Templates

- **back-ms-users**: Microservice for users management (Synchronous/Spring Boot)
- **back-ms-movies**: Microservice for movie rental management (Synchronous/Spring Boot)
- **back-ms-users-webflux**: Reactive microservice for users management with Spring WebFlux (Reactive/WebFlux)
- **back-ms-movies-webflux**: Reactive microservice for movie rental management with Spring WebFlux (Reactive/WebFlux)

## 🏛️ Architecture

All templates follow **Hexagonal Architecture** principles with three main layers:

### 🎯 Domain Layer
- Pure business logic and domain models
- No external dependencies
- Domain entities and business rules

### 🔧 Application Layer
- Use cases and application services
- DTOs and mappers (MapStruct)
- Input/Output ports (interfaces)

### 🏗️ Infrastructure Layer
- REST controllers (input adapters)
- JPA/R2DBC repositories (output adapters)
- Configuration and external integrations

## ✨ Features

### Code Generation
- ✅ Complete CRUD operations
- ✅ DTOs with Bean Validation
- ✅ MapStruct entity transformations
- ✅ JPA entities or R2DBC entities
- ✅ REST controllers with OpenAPI
- ✅ Service layer with business logic
- ✅ Repository interfaces

### Documentation
- ✅ OpenAPI/Swagger integration
- ✅ TechDocs for each API
- ✅ Architecture diagrams (PlantUML)
- ✅ API reference documentation
- ✅ Sequence diagrams for CRUD operations

### Testing
- ✅ Unit tests with 100% coverage
- ✅ Integration tests
- ✅ JaCoCo code coverage (85% threshold)
- ✅ Edge case testing

### DevOps
- ✅ GitHub Actions CI/CD workflows
- ✅ Multi-environment support (local, develop, test, staging, prod)
- ✅ Docker and docker-compose
- ✅ Automated branch management
- ✅ Pull request automation

### Backstage Integration
- ✅ Catalog entities (Components, APIs, Systems, Domains)
- ✅ TechDocs integration
- ✅ API entity files with OpenAPI specs
- ✅ System and domain relationships
- ✅ Dependency tracking

## 📁 Repository Structure

```
backstage-templates/
├── commons/                          # Shared catalog entities
│   ├── dependencies.yml             # Technology stack resources
│   ├── domains.yml                  # Business domains
│   ├── org.yml                      # Organization structure
│   └── systems.yml                  # System definitions
├── templates/                        # Generic templates
│   ├── java-springboot/
│   │   ├── skeleton/                # Project skeleton
│   │   │   ├── catalog-info.yml    # Component metadata (Nunjucks)
│   │   │   ├── Dockerfile          # Multi-stage Docker build (Nunjucks)
│   │   │   ├── docker-compose.yml  # Local development (Nunjucks)
│   │   │   └── README.md           # Project documentation (Nunjucks)
│   │   └── template.yml            # Backstage scaffolder template
│   └── java-spring-webflux/
│       ├── skeleton/
│       └── template.yml
├── {project-name}/                   # Project-specific templates
│   ├── apis/                        # API entity files
│   │   └── {service}/
│   │       ├── {service}-api.yml   # API entity
│   │       ├── mkdocs.yml          # TechDocs config
│   │       └── docs/               # API documentation
│   ├── openapi/                     # OpenAPI specifications
│   ├── docs/                        # Project documentation
│   ├── catalog-info.yml            # Template metadata
│   ├── mkdocs.yml                  # TechDocs config
│   └── template.yml                # Scaffolder template
├── catalog-location.yml             # Components location
├── apis-location.yml                # APIs location
├── dependencies-location.yml        # Dependencies location
├── domains-location.yml             # Domains location
├── org-location.yml                 # Organization location
├── systems-location.yml             # Systems location
└── README.md                        # This file
```

## 🚀 Usage

### In Backstage UI

1. Navigate to **Create** → **Choose a template**
2. Select **Spring Boot Microservice** or **Spring WebFlux Microservice**
3. Fill in the form:
   - Component information (name, description, owner)
   - Java configuration (groupId, artifactId, versions)
   - Database settings
   - Features (Swagger, Actuator, Security)
   - CI/CD options
4. Click **Create** to generate the project

### Template Parameters

#### Component Information
- **component_id**: Unique identifier (kebab-case)
- **description**: Brief service description
- **owner**: Team or person responsible
- **email**: Contact email
- **version**: Initial version (semver)
- **system**: System this component belongs to
- **lifecycle**: experimental | production | deprecated

#### Java Configuration
- **groupId**: Maven group ID (e.g., com.example)
- **artifactId**: Maven artifact ID
- **serviceName**: Java package name (lowercase, no hyphens)
- **javaVersion**: 17 | 21
- **springBootVersion**: 3.2.5 | 3.3.0

#### Database
- **database**: PostgreSQL | MySQL | H2
- **enableLiquibase**: Database migrations

#### Features
- **enableSwagger**: OpenAPI documentation
- **enableActuator**: Health checks and metrics
- **enableSecurity**: Spring Security
- **coverageThreshold**: Minimum code coverage (0-100)

#### DevOps
- **enableGithubActions**: CI/CD pipeline
- **enableDocker**: Dockerfile and docker-compose
- **environments**: Deployment environments

## 🔗 Catalog Integration

### Location Files

Import all entities using wildcard patterns:

```yaml
# Import all components
- type: url
  target: https://github.com/{org}/backstage-templates/blob/main/catalog-location.yml

# Import all APIs
- type: url
  target: https://github.com/{org}/backstage-templates/blob/main/apis-location.yml

# Import commons (domains, systems, org, dependencies)
- type: url
  target: https://github.com/{org}/backstage-templates/blob/main/domains-location.yml
- type: url
  target: https://github.com/{org}/backstage-templates/blob/main/systems-location.yml
- type: url
  target: https://github.com/{org}/backstage-templates/blob/main/org-location.yml
- type: url
  target: https://github.com/{org}/backstage-templates/blob/main/dependencies-location.yml
```

### Entity Relationships

- **Components** belong to **Systems**
- **Systems** belong to **Domains**
- **Components** provide **APIs**
- **Components** depend on **Resources** (dependencies)
- **APIs** have **TechDocs** with OpenAPI specs

## 🛠️ Technology Stack

### Spring Boot Templates
- Java 21
- Spring Boot 3.2.5
- Spring MVC
- JPA/Hibernate
- PostgreSQL 42.7.3
- H2 2.2.224
- MapStruct 1.5.5.Final
- Lombok 1.18.30
- SpringDoc OpenAPI 2.1.0
- JaCoCo 0.8.11

### Spring WebFlux Templates
- Java 21
- Spring Boot 3.2.5
- Spring WebFlux 3.2.5
- Spring Data R2DBC 3.2.5
- R2DBC PostgreSQL 1.0.4.RELEASE
- R2DBC H2 1.0.0.RELEASE
- MapStruct 1.5.5.Final
- Lombok 1.18.30
- SpringDoc WebFlux 2.1.0
- Reactor Test 3.6.5

## 📝 Generated Project Structure

```
generated-project/
├── src/main/java/{groupId}/{serviceName}/
│   ├── application/
│   │   ├── dto/
│   │   ├── mapper/
│   │   └── service/
│   ├── domain/
│   │   ├── model/
│   │   └── ports/
│   │       ├── input/
│   │       └── output/
│   ├── infrastructure/
│   │   ├── adapters/
│   │   │   ├── input/rest/
│   │   │   └── output/persistence/
│   │   └── config/
│   └── {ServiceName}Application.java
├── src/test/java/
├── Dockerfile
├── docker-compose.yml
├── catalog-info.yml
├── pom.xml
└── README.md
```

## 🤝 Contributing

Templates are automatically generated from Smithy service definitions using the code generation pipeline.

## 📄 License

MIT
