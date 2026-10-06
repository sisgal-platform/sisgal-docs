# Planning — Sprint 04

## Información general

| Campo | Información |
|---|---|
| **Fecha** | 05/10/2026 |
| **Sprint** | Sprint 04 |
| **Periodo** | 05/10/2026 – 11/10/2026 |
| **Duración** | 1 semana |
| **Duración de la sesión** | Pendiente |
| **Involucrados** | Mario Ramos, Marisol Perez, Tatiana Sanchez |

## Objetivo del Sprint

Desarrollar funcionalidades relacionadas con la parametrización de conceptos de nómina, la gestión de horarios y los cálculos requeridos para la liquidación de empleados, así como las consultas y comprobantes asociados a los resultados de nómina.

## Historias de usuario seleccionadas

### Marisol Perez

| ID | Historia de usuario | Prioridad |
|---|---|---|
| HU39 | Configurar parámetros de nómina - Jornada laboral | Alta |
| HU39 | Configurar parámetros de nómina - Recargos laborales | Alta |
| HU37 | Configurar parámetros de nómina - Descuentos legales | Alta |

### Mario Ramos

| ID | Historia de usuario | Prioridad |
|---|---|---|
| HU20 | Consultar liquidaciones de empleados | Alta |
| HU09 | Modificar horario laboral de empleado | Alta |
| HU30 | Consulta de comprobante detallado de nómina | Alta |

### Tatiana Sanchez

| ID | Historia de usuario | Prioridad |
|---|---|---|
| HU10 | Descontar cuotas de préstamos automáticamente | Alta |
| HU14 | Clasificar tipos de horas trabajadas | Alta |
| HU15 | Calcular auxilio de transporte | Alta |
| HU16 | Calcular primas | Alta |
| HU17 | Calcular deducciones legales | Alta |

## Alcance del Sprint

El alcance del Sprint 04 se concentra en avanzar en el proceso de parametrización y liquidación de nómina.

Las funcionalidades seleccionadas se agrupan de la siguiente manera:

### Parametrización

- Jornada laboral.
- Recargos laborales.
- Descuentos legales.

### Gestión de horarios

- Modificación del horario laboral de empleados.

### Cálculos de nómina

- Descuento automático de cuotas de préstamos.
- Clasificación de tipos de horas trabajadas.
- Cálculo del auxilio de transporte.
- Cálculo de primas.
- Cálculo de deducciones legales.

### Consultas

- Consulta de liquidaciones de empleados.
- Consulta del comprobante detallado de nómina.

El detalle de las tareas técnicas será gestionado mediante Azure DevOps.

## Organización del trabajo

La distribución del trabajo quedó establecida de la siguiente manera:

| Integrante | Historias asignadas |
|---|---|
| **Marisol Perez** | HU39 - Jornada laboral, HU39 - Recargos laborales, HU37 - Descuentos legales |
| **Mario Ramos** | HU20 - Consulta de liquidaciones, HU09 - Modificación de horario laboral, HU30 - Comprobante detallado de nómina |
| **Tatiana Sanchez** | HU10 - Descuento automático de préstamos, HU14 - Clasificación de horas, HU15 - Auxilio de transporte, HU16 - Primas, HU17 - Deducciones legales |

## Dependencias principales

El Sprint presenta una relación importante entre las funcionalidades de configuración y las funcionalidades de cálculo.

```text
Parámetros de nómina
        ↓
Clasificación de horas
        ↓
Cálculos de nómina
        ↓
Liquidación
        ↓
Consulta de liquidación
        ↓
Comprobante detallado
```

Además, el proceso de liquidación utiliza información proveniente de:

- Empleados.
- Horarios.
- Asistencia.
- Préstamos.
- Parámetros de nómina.

## Riesgos

- Dependencias entre historias relacionadas con parametrización y cálculo.
- Complejidad de las reglas involucradas en la liquidación de nómina.
- Dependencia de información generada en módulos desarrollados durante Sprints anteriores.
- Tiempo limitado del Sprint para completar once historias de usuario.
- Posibles ajustes en las reglas de negocio durante la implementación.

## Acuerdos

- El Sprint 04 tendrá una duración de una semana.
- Se trabajará sobre las historias seleccionadas.
- Cada integrante mantendrá las historias asignadas durante el Sprint.
- Las tareas técnicas serán gestionadas mediante Azure DevOps.
- Las dependencias entre parametrización y liquidación serán revisadas durante el desarrollo.
- Los criterios de aceptación serán utilizados como referencia para validar las funcionalidades.
- Los avances y posibles bloqueos serán registrados durante las Daily.

## Compromiso del Sprint

El equipo se compromete a trabajar durante el Sprint 04 en las siguientes funcionalidades:

### Marisol Perez

- HU39. Configurar parámetros de nómina - Jornada laboral.
- HU39. Configurar parámetros de nómina - Recargos laborales.
- HU37. Configurar parámetros de nómina - Descuentos legales.

### Mario Ramos

- HU20. Consultar liquidaciones de empleados.
- HU09. Modificar horario laboral de empleado.
- HU30. Consulta de comprobante detallado de nómina.

### Tatiana Sanchez

- HU10. Descontar cuotas de préstamos automáticamente.
- HU14. Clasificar tipos de horas trabajadas.
- HU15. Calcular auxilio de transporte.
- HU16. Calcular primas.
- HU17. Calcular deducciones legales.

## Estado inicial

Sprint iniciado el 05/10/2026.

El equipo inicia el desarrollo de las historias seleccionadas de acuerdo con la distribución establecida durante la Planning.
