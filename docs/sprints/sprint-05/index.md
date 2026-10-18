# Sprint 05

## Información general

| Campo | Información |
|---|---|
| **Sprint** | Sprint 05 |
| **Periodo** | 12/10/2026 – 18/10/2026 |
| **Duración** | 1 semana |
| **Estado** | En progreso |
| **Historias planificadas** | 7 |
| **Objetivo** | Cálculo automático y consolidación de nómina |

## Objetivo del Sprint

Desarrollar funcionalidades orientadas al cálculo automático de nómina, la gestión de conceptos pendientes y la generación de resultados de liquidación. Asimismo, se busca incorporar mecanismos para exportar la información de nómina en formato PDF y consultar indicadores relevantes mediante el dashboard administrativo.

Este Sprint da continuidad a las funcionalidades de parametrización y cálculo desarrolladas en las iteraciones anteriores, incorporando las historias pendientes relacionadas con el descuento automático de cuotas de préstamos y el cálculo de primas, además de avanzar en la generación de preliquidaciones y liquidaciones definitivas.

## Historias de usuario

### Marisol Perez

| ID | Historia de usuario | Estado inicial |
|---|---|---|
| HU13 | Calcular nómina automáticamente | Pendiente |
| HU10 | Descontar cuotas de préstamos automáticamente | Pendiente, trasladada del Sprint 04 |
| HU16 | Calcular primas | Pendiente, trasladada del Sprint 04 |

### Mario Ramos

| ID | Historia de usuario | Estado inicial |
|---|---|---|
| HU29 | Exportar nómina en PDF | Pendiente |
| HU35 | Consulta de indicadores en dashboard | Pendiente |

### Tatiana Sanchez

| ID | Historia de usuario | Estado inicial |
|---|---|---|
| HU18 | Generar preliquidación de nómina | Pendiente |
| HU19 | Crear liquidación de nómina | Pendiente |

## Alcance del Sprint

El alcance se organiza en cuatro áreas funcionales. La primera comprende el cálculo automático de nómina y la incorporación de los conceptos que quedaron pendientes en la iteración anterior. La segunda corresponde a la generación de preliquidaciones y liquidaciones definitivas. La tercera incluye la exportación de los resultados de nómina en formato PDF. Finalmente, la cuarta contempla la consulta de indicadores mediante el dashboard administrativo.

## Organización del trabajo

| Integrante | Historias asignadas |
|---|---|
| **Marisol Perez** | HU13 - Cálculo automático de nómina; HU10 - Descuento automático de cuotas de préstamos; HU16 - Cálculo de primas |
| **Mario Ramos** | HU29 - Exportación de nómina en PDF; HU35 - Consulta de indicadores en dashboard |
| **Tatiana Sanchez** | HU18 - Generación de preliquidación de nómina; HU19 - Creación de liquidación de nómina |

## Dependencias identificadas

| Historia | Dependencias principales |
|---|---|
| HU13 - Calcular nómina automáticamente | Parámetros laborales y legales, clasificación de horas, información salarial, novedades y conceptos aplicables a la nómina. |
| HU10 - Descontar cuotas de préstamos automáticamente | Préstamos registrados, cuotas pendientes e información del empleado. |
| HU16 - Calcular primas | Información salarial, periodo de cálculo y reglas de negocio aplicables. |
| HU18 - Generar preliquidación de nómina | Información de asistencia, parámetros de nómina y resultados de los cálculos requeridos. |
| HU19 - Crear liquidación de nómina | Datos de la preliquidación, cálculos validados y reglas de liquidación definidas. |
| HU29 - Exportar nómina en PDF | Información de nómina disponible y estructura de los datos que deben incluirse en el documento. |
| HU35 - Consulta de indicadores en dashboard | Datos disponibles en el sistema y definición de los indicadores que se mostrarán. |

## Flujo funcional de referencia

```text
Parámetros y novedades
        ↓
Cálculo automático de nómina
        ↓
Preliquidación
        ↓
Liquidación definitiva
        ↓
Consulta y exportación de resultados
```

La consulta de indicadores constituye una funcionalidad complementaria que utiliza la información disponible en el sistema para presentar datos relevantes para la administración.

## Riesgos

Se consideran como riesgos potenciales las dependencias entre los cálculos de nómina y las funcionalidades de preliquidación y liquidación, la necesidad de validar la consistencia de los valores calculados y el tiempo disponible para completar siete historias en una semana. También será necesario verificar que la información generada pueda ser utilizada correctamente por los mecanismos de exportación y consulta de indicadores.

## Seguimiento

El seguimiento se realizará mediante las reuniones Daily previstas para el 13 y el 17 de octubre. En estas reuniones se revisarán los avances, las actividades pendientes, las dependencias entre historias y los posibles impedimentos.

## Resultado del Sprint

*Pendiente de registrar al cierre del Sprint, el 18/10/2026.*

En esta sección se documentarán las historias completadas, las funcionalidades pendientes o trasladadas, el incremento obtenido y el nivel de cumplimiento del alcance planificado.

## Ceremonias

- [Refinamiento 01](refinement-01.md)
- [Planning](planning.md)
- [Daily 01 — Martes 13/10](dailies/2026-10-13.md)
- [Daily 02 — Sábado 17/10](dailies/2026-10-17.md)
- [Review](review.md)
- [Retrospectiva](retrospective.md)

## Estado actual

**Sprint en progreso.**

El Sprint comenzó el 12/10/2026 y tiene como fecha de finalización prevista el 18/10/2026.
