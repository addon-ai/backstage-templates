# Arquitectura

## Arquitectura Hexagonal (Puertos y Adaptadores)

Esta plantilla genera proyectos siguiendo el patrón de **Arquitectura Hexagonal**.

### Estructura del Proyecto Generado

```
src/main/java/com/example/service/
├── application/              # Capa de Aplicación
│   ├── dto/                 # Objetos de Transferencia de Datos
│   ├── mapper/              # Mapeadores MapStruct
│   └── service/             # Implementaciones de casos de uso
├── domain/                  # Capa de Dominio
│   ├── model/               # Entidades de dominio
│   └── ports/               # Interfaces de puertos
│       ├── input/           # Puertos de entrada (casos de uso)
│       └── output/          # Puertos de salida (repositorios)
└── infrastructure/          # Capa de Infraestructura
    ├── adapters/
    │   ├── input/rest/      # Controladores REST
    │   └── output/persistence/ # Repositorios JPA/Hibernate
    └── config/              # Clases de configuración
```

### Flujo de Peticiones

El microservicio generado sigue este flujo:

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

### Beneficios Clave

- **Simple**: Fácil de entender y mantener
- **Confiable**: Patrones y prácticas probadas
- **Testeable**: Separación clara de responsabilidades
- **Mantenible**: Límites arquitectónicos claros
- **Flexible**: Fácil cambiar dependencias externas
