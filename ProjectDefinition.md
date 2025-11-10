# Sistema Académico Riwi CodeUp – Introducción (Spring Framework)

Bienvenido al repositorio del **Sistema Académico Riwi CodeUp**, una aplicación profesional para la gestión de estudiantes, cursos y calificaciones, desarrollada con **Spring Framework** siguiendo principios de **arquitectura limpia**, **SOLID** y **DDD (Domain-Driven Design)**.

---

## 🎯 Objetivos del Módulo

- Construir una aplicación web sólida usando **Spring Framework**, aplicando los principios de diseño y buenas prácticas de ingeniería de software.  
- Comprender la estructura de proyectos profesionales basados en **Spring MVC**, **Spring Data** y **Spring Security**.  
- Implementar el patrón **arquitectura por capas**, evolucionando hacia **arquitecturas limpias (Clean Architecture / Hexagonal)**.  
- Aplicar los principios **SOLID** para lograr bajo acoplamiento y alta cohesión entre componentes.  
- Usar **Spring Data JPA** para persistencia de datos en **MySQL**.  
- Proteger la aplicación mediante **Spring Security**, controlando accesos por roles y autenticación.  
- Integrar validaciones, control de excepciones y pruebas unitarias con **JUnit**.  
- Adoptar buenas prácticas de documentación y versionamiento con **Git** y **GitFlow**.  
- Entregar un sistema funcional, bien estructurado, probado y documentado.

---

## 🧩 Enfoque del Desarrollo

El proyecto se construirá paso a paso, partiendo de una estructura base con **Spring Framework** hasta alcanzar una aplicación madura y mantenible.

1. **Configuración inicial:** creación del proyecto base, estructura de paquetes, configuración de dependencias y servidor embebido.  
2. **Modelo de dominio:** definición de entidades principales (*Estudiante, Curso, Profesor*) aplicando POO y principios **SOLID**.  
3. **Capa de persistencia:** implementación de repositorios con **Spring Data JPA** conectados a **MySQL**.  
4. **Servicios y casos de uso:** aplicación de reglas de negocio mediante servicios desacoplados.  
5. **Capa web (controladores):** exposición de endpoints REST con **Spring MVC**.  
6. **Seguridad:** integración de **Spring Security** para autenticación y autorización.  
7. **Validaciones y manejo de errores:** uso de `@Valid`, `@ControllerAdvice` y excepciones personalizadas.  
8. **Pruebas unitarias:** validación de lógica con **JUnit** y **Mockito**.  
9. **Documentación y despliegue:** guía técnica, **UML** y documentación **API**.

---

## 🏗️ Arquitectura del Sistema

El proyecto adoptará una **arquitectura limpia inspirada en DDD (Domain-Driven Design)**, estructurada de la siguiente forma:

```
com.riwi.academico
 ├─ domain/                  → Entidades, objetos de valor y servicios de dominio
 ├─ application/             → Casos de uso y lógica de negocio
 ├─ infrastructure/          → Adaptadores técnicos (JPA, seguridad, configuración)
 ├─ web/                     → Controladores y DTOs de presentación
 ├─ config/                  → Beans y configuración general
 └─ tests/                   → Pruebas unitarias e integración
```


---

## 🔁 Flujo de Dependencias

```
Controller → Service → Repository → Database
         ↘             ↑
          ↘----------↙
          Dominio y Casos de Uso
```


### Capas principales:
- **Dominio:** representa el corazón del sistema (entidades y reglas).  
- **Aplicación:** orquesta la lógica mediante casos de uso.  
- **Infraestructura:** conecta la aplicación con frameworks externos.  
- **Web:** define los endpoints y maneja las solicitudes HTTP.

---

## ⚙️ Principios Aplicados

### 🧱 Principios SOLID

| Principio | Descripción |
|------------|-------------|
| **S – Single Responsibility** | Cada clase tiene una única responsabilidad. |
| **O – Open/Closed** | El código se extiende sin modificar lo existente. |
| **L – Liskov Substitution** | Las subclases deben respetar los contratos de sus padres. |
| **I – Interface Segregation** | Interfaces pequeñas y específicas para cada necesidad. |
| **D – Dependency Inversion** | Las clases dependen de abstracciones, no de implementaciones. |

---

### 🧼 Arquitectura Limpia

- Independencia del framework: el dominio no depende de Spring ni JPA.  
- Separación por capas con dependencias unidireccionales.  
- Uso de **interfaces (puertos)** y **adaptadores (infraestructura)**.  
- Posibilidad de escalar a microservicios o integrarse con otros módulos.

---

## 🛠️ Tecnologías Principales

| Componente | Tecnología |
|-------------|-------------|
| **Framework principal** | Spring Framework 6.x |
| **Web y controladores** | Spring MVC |
| **Persistencia** | Spring Data JPA + MySQL |
| **Seguridad** | Spring Security |
| **Validaciones** | Jakarta Bean Validation |
| **Pruebas** | JUnit 5 + Mockito |
| **Documentación** | JavaDoc + UML |
| **Versionamiento** | Git + GitFlow |

---

## 💡 Buenas Prácticas

- Inyección de dependencias por **constructor**.  
- Evitar acoplamiento directo entre capas.  
- Manejo centralizado de excepciones.  
- Validación en el borde (controladores).  
- Mapeo **DTO ↔ Entidad** mediante convertidores o **MapStruct**.  
- Uso correcto de `@Service`, `@Repository`, `@Controller`.  
- Creación de pruebas unitarias para cada capa.  
- Documentación actualizada del código y endpoints.

---

## 🚀 Resultado Esperado

- Sistema académico funcional desarrollado con **Spring Framework**.  
- Arquitectura profesional basada en principios **SOLID** y **DDD**.  
- Persistencia implementada con **Spring Data JPA**.  
- Seguridad integrada con **Spring Security**.  
- Validaciones, excepciones y pruebas unitarias completas.  
- Documentación técnica y versionamiento con **GitFlow**.

---

> 💬 Este proyecto te llevará de un enfoque tradicional en Java SE a una **arquitectura empresarial sólida basada en Spring Framework**, principios de ingeniería de software y buenas prácticas de desarrollo profesional.

---
