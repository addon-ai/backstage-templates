# Architecture

## Hexagonal Architecture (Ports and Adapters)

This template generates projects following the **Hexagonal Architecture** pattern.

### Generated Project Structure

```
src/main/java/com/example/service/
├── application/              # Application Layer
│   ├── dto/                 # Data Transfer Objects
│   ├── mapper/              # MapStruct mappers
│   └── service/             # Use case implementations
├── domain/                  # Domain Layer
│   ├── model/               # Domain entities
│   └── ports/               # Port interfaces
│       ├── input/           # Input ports (use cases)
│       └── output/          # Output ports (repositories)
└── infrastructure/          # Infrastructure Layer
    ├── adapters/
    │   ├── input/rest/      # REST controllers
    │   └── output/persistence/ # JPA/Hibernate repositories
    └── config/              # Configuration classes
```

### Request Flow

The generated microservice follows this flow:

```mermaid
graph TD
    A[HTTP Request] --> B[REST Controller]
    B --> C[Use Case Service]
    C --> D[Domain Service]
    D --> E[Repository Port]
    E --> F[JPA Repository]
    F --> G[PostgreSQL]
    G --> F
    F --> E
    E --> D
    D --> C
    C --> B
    B --> H[HTTP Response]
```

### Key Benefits

- **Simple**: Easy to understand and maintain
- **Reliable**: Proven patterns and practices
- **Testable**: Clean separation of concerns
- **Maintainable**: Clear architectural boundaries
- **Flexible**: Easy to change external dependencies
