# Refinamiento 01 — Sprint 03

## Información general

| Campo | Información |
|---|---|
| **Fecha** | 28/09/2026 |
| **Sprint objetivo** | Sprint 03 |
| **Tipo** | Refinamiento |
| **Duración** | Pendiente |
| **Involucrados** | Mario Ramos, Marisol Perez, Tatiana Sanchez |

## Objetivo

Revisar las historias de usuario candidatas para el Sprint 03, validar su alcance funcional, resolver dudas generales y verificar las dependencias con las funcionalidades desarrolladas durante los Sprints anteriores.

El refinamiento permitió preparar las historias para una sesión de Planning de corta duración, en la cual se definiría el alcance definitivo y la asignación de responsables.

## Historias revisadas

| ID | Historia de usuario | Responsable propuesto | Estado |
|---|---|---|---|
| HU42 | Consultar incapacidades | Mario Ramos | Refinada |
| HU11 | Registrar préstamos a empleados | Tatiana Sanchez | Refinada |
| HU12 | Registrar incapacidades de empleados | Mario Ramos | Refinada |
| HU04 | Consultar historial de asistencia por empleado | Marisol Perez | Refinada |
| HU05 | Visualizar ingresos del día en tiempo real | Marisol Perez | Refinada |
| HU41 | Consultar préstamos de empleados | Tatiana Sanchez | Refinada |

## Dudas identificadas

Durante la revisión se verificó principalmente el alcance funcional de cada historia, la información que debía presentarse al usuario y su relación con las funcionalidades desarrolladas en Sprints anteriores.

| Historia | Duda / aspecto a aclarar | Resolución |
|---|---|---|
| HU42 | Información que debe mostrarse en la consulta de incapacidades. | Se definió que la consulta debe permitir identificar al empleado y la información relevante de cada incapacidad. |
| HU11 | Información requerida para registrar un préstamo. | Se validaron los datos necesarios para registrar el préstamo y su relación con el empleado. |
| HU12 | Información necesaria para registrar una incapacidad. | Se confirmó que el registro debe asociarse a un empleado y contener la información requerida para gestionar la novedad. |
| HU04 | Información que debe mostrarse en el historial de asistencia. | Se definió que la consulta debe permitir revisar las marcaciones e información de asistencia asociada a un empleado. |
| HU05 | Información requerida para visualizar los ingresos del día. | Se acordó mostrar la información correspondiente a las personas que ingresan durante la jornada y mantenerla disponible para consulta. |
| HU41 | Información que debe mostrarse en la consulta de préstamos. | Se confirmó que la consulta debe permitir identificar los préstamos asociados a los empleados y su estado. |

## Criterios de aceptación

Los criterios de aceptación fueron revisados para asegurar que las historias tuvieran un alcance suficientemente claro para iniciar el desarrollo.

| Historia | Ajuste realizado |
|---|---|
| HU42 | Se precisó el alcance de la consulta de incapacidades y la información que debe presentar. |
| HU11 | Se verificaron los datos requeridos para registrar préstamos asociados a empleados. |
| HU12 | Se precisó la información necesaria para registrar incapacidades de empleados. |
| HU04 | Se aclaró el alcance de la consulta del historial de asistencia por empleado. |
| HU05 | Se precisó la información que debe estar disponible para consultar los ingresos del día. |
| HU41 | Se aclaró el alcance de la consulta de préstamos de empleados. |

## Cambios realizados

Como resultado del refinamiento:

- Se aclaró el alcance funcional de las seis historias.
- Se revisaron los criterios de aceptación asociados.
- Se identificaron las relaciones entre las nuevas funcionalidades y los módulos desarrollados previamente.
- Se verificó que las historias fueran suficientemente claras para definir el alcance del Sprint 03.
- Se mantuvo la asignación de las historias de acuerdo con la disponibilidad y continuidad del trabajo del equipo.

## Dependencias identificadas

| Historia | Dependencia | Impacto |
|---|---|---|
| HU42 | Información de empleados y módulo de incapacidades. | Requiere contar con la información de empleados para realizar la consulta. |
| HU11 | Información de empleados. | El préstamo debe asociarse a un empleado existente. |
| HU12 | Información de empleados. | La incapacidad debe asociarse a un empleado existente. |
| HU04 | Registros de asistencia. | La consulta depende de la información de marcaciones almacenada. |
| HU05 | Registros de asistencia. | Requiere disponer de información actualizada de las marcaciones del día. |
| HU41 | Información de empleados y préstamos registrados. | Requiere que existan préstamos asociados a los empleados para realizar la consulta. |

## Resultado del refinamiento

Las seis historias de usuario revisadas quedaron con un alcance suficientemente definido para ser consideradas durante la Planning del Sprint 03.

El equipo acordó continuar con estas historias como candidatas para el Sprint, dejando la selección y distribución definitiva para la sesión de Planning.

## Acuerdos

- Mantener criterios de aceptación claros y verificables.
- Considerar las funcionalidades desarrolladas durante los Sprints anteriores.
- Identificar las dependencias entre las historias antes de iniciar su implementación.
- Mantener la asignación de historias de acuerdo con la disponibilidad de cada integrante.
- Gestionar las tareas técnicas asociadas a cada historia mediante Azure DevOps.

## Pendientes

| Pendiente | Responsable | Fecha |
|---|---|---|
| Definir el alcance definitivo del Sprint 03. | Equipo | 28/09/2026 |
| Confirmar responsables de las historias. | Equipo | 28/09/2026 |
