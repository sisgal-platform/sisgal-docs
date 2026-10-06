# Sprint 04

## Información general

| Campo | Información |
|---|---|
| **Sprint** | Sprint 04 |
| **Periodo** | 05/10/2026 – 11/10/2026 |
| **Duración** | 1 semana |
| **Estado** | En progreso |
| **Historias de usuario** | 11 |
| **Objetivo** | Parametrización y liquidación de nómina |

## Objetivo del Sprint

Desarrollar funcionalidades relacionadas con la parametrización de los conceptos de nómina y el proceso de liquidación de empleados, dando continuidad a las funcionalidades de empleados, asistencia, préstamos e incapacidades desarrolladas durante los Sprints anteriores.

El Sprint busca avanzar en la configuración de parámetros laborales y legales, así como en los cálculos requeridos para la liquidación de nómina y la consulta de sus resultados.

## Historias de usuario

### Marisol Perez

| ID | Historia de usuario | Estado |
|---|---|---|
| HU39 | Configurar parámetros de nómina - Jornada laboral | En progreso |
| HU39 | Configurar parámetros de nómina - Recargos laborales | En progreso |
| HU37 | Configurar parámetros de nómina - Descuentos legales | En progreso |

### Mario Ramos

| ID | Historia de usuario | Estado |
|---|---|---|
| HU20 | Consultar liquidaciones de empleados | En progreso |
| HU09 | Modificar horario laboral de empleado | En progreso |
| HU30 | Consulta de comprobante detallado de nómina | En progreso |

### Tatiana Sanchez

| ID | Historia de usuario | Estado |
|---|---|---|
| HU10 | Descontar cuotas de préstamos automáticamente | En progreso |
| HU14 | Clasificar tipos de horas trabajadas | En progreso |
| HU15 | Calcular auxilio de transporte | En progreso |
| HU16 | Calcular primas | En progreso |
| HU17 | Calcular deducciones legales | En progreso |

## Alcance del Sprint

El Sprint 04 comprende funcionalidades orientadas principalmente a la configuración de parámetros de nómina y al cálculo y consulta de los resultados de liquidación.

El alcance incluye:

### Parametrización de nómina

- Configuración de la jornada laboral.
- Configuración de recargos laborales.
- Configuración de descuentos legales.

### Gestión de horarios

- Modificación del horario laboral de los empleados.

### Liquidación de nómina

- Consulta de liquidaciones de empleados.
- Descuento automático de cuotas de préstamos.
- Clasificación de tipos de horas trabajadas.
- Cálculo del auxilio de transporte.
- Cálculo de primas.
- Cálculo de deducciones legales.

### Comprobantes

- Consulta del comprobante detallado de nómina.

El detalle de las tareas técnicas asociadas a cada historia será gestionado mediante Azure DevOps.

## Organización del trabajo

La asignación de historias se realizó de acuerdo con las responsabilidades definidas para cada integrante y considerando la relación entre las funcionalidades de parametrización, cálculo y consulta de nómina.

| Integrante | Historias asignadas |
|---|---|
| **Marisol Perez** | HU39 - Jornada laboral, HU39 - Recargos laborales, HU37 - Descuentos legales |
| **Mario Ramos** | HU20 - Consulta de liquidaciones, HU09 - Modificación de horario laboral, HU30 - Comprobante detallado de nómina |
| **Tatiana Sanchez** | HU10 - Descuento automático de préstamos, HU14 - Clasificación de horas, HU15 - Auxilio de transporte, HU16 - Primas, HU17 - Deducciones legales |

## Dependencias identificadas

Las historias seleccionadas presentan dependencias con funcionalidades desarrolladas durante los Sprints anteriores y entre los diferentes componentes del proceso de liquidación.

| Historia | Dependencia |
|---|---|
| HU39 - Jornada laboral | Configuración requerida para determinar la jornada de los empleados. |
| HU39 - Recargos laborales | Parámetros laborales utilizados durante la clasificación y liquidación de horas. |
| HU37 - Descuentos legales | Parámetros necesarios para calcular las deducciones de nómina. |
| HU20 | Información generada durante el proceso de liquidación de nómina. |
| HU09 | Información del empleado y configuración de horarios. |
| HU30 | Resultado de la liquidación de nómina. |
| HU10 | Préstamos registrados y cuotas pendientes de los empleados. |
| HU14 | Registros de asistencia y parámetros de jornada y recargos. |
| HU15 | Información salarial y condiciones del empleado. |
| HU16 | Información salarial y periodo de liquidación. |
| HU17 | Salario base y parámetros de descuentos legales. |

## Seguimiento

El avance del Sprint será realizado mediante reuniones Daily, en las cuales se revisarán:

- Avances realizados.
- Próximos pasos.
- Estado de las historias.
- Dependencias entre funcionalidades.
- Bloqueos o impedimentos.
- Acuerdos y acciones pendientes.

## Riesgos

- Dependencias entre las funcionalidades de parametrización y los cálculos de nómina.
- Dependencia de información de asistencia, préstamos y empleados para realizar los cálculos.
- Tiempo reducido del Sprint para completar las funcionalidades seleccionadas.
- Posibles ajustes en las reglas de negocio durante la implementación de los cálculos.

## Resultado del Sprint

> Pendiente de registrar al finalizar el Sprint.

Al finalizar el Sprint se actualizará esta sección con las historias completadas, el incremento desarrollado y los principales resultados obtenidos.

## Ceremonias

- [Refinamiento 01](refinement-01.md)
- [Planning](planning.md)
- Daily — Pendiente
- Review — Pendiente
- Retrospectiva — Pendiente

## Estado actual

**Sprint en progreso.**

El equipo inició el desarrollo de las historias seleccionadas el 05/10/2026.
