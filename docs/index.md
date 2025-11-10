# Backstage Templates - Hexagonal Architecture

Colección de templates de Backstage para crear microservicios Java con Arquitectura Hexagonal (Ports and Adapters).

## 📋 Templates Disponibles

### 1. Spring Boot Service Template
- **Nombre:** `springboot-service-template`
- **Descripción:** Microservicio Java tradicional con Spring Boot
- **Arquitectura:** Hexagonal (Ports and Adapters)
- **Tecnologías:** Java, Spring Boot, Maven

### 2. WebFlux Reactive Service Template
- **Nombre:** `back-ms-movies-webflux-template`
- **Descripción:** Microservicio reactivo para gestión de películas con Spring WebFlux
- **Arquitectura:** Hexagonal (Ports and Adapters)
- **Tecnologías:** Java, Spring WebFlux, R2DBC, Maven

## 🏗️ Arquitectura Hexagonal

Los templates implementan el patrón de Arquitectura Hexagonal con las siguientes capas:

- **Domain Layer:** Lógica de negocio y entidades
- **Application Layer:** Casos de uso y puertos
- **Infrastructure Layer:** Adaptadores y configuraciones

## ⚙️ Características

### Spring Boot Service
- Java 17/21
- Spring Boot
- Maven como build tool
- Configuración básica de microservicio

### WebFlux Reactive Service
- **Java:** 17/21
- **Spring Boot:** 3.2.5/3.3.0
- **Base de Datos:** PostgreSQL, MySQL, H2
- **Migraciones:** Liquibase
- **Documentación:** Swagger/OpenAPI
- **Monitoreo:** Spring Actuator
- **Seguridad:** Spring Security (opcional)
- **CI/CD:** GitHub Actions
- **Containerización:** Docker y docker-compose
- **Cobertura de código:** Configurable (default: 85%)

## 🚀 Uso

1. Accede a Backstage
2. Ve a "Create Component"
3. Selecciona uno de los templates disponibles
4. Completa los parámetros requeridos:
   - **Component ID:** Identificador único (kebab-case)
   - **Owner:** Equipo propietario
   - **Repository URL:** URL del repositorio GitHub
   - **Configuración Java:** Group ID, versiones, etc.

## 📁 Estructura del Repositorio

```
backstage-templates/
├── catalog-info.yaml              # Registro del template collection
├── springboot-service/
│   ├── template.yaml             # Definición del template Spring Boot
│   └── skeleton/                 # Código base del template
│       ├── src/
│       ├── pom.xml
│       ├── catalog-info.yaml
│       └── ...
└── webflux-service/
    ├── template.yaml             # Definición del template WebFlux
    └── skeleton/                 # Código base del template
        ├── src/
        ├── pom.xml
        ├── catalog-info.yaml
        ├── docker-compose.yml
        └── ...
```

## 🔧 Configuración

### Parámetros del Template WebFlux

#### Información del Componente
- `component_id`: Identificador único (máx. 63 caracteres, kebab-case)
- `description`: Descripción del servicio
- `owner`: Equipo propietario
- `system`: Sistema al que pertenece
- `lifecycle`: experimental | production | deprecated

#### Configuración Java
- `groupId`: Group ID de Maven
- `artifactId`: Artifact ID de Maven
- `javaVersion`: 17 | 21
- `springBootVersion`: 3.2.5 | 3.3.0

#### Base de Datos
- `database`: PostgreSQL | MySQL | H2
- `enableLiquibase`: Habilitar migraciones

#### Características Adicionales
- `enableSwagger`: Documentación API
- `enableActuator`: Endpoints de monitoreo
- `enableSecurity`: Autenticación y autorización
- `coverageThreshold`: Umbral de cobertura (0-100%)

#### CI/CD y DevOps
- `enableGithubActions`: Pipeline CI/CD
- `enableDocker`: Containerización
- `environments`: Ambientes de despliegue

## 📝 Validaciones

- **Component ID:** Debe seguir el patrón `^[a-z0-9]([a-z0-9-]*[a-z0-9])?$`
- **Longitud máxima:** 63 caracteres
- **Formato:** kebab-case (minúsculas, números y guiones)
- **Restricciones:** No puede empezar o terminar con guión

## 🔗 Enlaces

- **Repository:** [addon-ai/backstage-templates](https://github.com/addon-ai/backstage-templates)
- **Owner:** platform-team
- **Lifecycle:** production