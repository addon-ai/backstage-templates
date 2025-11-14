# Características

## Características del Proyecto Generado

### Framework Principal
- **Spring WebFlux**: Framework web reactivo
- **R2DBC**: Conectividad reactiva a base de datos
- **Spring Boot Actuator**: Verificaciones de salud y métricas
- **Spring Security**: Servidor de recursos OAuth2 opcional

### Generación de Código
- **CRUD Completo**: Operaciones completas de crear, leer, actualizar y eliminar
- **DTOs**: Objetos de petición/respuesta con Bean Validation
- **MapStruct**: Mapeo automático de entidad-DTO
- **Capa de Repositorio**: Repositorios reactivos R2DBC
- **Controladores REST**: Endpoints funcionales WebFlux

### Documentación
- **OpenAPI/Swagger**: Documentación de API autogenerada
- **TechDocs**: Documentación completa del proyecto
- **README**: Instrucciones de configuración y uso

### Pruebas
- **Pruebas Unitarias**: 100% de cobertura para lógica de negocio
- **Pruebas de Integración**: WebTestClient para pruebas de API
- **Test Containers**: Pruebas de integración con base de datos
- **JaCoCo**: Reporte de cobertura de código (umbral del 85%)

### DevOps
- **GitHub Actions**: Pipeline de CI/CD
- **Docker**: Dockerfile multi-etapa
- **Docker Compose**: Entorno de desarrollo local
- **Flyway**: Migraciones de base de datos

### Opciones de Configuración

#### Soporte de Base de Datos
- PostgreSQL (por defecto)
- MySQL
- H2 (para pruebas)

#### Características Opcionales
- **Swagger/OpenAPI**: Documentación de API (por defecto: habilitado)
- **Spring Actuator**: Monitoreo de salud (por defecto: habilitado)  
- **Spring Security**: Seguridad OAuth2 (por defecto: deshabilitado)
- **Flyway**: Migraciones de base de datos (por defecto: habilitado)

#### Ambientes
- Desarrollo local
- Pruebas
- Staging  
- Producción
