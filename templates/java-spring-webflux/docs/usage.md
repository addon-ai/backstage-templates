# Guía de Uso

## Crear un Nuevo Servicio

### 1. Acceder a la Plantilla
- Navega a **Crear** → **Elegir una plantilla** en Backstage
- Selecciona **Spring WebFlux Microservice**

### 2. Información del Componente
- **ID del Componente**: Identificador único (kebab-case, ej. `user-service-webflux`)
- **Descripción**: Descripción breve del servicio
- **Propietario**: Equipo o persona responsable
- **Email**: Email de contacto

### 3. Configuración Java
- **Artifact ID**: Identificador de artefacto Maven
- **Versión de Java**: 17 o 21
- **Versión de Spring Boot**: 3.2.5 o 3.3.0

### 4. Repositorio
- **URL del Repositorio**: Ubicación del repositorio en GitHub
- Debe estar bajo la organización `addon-ai`

## Proyecto Generado

### Qué se Crea
```
tu-servicio/
├── src/main/java/com/example/userservice/
├── src/test/java/
├── docs/                    # Documentación TechDocs
├── .github/workflows/       # Pipelines CI/CD
├── docker-compose.yml       # Desarrollo local
├── Dockerfile              # Imagen de contenedor
├── pom.xml                 # Configuración Maven
├── catalog-info.yml        # Metadatos de Backstage
└── README.md               # Documentación del proyecto
```

### Próximos Pasos Inmediatos
1. **Revisar la estructura del código generado**
2. **Configurar variables de entorno**
3. **Ejecutar pruebas**: `./mvnw test`
4. **Iniciar aplicación**: `./mvnw spring-boot:run`
5. **Acceder a documentación de API**: http://localhost:8080/swagger-ui.html

### Flujo de Desarrollo
1. **Desarrollo local**: Usar docker-compose para dependencias
2. **Desarrollo de features**: Crear ramas de características
3. **Pruebas**: Mantener 85% de cobertura de código
4. **Pull requests**: PR automático a rama develop
5. **Despliegue**: CI/CD maneja construcción y despliegue

## Mejores Prácticas

### Programación Reactiva
- Usar `Mono<T>` para valores únicos
- Usar `Flux<T>` para múltiples valores
- Evitar operaciones bloqueantes
- Encadenar operaciones reactivas

### Arquitectura
- Mantener la capa de dominio pura (sin dependencias externas)
- Usar patrón de puertos y adaptadores
- Implementar casos de uso en capa de aplicación
- Configurar integraciones externas en capa de infraestructura
