# Refinamiento 01 — Sprint 06

## Información general

| Campo | Información |
|---|---|
| **Sprint** | Sprint 06 |
| **Periodo del Sprint** | 19/10/2026 – 25/10/2026 |
| **Participantes** | Mario Ramos, Marisol Perez, Tatiana Sanchez |
| **Historias consideradas** | HU01, HU03, HU31 y HU49 |

## Objetivo del refinamiento

Revisar el alcance de las historias propuestas para el Sprint 06, identificar sus dependencias y precisar los aspectos funcionales que debían considerarse durante el desarrollo.

## Historias de usuario

### HU01 — Registrar entrada con huella

La funcionalidad se orienta a registrar la entrada del empleado mediante el mecanismo de identificación por huella. Su implementación debe considerar la identificación del empleado, la captura de la marcación y las validaciones necesarias para registrar la información correctamente.

### HU03 — Almacenar registros de asistencia automáticamente

La historia busca garantizar que los registros de asistencia se almacenen automáticamente después de su captura. Se debe mantener la asociación con el empleado y la información temporal necesaria para su consulta y procesamiento posterior.

### HU31 — Exportar nómina en formato CSV

La funcionalidad permite generar un archivo CSV con la información de nómina disponible para exportación. Se deben considerar la estructura del archivo, los encabezados, la correspondencia entre los campos y los valores exportados y la legibilidad del resultado.

### HU49 — Consultar y aceptar la política de tratamiento de datos personales

La historia contempla permitir la consulta de la política de tratamiento de datos personales y registrar su aceptación dentro del flujo correspondiente de creación del empleado.

La funcionalidad debe facilitar el acceso al texto completo de la política y asegurar que la aceptación se presente como un requisito obligatorio cuando así lo establezca el proceso definido para el sistema.

## Dependencias identificadas

| Historia | Aspectos relacionados |
|---|---|
| HU01 | Identificación del empleado y mecanismo de captura de huella. |
| HU03 | Registro de marcaciones y persistencia de los datos de asistencia. |
| HU31 | Información de nómina disponible y estructura del archivo CSV. |
| HU49 | Contenido de la política, formulario de creación del empleado y registro de aceptación. |

## Criterios de revisión

Durante la revisión de las historias se deben considerar la consistencia de los datos, el cumplimiento de los criterios de aceptación, el tratamiento de errores y la integración con las funcionalidades existentes.

## Resultado

Las cuatro historias consideradas para el Sprint 06 fueron completadas y entregadas durante la iteración.
