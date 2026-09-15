# Cronograma de Actividades

> Completar fechas reales antes de la entrega. Formato sugerido tipo Gantt en tabla.

| Fase | Actividad | Semana inicio | Semana fin | Responsable(s) |
|---|---|---|---|---|
| 1 | Levantamiento de información y realidad problemática | | | |
| 2 | Justificación y marco teórico | | | |
| 3 | Definición de objetivos | | | |
| 4 | Modelado Lean Canvas | | | |
| 5 | Prototipado en Figma | | | |
| 6 | Diagramas UML / BPMN | | | |
| 7 | Diseño de base de datos (PostgreSQL) | | | |
| 8 | Desarrollo del backend (Spring Boot) | | | |
| 9 | Desarrollo del frontend (React) | | | |
| 10 | Integración backend-frontend | | | |
| 11 | Pruebas y ajustes | | | |
| 12 | Despliegue (Render / Netlify) | | | |
| 13 | Informe final y presentación | | | |

## Diagrama de Gantt

Puede generarse a partir de esta tabla usando herramientas como GanttProject, Excel, o directamente en Mermaid dentro de este mismo archivo, por ejemplo:

```mermaid
gantt
    title Cronograma Ayuda Z
    dateFormat  YYYY-MM-DD
    section Investigación
    Justificación y marco teórico :a1, 2026-01-01, 7d
    section Diseño
    Lean Canvas y Figma           :a2, after a1, 7d
    Diagramas UML/BPMN            :a3, after a2, 7d
    section Desarrollo
    Backend Spring Boot           :a4, after a3, 14d
    Frontend React                :a5, after a3, 14d
    Integración                   :a6, after a4, 7d
    section Cierre
    Pruebas y despliegue          :a7, after a6, 7d
    Informe final                 :a8, after a7, 5d
```
