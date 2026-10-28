# Sprint 05

## Información general

| Campo | Información |
|---|---|
| **Sprint** | Sprint 05 |
| **Periodo** | 12/10/2026 – 18/10/2026 |
| **Duración** | 1 semana |
| **Estado** | Completado |
| **Historias planificadas** | 7 |
| **Historias completadas** | 7 |
| **Cumplimiento** | 100 % |
| **Objetivo** | Cálculo automático y consolidación de nómina |

## Objetivo del Sprint

Desarrollar funcionalidades orientadas al cálculo automático de nómina, la gestión de conceptos laborales pendientes y la generación de resultados de liquidación. Asimismo, incorporar mecanismos para exportar la información de nómina en formato PDF y consultar indicadores relevantes mediante el dashboard administrativo.

Este Sprint dio continuidad a las funcionalidades de parametrización y cálculo desarrolladas en las iteraciones anteriores, incorporando las historias pendientes relacionadas con el descuento automático de cuotas de préstamos y el cálculo de primas, además de las funcionalidades de preliquidación, liquidación definitiva, exportación de resultados y consulta de indicadores.

## Historias de usuario

### Marisol Perez

| ID | Historia de usuario | Estado final |
|---|---|---|
| HU13 | Calcular nómina automáticamente | Completada |
| HU10 | Descontar cuotas de préstamos automáticamente | Completada |
| HU16 | Calcular primas | Completada |

### Mario Ramos

| ID | Historia de usuario | Estado final |
|---|---|---|
| HU29 | Exportar nómina en PDF | Completada |
| HU35 | Consulta de indicadores en dashboard | Completada |

### Tatiana Sanchez

| ID | Historia de usuario | Estado final |
|---|---|---|
| HU18 | Generar preliquidación de nómina | Completada |
| HU19 | Crear liquidación de nómina | Completada |

## Alcance del Sprint

El Sprint comprendió cuatro áreas funcionales:

1. **Cálculo de nómina:** cálculo automático e incorporación de los conceptos asociados a préstamos y primas.
2. **Procesamiento de liquidaciones:** generación de preliquidaciones y creación de liquidaciones definitivas.
3. **Generación de documentos:** exportación de información de nómina en formato PDF.
4. **Consulta de información administrativa:** visualización de indicadores mediante el dashboard.

Las siete historias de usuario planificadas fueron completadas, cubriendo el alcance establecido para la iteración.

## Organización del trabajo

| Integrante | Historias completadas |
|---|---|
| **Marisol Perez** | HU13 - Cálculo automático de nómina; HU10 - Descuento automático de cuotas de préstamos; HU16 - Cálculo de primas. |
| **Mario Ramos** | HU29 - Exportación de nómina en PDF; HU35 - Consulta de indicadores en dashboard. |
| **Tatiana Sanchez** | HU18 - Generación de preliquidación de nómina; HU19 - Creación de liquidación de nómina. |

## Dependencias identificadas

El desarrollo contempló la relación entre los parámetros laborales y legales, la clasificación de horas trabajadas, la información salarial y las novedades de los empleados.

Asimismo, la generación de preliquidaciones y liquidaciones se relacionó con los resultados de los cálculos de nómina. La exportación en PDF y los indicadores del dashboard utilizaron la información correspondiente a sus respectivas funcionalidades.

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

## Riesgos identificados

Durante la planificación se consideraron los siguientes riesgos potenciales:

- Dependencias entre los cálculos de nómina y los procesos de preliquidación y liquidación.
- Necesidad de verificar la consistencia de los valores calculados.
- Integración de los resultados con los mecanismos de exportación y consulta.
- Tiempo disponible para desarrollar y validar siete historias durante una semana.

## Resultado del Sprint

El Sprint 05 finalizó con las **7 historias de usuario completadas de las 7 planificadas**, alcanzando un cumplimiento del **100 %**.

Se completaron las funcionalidades de cálculo automático de nómina, descuento de cuotas de préstamos, cálculo de primas, generación de preliquidaciones, creación de liquidaciones, exportación de nómina en PDF y consulta de indicadores en el dashboard administrativo.

Con este resultado, el equipo completó el alcance planificado para la iteración y avanzó en la consolidación de los procesos centrales de nómina de SISGAL.

## Indicadores de cumplimiento

| Indicador | Resultado |
|---|---:|
| Historias planificadas | 7 |
| Historias completadas | 7 |
| Historias pendientes al cierre | 0 |
| Historias trasladadas al siguiente Sprint | 0 |
| Porcentaje de cumplimiento | 100 % |

El porcentaje de cumplimiento se calculó dividiendo las historias completadas entre las historias planificadas y multiplicando el resultado por cien.

## Ceremonias

- [Refinamiento 01](refinement-01.md)
- [Planning](planning.md)
- [Daily 01 — Martes 13/10](dailies/2026-10-13.md)
- [Daily 02 — Sábado 17/10](dailies/2026-10-17.md)
- [Review](review.md)
- [Retrospectiva](retrospective.md)

## Estado final

**Sprint completado.**

El Sprint 05 se desarrolló entre el 12 y el 18 de octubre de 2026. Las siete historias de usuario comprometidas fueron completadas, sin historias pendientes de traslado al siguiente Sprint.