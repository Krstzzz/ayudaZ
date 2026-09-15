# Metodología

## Tipo de investigación

Proyecto de desarrollo tecnológico aplicado, orientado a la construcción de una plataforma web funcional que resuelve una problemática social específica (apoyo comunitario a personas de bajos recursos en SJL).

## Técnicas y herramientas

- **Lean Canvas:** empleado para la estructuración y validación rápida del modelo de negocio social, permitiendo identificar los problemas críticos de los usuarios (beneficiarios y voluntarios) y enfocar la solución tecnológica en generar impacto social medible (Maurya, 2024).
- **Prototipado en Figma:** diseño de interfaces (inicio de sesión, creación y seguimiento de actividades) validadas antes del desarrollo, priorizando accesibilidad para usuarios con distintos niveles de alfabetización digital.
- **Modelado con UML y BPMN:** diagramas de casos de uso, diagramas de secuencia y diagramas BPMN (elaborados con Draw.io y Mermaid) para representar los flujos de inicio de sesión, creación de actividades y entrega de ayuda.
- **Diagrama de arquitectura de software:** priorizado frente a un diagrama de clases tradicional, dado que el sistema involucra múltiples módulos interconectados: gestión de usuarios, solicitudes, ofertas de ayuda, verificación de beneficiarios, registro de ayudados y ranking de desempeño (Koç et al., 2021).

## Arquitectura técnica

Arquitectura desacoplada (cliente-servidor):

- **Backend:** Spring Boot (API REST), Java 21, Spring Security + JWT, Spring Data JPA, Firebase Admin SDK, desplegado con Docker en Render.
- **Frontend:** React.js + Vite, Axios, React Router, Firebase Authentication, Tailwind CSS y Bootstrap, desplegado en Netlify.
- **Base de datos:** PostgreSQL, elegida frente a MySQL, MongoDB y SQLite por su cumplimiento estricto de ACID y su capacidad de manejar consultas complejas y datos sensibles de usuarios vulnerables.

```
React (frontend) ⇄ API REST / JWT (Spring Boot) ⇄ PostgreSQL
                          │
                    Firebase Auth
```

## Instrumentos

- Repositorios de código en GitHub (`ayudaz-backend`, `AyudaZ-frontend`).
- Diagramas UML/BPMN (Draw.io, Mermaid).
- Prototipos de interfaz (Figma).
- Modelo Lean Canvas del negocio social.
