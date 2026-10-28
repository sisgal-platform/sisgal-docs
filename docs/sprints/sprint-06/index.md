# Sprint 06

## Información general

| Campo | Información |
|---|---|
| **Sprint** | Sprint 06 |
| **Periodo** | 19/10/2026 – 25/10/2026 |
| **Duración** | 1 semana |
| **Estado** | Completado |
| **Historias planificadas** | 4 |
| **Historias completadas** | 4 |
| **Cumplimiento** | 100 % |
| **Objetivo** | Registro de asistencia, exportación de nómina y tratamiento de datos personales |

## Objetivo del Sprint

Implementar funcionalidades orientadas al registro de asistencia mediante huella, el almacenamiento automático de los registros de asistencia, la exportación de nómina en formato CSV y la consulta y aceptación de la política de tratamiento de datos personales.

Este Sprint amplió las capacidades de SISGAL en los procesos de asistencia y consulta de información, incorporando también la funcionalidad relacionada con el tratamiento de datos personales de los empleados.

## Historias de usuario

### Marisol Perez

| ID | Historia de usuario | Estado final |
|---|---|---|
| HU01 | Registrar entrada con huella | Completada |
| HU03 | Almacenar registros de asistencia automáticamente | Completada |

### Mario Ramos

| ID | Historia de usuario | Estado final |
|---|---|---|
| HU31 | Exportar nómina en formato CSV | Completada |

### Tatiana Sanchez

| ID | Historia de usuario | Estado final |
|---|---|---|
| HU49 | Consultar y aceptar la política de tratamiento de datos personales | Completada |

## Alcance del Sprint

El alcance del Sprint se organizó en tres áreas funcionales:

1. **Registro y almacenamiento de asistencia:** implementación del registro de entrada mediante huella y almacenamiento automático de los registros de asistencia.
2. **Exportación de nómina:** generación de archivos CSV con la información de nómina correspondiente.
3. **Tratamiento de datos personales:** consulta de la política de tratamiento de datos personales y aceptación de sus condiciones por parte del usuario durante el proceso definido para el registro del empleado.

Las cuatro historias de usuario planificadas fueron completadas y entregadas durante el Sprint.

## Organización del trabajo

| Integrante | Historias completadas |
|---|---|
| **Marisol Perez** | HU01 - Registrar entrada con huella; HU03 - Almacenar registros de asistencia automáticamente. |
| **Mario Ramos** | HU31 - Exportar nómina en formato CSV. |
| **Tatiana Sanchez** | HU49 - Consultar y aceptar la política de tratamiento de datos personales. |

## Dependencias identificadas

| Historia | Dependencias principales |
|---|---|
| HU01 | Identificación del empleado, mecanismo de captura de huella y validaciones necesarias para registrar la entrada. |
| HU03 | Información de las marcaciones, identificación del empleado y mecanismo de almacenamiento de los registros. |
| HU31 | Información de nómina disponible y definición de los campos que se incluirán en el archivo CSV. |
| HU49 | Política de tratamiento de datos personales, acceso a su contenido y mecanismo de aceptación asociado al proceso de registro del empleado. |

## Flujo funcional de referencia

```text
Registro de asistencia
        ↓
Almacenamiento automático
        ↓
Disponibilidad de los registros
        ↓
Procesamiento y consulta de información
```

De manera complementaria, el sistema permite exportar información de nómina en formato CSV y consultar la política de tratamiento de datos personales para aceptar sus condiciones en el flujo correspondiente.

## Riesgos identificados

Durante la planificación se debían considerar posibles inconsistencias en la captura o almacenamiento de las marcaciones, problemas de formato o integridad en los archivos CSV y la necesidad de garantizar que la aceptación de la política de tratamiento de datos personales estuviera correctamente asociada al proceso de registro del empleado.

## Resultado del Sprint

El Sprint 06 finalizó con las cuatro historias de usuario completadas y entregadas. Se implementaron las funcionalidades de registro de entrada con huella, almacenamiento automático de registros de asistencia, exportación de nómina en CSV y consulta y aceptación de la política de tratamiento de datos personales.

El equipo alcanzó el 100 % de cumplimiento del alcance planificado, sin historias pendientes de traslado a la siguiente iteración.

## Indicadores de cumplimiento

| Indicador | Resultado |
|---|---|
| Historias planificadas | 4 |
| Historias completadas | 4 |
| Historias pendientes al cierre | 0 |
| Historias trasladadas al siguiente Sprint | 0 |
| Porcentaje de cumplimiento | 100 % |

## Ceremonias

- [Refinamiento 01](refinement-01.md)
- [Planning](planning.md)
- [Daily 01](dailies/2026-10-20.md)
- [Daily 02](dailies/2026-10-24.md)
- [Review](review.md)
- [Retrospectiva](retrospective.md)

## Estado final

**Sprint completado.**

El Sprint 06 se desarrolló del 19 al 25 de octubre de 2026. Las cuatro historias de usuario comprometidas fueron completadas y entregadas, alcanzando el 100 % de cumplimiento del alcance planificado.
