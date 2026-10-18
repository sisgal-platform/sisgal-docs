# Planning — Sprint 05

## Información general

| Campo | Información |
|---|---|
| **Fecha** | 12/10/2026 |
| **Sprint** | Sprint 05 |
| **Periodo** | 12/10/2026 – 18/10/2026 |
| **Duración** | 1 semana |
| **Duración de la sesión** | Pendiente de confirmar |
| **Participantes** | Mario Ramos, Marisol Perez, Tatiana Sanchez |

## Objetivo del Sprint

Avanzar en la consolidación del proceso de nómina mediante el cálculo automático, la incorporación de los conceptos pendientes, la generación de preliquidaciones y liquidaciones definitivas, la exportación de resultados en PDF y la consulta de indicadores administrativos.

## Historias de usuario seleccionadas

### Marisol Perez

| ID | Historia de usuario | Prioridad |
|---|---|---|
| HU13 | Calcular nómina automáticamente | Alta |
| HU10 | Descontar cuotas de préstamos automáticamente | Alta |
| HU16 | Calcular primas | Alta |

### Mario Ramos

| ID | Historia de usuario | Prioridad |
|---|---|---|
| HU29 | Exportar nómina en PDF | Alta |
| HU35 | Consulta de indicadores en dashboard | Alta |

### Tatiana Sanchez

| ID | Historia de usuario | Prioridad |
|---|---|---|
| HU18 | Generar preliquidación de nómina | Alta |
| HU19 | Crear liquidación de nómina | Alta |

## Alcance del Sprint

El trabajo se concentra en el cálculo automático de nómina y la incorporación de los conceptos pendientes de préstamos y primas. Adicionalmente, se desarrollarán las funcionalidades para generar preliquidaciones y liquidaciones definitivas, exportar nómina en PDF y consultar indicadores desde el dashboard administrativo.

El alcance técnico de cada historia se desarrollará de acuerdo con sus criterios de aceptación y las tareas registradas en Azure DevOps.

## Organización del trabajo

| Integrante | Responsabilidades |
|---|---|
| **Marisol Perez** | Implementación del cálculo automático de nómina, descuento de cuotas de préstamos y cálculo de primas. |
| **Mario Ramos** | Implementación de la exportación de nómina en PDF y consulta de indicadores del dashboard. |
| **Tatiana Sanchez** | Implementación de la generación de preliquidación y creación de liquidación de nómina. |

## Dependencias principales

El cálculo automático depende de los parámetros laborales y legales, la clasificación de horas trabajadas y la información salarial y de novedades de los empleados. Los procesos de preliquidación y liquidación requieren integrar los resultados de los cálculos para construir los resultados correspondientes.

La exportación en PDF necesita disponer de la información que se presentará en el documento. Por su parte, los indicadores del dashboard requieren que los datos relevantes estén disponibles y puedan consultarse de manera consistente.

## Riesgos

Se identifican como riesgos potenciales la complejidad de integrar las reglas de cálculo, la dependencia entre preliquidación y liquidación definitiva, la validación de los valores calculados y el tiempo disponible para implementar y probar siete historias durante una semana.

## Acuerdos

El equipo trabajará sobre las historias seleccionadas, mantendrá actualizados sus estados y tareas en Azure DevOps y utilizará los criterios de aceptación para verificar los resultados. Se revisarán las dependencias entre cálculo y liquidación durante el desarrollo, y se priorizará la validación de las funcionalidades antes del cierre del Sprint.

## Compromiso del Sprint

El equipo establece como alcance comprometido las siete historias de usuario relacionadas con el cálculo de nómina, los conceptos pendientes, la generación de liquidaciones, la exportación en PDF y la consulta de indicadores.

La finalización de cada historia estará sujeta al cumplimiento de sus criterios de aceptación y a la validación de su comportamiento.

## Estado inicial

Sprint iniciado el 12/10/2026.

El equipo comienza el desarrollo de acuerdo con la distribución de responsabilidades establecida durante la Planning.
