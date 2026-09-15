# AyudaZ Backend

Backend desarrollado con Spring Boot para la plataforma **AyudaZ**, una aplicación web destinada a gestionar solicitudes de ayuda social, voluntarios y beneficiarios mediante una arquitectura REST.

## Descripción

AyudaZ permite administrar usuarios, solicitudes de ayuda y procesos de validación mediante una API segura basada en JWT.

El backend implementa autenticación, autorización por roles, gestión de usuarios, registro de actividades administrativas y persistencia de datos utilizando PostgreSQL.

---

## Tecnologías

- Java 21
- Spring Boot
- Spring Security
- JWT
- Spring Data JPA
- PostgreSQL
- Firebase Admin SDK
- Maven
- Docker

---

## Funcionalidades

### Autenticación

- Registro de usuarios
- Inicio de sesión
- Autenticación mediante JWT
- Integración con Firebase Authentication
- Recuperación de sesión

### Gestión de Usuarios

- Registro de beneficiarios
- Registro de voluntarios
- Administración de usuarios
- Cambio de estados
- Suspensión y activación de cuentas

### Panel Administrativo

- Gestión de usuarios
- Gestión de solicitudes
- Registro de actividades (Logs)
- Estadísticas

### Seguridad

- Autenticación JWT
- Control de acceso por roles
- Endpoints protegidos
- Validación de permisos

---

## Arquitectura

```
Controller
    │
Service
    │
Repository
    │
PostgreSQL
```

La aplicación sigue una arquitectura basada en el patrón MVC utilizando Spring Boot.

---

## Estructura

```
src
│
├── config
├── controller
├── dto
├── model
├── repository
├── security
├── service
```

---

## Instalación

### Clonar repositorio

```bash
git clone https://github.com/usuario/ayudaz-backend.git
```

### Instalar dependencias

```bash
mvn clean install
```

### Variables de entorno

```
DB_URL=

DB_USER=

DB_PASSWORD=

JWT_SECRET=

FIREBASE_CONFIG_PATH=

CORS_ALLOWED_ORIGINS=
```

### Ejecutar

```bash
mvn spring-boot:run
```

---

## API REST

Ejemplos de endpoints

### Auth

```
POST /auth/login

POST /auth/register

POST /auth/verify
```

### Usuarios

```
GET /usuarios

GET /usuarios/{id}

POST /usuarios

PUT /usuarios/{id}

DELETE /usuarios/{id}
```

### Administración

```
GET /admin/logs

GET /admin/dashboard
```

---

## Seguridad

- Spring Security
- JWT
- Roles
- Validación de Token
- CORS
- Firebase Authentication

---

## Base de Datos

PostgreSQL

ORM utilizado:

- Spring Data JPA
- Hibernate

---

## Despliegue

Backend desplegado utilizando Docker y Render.

---

## Autor

Helson Palomino

Estudiante de Ingeniería de Software
