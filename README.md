# Ruta Avanzada Spring Boot – Arquitectura por Capas → Hexagonal (REST Only)

**Duración**: 7 semanas  
**Dedicación**: 3 días por semana, 3 horas por día  
**Metodología**: 60% práctica, 40% teoría  
**Enfoque**: Construcción progresiva de un Monolito Modular Hexagonal con REST, Seguridad, Testing y Deploy en Docker.  
**Descripción**: El estudiante inicia con arquitectura por capas tradicional y migra progresivamente a Hexagonal, asegurando comprensión conceptual y técnica del por qué de la evolución.

## Semana 1 — Spring Boot Core + REST + Arquitectura por Capas

### Objetivo Principal
Comprender responsabilidades por capa y diseñar servicios REST iniciales con buenas prácticas.

### Contenido Detallado
- Creación de aplicaciones con **Spring Initializr** (Starters)
- Componentes base: **Controller**, **Service**, **Repository**
- Inversión de Control (IoC) y **Dependency Injection** (DI)
- `@RestController`, mapeo de rutas, métodos HTTP, **ResponseEntity**
- Gestión de propiedades por entorno (perfiles dev/test)
- Generación de documentación con **OpenAPI/Swagger**
- Diseño básico de **DTOs** para entrada/salida de datos

### Resultados Esperados
- CRUD básico en memoria para recurso **Usuario**
- API documentada y navegable en **Swagger UI**
- Paquetización aplicando arquitectura por capas clásica

### Historia de Usuario Semanal
- Exponer endpoints de creación, actualización, consulta y eliminación.

---

## Semana 2 — Persistencia JPA + Validación REST + Manejo de Errores Básico

### Objetivo Principal
Agregar persistencia real y reforzar calidad de REST aplicando validaciones.

### Contenido Detallado
- **Spring Data JPA** + **H2** para persistencia en ambiente dev
- Relaciones simples y consultas básicas
- Uso correcto de códigos **HTTP** en respuestas
- **Bean Validation**: `@Valid`, `@NotNull`, `@Email`, anotaciones compuestas
- **Lombok** como acelerador de boilerplate
- Introducción al manejo de errores con `@ExceptionHandler`
- Paginación con **Pageable**

### Resultados Esperados
- CRUD persistido en base de datos real
- Validaciones aplicadas en nivel **DTO** con mensajes claros
- API paginada y parametrizable

### Historia de Usuario Semanal
- Ajustar endpoints con validación estricta y paginación implementada.

---

## Semana 3 — Introducción a Arquitectura Hexagonal (Ports & Adapters)

### Objetivo Principal
Separar el núcleo de negocio de los frameworks para mejorar flexibilidad y mantenibilidad.

### Contenido Detallado
- Motivación arquitectónica: problemas del modelo por capas tradicional
- Conceptos claves: **Dominio**, **Aplicación** (Use Cases), **Puertos** y **Adaptadores**
- Diseño de puertos de entrada (REST) y salida (persistencia)
- Reorganización del proyecto en paquetes hexagonales
- Uso de **MapStruct** como mapeador recomendado
- Testeo del dominio sin necesidad de base de datos

### Resultados Esperados
- Proyecto refactorizado sin romper la API existente
- Independencia del dominio respecto a tecnología de persistencia o web
- Primeros tests de dominio

### Historia de Usuario Semanal
- Refactor total hacia arquitectura **Hexagonal** con equivalencia funcional.

---

## Semana 4 — JPA/Hibernate Avanzado + Transaccionalidad + Optimización de Consultas

### Objetivo Principal
Optimizar el acceso a datos y las operaciones transaccionales dentro de la arquitectura Hexagonal.

### Contenido Detallado
- Relaciones **JPA**: OneToMany, ManyToOne, ManyToMany
- **Lazy vs Eager**, ciclo de vida de entidades y gestión de N+1
- Consultas **JPQL** y **Specifications**
- Uso correcto de `@Transactional` en capa de aplicación
- Introducción a migraciones de base de datos con **Flyway**

### Resultados Esperados
- Reducción de N+1 y consultas pesadas
- Migraciones versionadas y ambientes reproducibles

### Historia de Usuario Semanal
- Administración de tarea por usuario con relación persistente y optimizada.

---

## Semana 5 — Validación Avanzada + Exception Handling Global + Contratos de Error REST

### Objetivo Principal
Diseñar un esquema de errores estandarizado y mantenible compatible con clientes REST.

### Contenido Detallado
- **Bean Validation** avanzada: validaciones cruzadas, grupos
- Manejo global de errores con `@ControllerAdvice`
- **ProblemDetail** (RFC 7807) como estándar de error
- Inclusión de **traceId** y **timestamps** en respuesta
- Logging estructurado para observabilidad

### Resultados Esperados
- Contrato de error consistente, documentado y consumible por clientes
- Mayor resiliencia y mantenibilidad de la API

### Historia de Usuario Semanal
- Aplicar contratos de error uniformes en todos los recursos expuestos.

---

## Semana 6 — Seguridad en REST: Spring Security + JWT + Roles (RBAC)

### Objetivo Principal
Habilitar seguridad robusta con autenticación stateless y control de acceso por rol.

### Contenido Detallado
- Configuración moderna usando **SecurityFilterChain**
- Registro/autenticación y generación de **JWT**
- Protección basada en roles y permisos (`@PreAuthorize`)
- **CORS** y políticas de seguridad REST
- Encriptación de contraseñas con **PasswordEncoder**

### Resultados Esperados
- API protegida por **JWT** y rutas limitadas por rol
- Seguridad por capas: Web + Aplicación + Dominio

### Historia de Usuario Semanal
- Autenticación completa y protección de endpoints críticos.

---

## Semana 7 — Testing, Observabilidad y Despliegue en Docker

### Objetivo Principal
Garantizar calidad del sistema y facilitar operación/despliegue en entornos reales.

### Contenido Detallado
- Pruebas Unitarias con **JUnit** y **Mockito**
- Pruebas de Integración con **Spring Boot Test**
- **Testcontainers** para pruebas con DB real
- **Actuator** y **Micrometer** para métricas
- Construcción de **Dockerfile** multi-stage
- Orquestación básica con **docker-compose**

### Resultados Esperados
- Monolito hexagonal listo para ser entregado a operaciones
- Tests mínimos que validan casos de uso críticos
- Entorno ejecutable con un solo comando

### Historia de Usuario Semanal
- Ejecutar tests + levantar stack completo con **docker-compose**.

---
