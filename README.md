# Ayuda Z

Sistema Web de Apoyo Comunitario para Personas de Bajos Recursos del Distrito de San Juan de Lurigancho (SJL)

## Información General del Proyecto

- **Título del proyecto:** Ayuda Z — Sistema Web de Apoyo Comunitario para Personas de Bajos Recursos del Distrito de SJL
- **Curso:** Herramientas de Desarrollo
- **Universidad / Facultad:** Facultad de Ingeniería
- **Docente:** Cristian Arce Villanueva
- **Integrantes:**
  - Amanqui Nuñez, Junior Nahuel
  - Camargo Vargas, Gabriel Omar
  - Garcia Florian, Mariano
  - Miranda Saturno, Ivan David
  - Zúñiga Ocrospoma, Christopher
- **Sección:** 38211
- **Lugar:** Lima, Perú — San Juan de Lurigancho, 2026
- **Fecha de inicio:** _(completar)_
- **Fecha de finalización:** _(completar)_

## Agradecimiento y Dedicatoria

Agradecemos en primer lugar a nuestras familias por el apoyo, la confianza y la motivación brindada durante nuestra formación académica. Agradecemos también a nuestro profesor, Cristian Arce Villanueva, por su orientación y los conocimientos compartidos durante el desarrollo de este trabajo, así como a todos los integrantes del equipo por el esfuerzo y compromiso puesto en el proyecto.

Dedicamos este trabajo a las personas y familias de bajos recursos del distrito de San Juan de Lurigancho, razón principal por la que nace Ayuda Z: una iniciativa que busca usar la tecnología para facilitar la solidaridad y generar un apoyo más organizado entre quienes necesitan ayuda y quienes están dispuestos a brindarla.

## Resumen

El presente proyecto propone el diseño y desarrollo de "Ayuda Z", una plataforma web orientada a optimizar el apoyo comunitario hacia personas de bajos recursos del distrito de San Juan de Lurigancho (SJL). El sistema conecta de manera organizada, segura y transparente a beneficiarios en situación de pobreza o pobreza extrema con voluntarios dispuestos a colaborar en tareas cotidianas (limpieza, transporte, mudanzas y mandados). Incorpora un módulo de verificación socioeconómica (apoyado en SISFOH) que prioriza la ayuda según el nivel de vulnerabilidad, además de un sistema de seguimiento de solicitudes y calificación bidireccional entre usuarios. El desarrollo técnico se sustenta en una arquitectura desacoplada con **Spring Boot** (backend), **React.js** (frontend) y **PostgreSQL** (base de datos relacional), validada mediante metodología **Lean Canvas** y prototipado en **Figma**.

## Abstract

This project proposes the design and development of "Ayuda Z," a web platform aimed at optimizing community support for low-income residents of the San Juan de Lurigancho (SJL) district. The system connects beneficiaries facing poverty or extreme poverty with volunteers willing to help with everyday tasks (cleaning, transportation, moving, and errands) in an organized, secure, and transparent way. The platform includes a socioeconomic verification module (supported by SISFOH), a request-tracking system, and two-way rating between users. The technical development is built on a decoupled architecture using Spring Boot (backend), React.js (frontend), and PostgreSQL (database), validated through the Lean Canvas methodology and prototyped in Figma.

## Palabras clave

Apoyo comunitario, voluntariado, pobreza, inclusión social, plataforma web, Spring Boot, React, PostgreSQL, SISFOH.

## Realidad Problemática

Los residentes de SJL en situación de pobreza o pobreza extrema enfrentan dificultades críticas para realizar tareas cotidianas esenciales (limpieza, transporte, mudanzas, mandados) por falta de recursos económicos. Existen ciudadanos con voluntad de ayudar, pero sin una herramienta que les permita identificar solicitudes reales y cercanas, lo que reduce el impacto de la solidaridad comunitaria. Además, la ausencia de mecanismos de validación formal impide verificar la condición social de los solicitantes y priorizar la ayuda según niveles socioeconómicos. Ver detalle en [`docs/01_justificacion.md`](docs/01_justificacion.md).

## Objetivo general y específicos

Ver detalle completo en [`docs/02_objetivos.md`](docs/02_objetivos.md).

## Marco teórico

Ver detalle completo en [`docs/03_marco_teorico.md`](docs/03_marco_teorico.md).

## Metodología

Ver detalle completo en [`docs/04_metodologia.md`](docs/04_metodologia.md).

## Cronograma de actividades

Ver [`docs/05_cronograma.md`](docs/05_cronograma.md).

## Desarrollo del proyecto

### Aplicación

- **Backend** (`/backend`): API REST desarrollada con Spring Boot (Java 21), Spring Security + JWT, Spring Data JPA, integración con Firebase Admin SDK, desplegado con Docker en Render.
- **Frontend** (`/frontend`): SPA desarrollada con React + Vite, Axios, React Router, Firebase Authentication, Tailwind CSS y Bootstrap, desplegada en Netlify.

Arquitectura general:

```
React (frontend) ⇄ API REST (Spring Boot) ⇄ PostgreSQL
                        │
                  Firebase Auth
```

### Base de datos

Modelo relacional en PostgreSQL con las tablas: `usuarios`, `ayudados`, `verificacion_pobreza`, `solicitudes`, `ofertas_ayuda`, `ranking_mensual`, `logs_admin`. PostgreSQL fue elegido frente a MySQL, MongoDB y SQLite por su cumplimiento estricto de ACID y su capacidad de manejar consultas complejas y datos sensibles de usuarios vulnerables.

## Resultados

Ver [`docs/06_resultados_y_conclusiones.md`](docs/06_resultados_y_conclusiones.md).

## Estructura del repositorio

```
AyudaZ/
├── README.md
├── docs/
│   ├── 01_justificacion.md
│   ├── 02_objetivos.md
│   ├── 03_marco_teorico.md
│   ├── 04_metodologia.md
│   ├── 05_cronograma.md
│   └── 06_resultados_y_conclusiones.md
├── backend/     # API REST — Spring Boot + PostgreSQL
└── frontend/    # SPA — React + Vite
```

## Instalación rápida

### Backend

```bash
cd backend
mvn clean install
mvn spring-boot:run
```

Variables de entorno necesarias: `DB_URL`, `DB_USER`, `DB_PASSWORD`, `JWT_SECRET`, `FIREBASE_CONFIG_PATH`, `CORS_ALLOWED_ORIGINS`.

### Frontend

```bash
cd frontend
npm install
npm run dev
```

Variables de entorno necesarias: `VITE_API_URL`, `VITE_FIREBASE_API_KEY`, `VITE_FIREBASE_AUTH_DOMAIN`, `VITE_FIREBASE_PROJECT_ID`, `VITE_FIREBASE_STORAGE_BUCKET`, `VITE_FIREBASE_MESSAGING_SENDER_ID`, `VITE_FIREBASE_APP_ID`.

## Autores

Ver sección [Información General del Proyecto](#información-general-del-proyecto).
