# Refinamiento 01 — Sprint 05

## Información general

| Campo | Información |
|---|---|
| **Sprint** | Sprint 05 |
| **Fecha** | Pendiente de confirmar |
| **Participantes** | Mario Ramos, Marisol Perez, Tatiana Sanchez |
| **Objetivo** | Revisar el alcance, los criterios de aceptación y las dependencias de las historias propuestas para el Sprint 05. |

## Objetivo del refinamiento

Analizar las historias de usuario relacionadas con el cálculo automático de nómina, la generación de liquidaciones, la exportación de resultados y la consulta de indicadores, con el propósito de aclarar su alcance y facilitar su planificación.

## Historias revisadas

Durante el refinamiento se consideran las siete historias propuestas para la iteración: HU13, HU10, HU16, HU29, HU35, HU18 y HU19.

La revisión de HU13 se centra en identificar las entradas necesarias para calcular la nómina y establecer su relación con los parámetros laborales, los recargos, las deducciones y las novedades registradas. Para HU10 y HU16 se contempla revisar las reglas pendientes correspondientes al descuento de cuotas de préstamos y al cálculo de primas, dado que ambas historias fueron trasladadas desde el Sprint 04.

En relación con HU18 y HU19, se considera necesario precisar la diferencia entre la generación de una preliquidación y la creación de una liquidación definitiva, así como la información que debe conservarse en cada etapa. Para HU29 se revisan los datos que debe contener el archivo PDF y su relación con la información de nómina disponible. Finalmente, para HU35 se contempla establecer los indicadores que se presentarán en el dashboard y verificar la disponibilidad de los datos necesarios para su consulta.

## Dependencias identificadas

Se reconoce una dependencia funcional entre los cálculos de nómina y los procesos de preliquidación y liquidación. La exportación en PDF requiere disponer de información de nómina que pueda presentarse de forma consistente, mientras que los indicadores del dashboard dependen de la disponibilidad y calidad de los datos utilizados para su construcción.

También se considera necesario mantener la coherencia con las reglas y parámetros implementados en los Sprints anteriores.

## Aspectos que deben quedar definidos

| Aspecto | Propósito |
|---|---|
| Entradas del cálculo automático | Identificar la información necesaria para procesar la nómina. |
| Reglas de préstamos y primas | Confirmar las condiciones de cálculo y los datos requeridos. |
| Diferencia entre preliquidación y liquidación | Evitar duplicidad funcional y establecer el resultado esperado de cada proceso. |
| Contenido del PDF | Determinar la información que se debe presentar y su formato. |
| Indicadores del dashboard | Precisar qué datos se mostrarán y cómo se obtendrán. |
| Validación de resultados | Establecer cómo se verificará la consistencia de los cálculos y documentos generados. |

## Acuerdos y conclusiones

Las historias se organizarán de acuerdo con las responsabilidades definidas para cada integrante. Se tendrá en cuenta la relación entre las funcionalidades de cálculo y liquidación para coordinar su integración y validación.

Las tareas técnicas específicas, los criterios de aceptación y el seguimiento de las historias se gestionarán mediante Azure DevOps.

**Duración de la sesión:** Pendiente de confirmar.