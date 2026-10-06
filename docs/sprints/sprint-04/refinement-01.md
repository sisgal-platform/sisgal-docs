# Refinamiento 01 — Sprint 04

## Información general

| Campo | Información |
|---|---|
| **Fecha** | 05/10/2026 |
| **Sprint objetivo** | Sprint 04 |
| **Tipo** | Refinamiento |
| **Duración** | Pendiente |
| **Involucrados** | Mario Ramos, Marisol Perez, Tatiana Sanchez |

## Objetivo

Revisar las historias de usuario candidatas para el Sprint 04, validar su alcance funcional, identificar dependencias y aclarar los aspectos necesarios para iniciar el desarrollo de las funcionalidades relacionadas con la parametrización y liquidación de nómina.

## Historias revisadas

### Marisol Perez

| ID | Historia de usuario | Estado |
|---|---|---|
| HU39 | Configurar parámetros de nómina - Jornada laboral | Refinada |
| HU39 | Configurar parámetros de nómina - Recargos laborales | Refinada |
| HU37 | Configurar parámetros de nómina - Descuentos legales | Refinada |

### Mario Ramos

| ID | Historia de usuario | Estado |
|---|---|---|
| HU20 | Consultar liquidaciones de empleados | Refinada |
| HU09 | Modificar horario laboral de empleado | Refinada |
| HU30 | Consulta de comprobante detallado de nómina | Refinada |

### Tatiana Sanchez

| ID | Historia de usuario | Estado |
|---|---|---|
| HU10 | Descontar cuotas de préstamos automáticamente | Refinada |
| HU14 | Clasificar tipos de horas trabajadas | Refinada |
| HU15 | Calcular auxilio de transporte | Refinada |
| HU16 | Calcular primas | Refinada |
| HU17 | Calcular deducciones legales | Refinada |

## Aspectos revisados

Durante el refinamiento se revisó principalmente:

- Alcance funcional de las historias.
- Información requerida para cada funcionalidad.
- Dependencias con funcionalidades desarrolladas en Sprints anteriores.
- Relación entre los parámetros configurables y los cálculos de nómina.
- Información necesaria para consultar las liquidaciones.
- Información requerida para generar el comprobante detallado.
- Dependencias entre asistencia, préstamos, empleados y liquidación.

## Dependencias identificadas

| Funcionalidad | Dependencia |
|---|---|
| Jornada laboral | Información de horarios y configuración laboral. |
| Recargos laborales | Jornada laboral y clasificación de horas trabajadas. |
| Descuentos legales | Parámetros legales y salario del empleado. |
| Consulta de liquidaciones | Resultados generados por el proceso de liquidación. |
| Modificación de horario | Información del empleado y configuración de jornada. |
| Comprobante de nómina | Resultado detallado de la liquidación. |
| Descuento de préstamos | Préstamos y cuotas pendientes. |
| Clasificación de horas | Marcaciones de asistencia y parámetros laborales. |
| Auxilio de transporte | Información salarial y condiciones del empleado. |
| Primas | Información salarial y periodo de liquidación. |
| Deducciones legales | Salario y parámetros de descuentos legales. |

## Criterios de aceptación

Los criterios de aceptación fueron revisados con el propósito de asegurar que las historias tuvieran un alcance claro y verificable antes de iniciar el desarrollo.

Se verificó especialmente que las historias relacionadas con cálculos de nómina tuvieran definidas las entradas necesarias y el resultado esperado.

También se revisó la relación entre las historias de parametrización y las historias encargadas de utilizar dichos parámetros durante el proceso de liquidación.

## Acuerdos

- Mantener separadas las funcionalidades de configuración y las funcionalidades de cálculo.
- Utilizar los parámetros configurados como entrada para los procesos de liquidación correspondientes.
- Considerar la información generada por asistencia, empleados y préstamos como parte de las entradas requeridas para la liquidación.
- Mantener actualizados los estados de las historias y tareas en Azure DevOps.
- Identificar oportunamente cualquier dependencia que pueda afectar el desarrollo.

## Resultado del refinamiento

Las historias revisadas quedaron suficientemente definidas para ser consideradas durante la Planning del Sprint 04.

El equipo continuará con la selección y distribución definitiva del trabajo durante la sesión de Planning.

## Pendientes

| Pendiente | Responsable | Fecha |
|---|---|---|
| Definir el alcance definitivo del Sprint 04. | Equipo | 05/10/2026 |
| Confirmar responsables de las historias. | Equipo | 05/10/2026 |
| Identificar tareas técnicas asociadas a las historias. | Equipo | 05/10/2026 |
