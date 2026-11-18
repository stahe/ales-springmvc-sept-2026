# Introducción paso a paso al framework web [Spring MVC]

**El curso: https://stahe.github.io/ales-springmvc-sept-2026/**

Autor de todo el código y del curso: **Claude** (IA de Anthropic), a petición de **Serge Tahé**, septiembre de 2026.

## Descripción general

Este curso ofrece una guía paso a paso para construir aplicaciones web con **Spring MVC** (Spring Boot 4), donde el servidor genera las páginas HTML (vistas **Thymeleaf**). Solo supone un conocimiento básico de HTTP, HTML y del lenguaje de programación Java.

Consta de dos partes:

- **28 ejemplos cortos**, cada uno centrado en un único concepto, organizados en capítulos:

| Capítulo | Contenido | Ejemplos |
|---|---|---|
| Controladores, acciones, enrutamiento | Del navegador a la acción: rutas, respuestas, redirecciones, servicios e inyección de dependencias | 01–06 |
| El modelo de la acción | Parámetros de la solicitud: enlace (binding), conversión, validación, solicitudes POST, binding personalizado | 07–12 |
| La vista y su modelo | Thymeleaf, plantillas y fragmentos, helpers, formularios, validación, Post/Redirect/Get | 13–21 |
| Internacionalización | una aplicación bilingüe (MessageSource, LocaleResolver) | 22 |
| Ámbitos de datos | beans singleton, de solicitud y prototipo; cookies | 23 |
| El ciclo de vida de la solicitud | filtros de servlet, interceptores, `@ControllerAdvice`, página de error | 24 |
| Autenticación y autorización | Spring Security, token JWT en una cookie, roles, CAPTCHA, limitación de tasa | 25–27 |
| Arquitectura en capas y acceso a datos | capas Web / Negocio / DAO, Spring Data JPA, Hibernate, MySQL, transacciones | 28 |

- **Un caso de estudio completo**: la aplicación **RdvMedecins** para programar citas en un consultorio médico. Cuenta con tres roles (administrador, médicos, pacientes), un calendario, funciones de reserva y cancelación, administración de médicos y clientes, creación de cuentas de pacientes, protección contra bots y una interfaz en francés e inglés. Cada uno de sus archivos se comenta en el curso.

## Código fuente

El código fuente se puede descargar desde el curso. Incluye:

- `exemples/`: los 28 ejemplos, un módulo Maven por carpeta;
- `rdvmedecins2-spring-mvc/`: el caso de estudio.

## Tecnologías

Java 21 · Spring Boot 4.1 (Spring MVC, Spring Security, Spring Data JPA) · Thymeleaf · Hibernate · MySQL 8 (o MariaDB) · Maven (Maven Wrapper) · Bootstrap 5.

## Requisitos previos

- un JDK 21 (por ejemplo, Eclipse Temurin);
- Visual Studio Code, con las extensiones «Extension Pack for Java» y «Spring Boot Extension Pack»;
- MySQL 8 (Laragon en Windows) o MariaDB, para el ejemplo 28 y el caso de estudio;
- curl.

Las instrucciones de instalación de estas herramientas se proporcionan en los apéndices del curso.

## Ejecución de un ejemplo o del caso de estudio

```bash
# an example (port 5000), from its directory
cd examples/01-structure
../mvnw spring-boot:run          # Windows: ..\mvnw spring-boot:run

# el caso de estudio (puerto 8081), tras crear la base de datos con database/dbrdvmedecins2.sql
cd rdvmedecins2-spring-mvc
./mvnw spring-boot:run           # Windows: mvnw spring-boot:run
```

La primera vez que se ejecuta, Maven Wrapper descarga Maven y luego las bibliotecas: es necesario estar conectado a Internet.
