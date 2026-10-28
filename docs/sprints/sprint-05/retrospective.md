# Retrospectiva — Sprint 05

## 1. Información general

| Campo | Información |
|---|---|
| **Sprint** | Sprint 05 |
| **Periodo evaluado** | 12/10/2026 – 18/10/2026 |
| **Participantes** | Mario Ramos, Marisol Perez, Tatiana Sanchez |
| **Historias planificadas** | 7 |
| **Historias completadas** | 7 |
| **Cumplimiento** | 100 % |
| **Estado** | Sprint completado |

## 2. Objetivo de la retrospectiva

Evaluar el proceso de trabajo del equipo durante el Sprint 05, identificar los aspectos que contribuyeron al cumplimiento de los objetivos y establecer acciones de mejora para las siguientes iteraciones.

La retrospectiva se enfoca en la organización del trabajo, la distribución de responsabilidades, la coordinación entre funcionalidades relacionadas y la validación de los resultados obtenidos durante el desarrollo.

## 3. Aspectos positivos

### 3.1. Cumplimiento del alcance planificado

El equipo completó las siete historias de usuario comprometidas para el Sprint, alcanzando un cumplimiento del 100 %. Este resultado permitió avanzar en las funcionalidades centrales de cálculo y consolidación de nómina sin trasladar historias pendientes a la siguiente iteración.

### 3.2. Distribución de responsabilidades

La asignación de historias entre los integrantes permitió organizar el trabajo por funcionalidades y mantener responsables definidos para las actividades de desarrollo.

Marisol trabajó en el cálculo automático de nómina y los conceptos asociados a préstamos y primas; Mario, en la exportación de nómina en PDF y los indicadores del dashboard; y Tatiana, en la generación de preliquidaciones y liquidaciones.

### 3.3. Avance funcional del sistema

Se completaron funcionalidades que permiten avanzar desde el cálculo de los conceptos de nómina hasta la generación de resultados de liquidación y su posterior consulta.

También se completaron las historias HU10 y HU16, que habían quedado pendientes del Sprint 04, evitando que estas actividades continuaran acumulándose en el backlog de trabajo pendiente.

### 3.4. Continuidad del desarrollo

El Sprint dio continuidad a las funcionalidades de parametrización y clasificación de horas desarrolladas en iteraciones anteriores, permitiendo avanzar hacia un proceso de nómina más integrado.

## 4. Aspectos por mejorar

### 4.1. Gestión de dependencias

Las funcionalidades de cálculo, preliquidación y liquidación tienen una relación directa. Por esta razón, es importante identificar desde la planificación cuáles historias requieren resultados de otras funcionalidades y coordinar su integración oportunamente.

### 4.2. Estimación de la capacidad del equipo

El Sprint contempló siete historias en una semana. Aunque todas fueron completadas, se recomienda continuar revisando el esfuerzo requerido para cada historia y considerar las actividades de integración, pruebas y documentación al estimar la capacidad disponible.

### 4.3. Validación de las reglas de negocio

Los cálculos de nómina requieren consistencia entre la información salarial, las horas trabajadas, los recargos, las deducciones y las novedades de los empleados. Se recomienda mantener las reglas de negocio documentadas y validar los casos límite antes de considerar finalizada cada funcionalidad.

### 4.4. Seguimiento de las actividades

Mantener actualizados los estados, las tareas y los criterios de aceptación en Azure DevOps facilita conocer el avance real, detectar dependencias y conservar evidencia del trabajo realizado.

## 5. Acciones de mejora

| Acción | Propósito | Responsable |
|---|---|---|
| Revisar las dependencias técnicas y funcionales antes de iniciar cada Sprint. | Facilitar la coordinación entre historias relacionadas. | Todo el equipo |
| Incluir tareas de pruebas e integración en la estimación de las historias. | Evitar que la validación quede relegada al final de la iteración. | Todo el equipo |
| Mantener actualizados los criterios de aceptación y estados en Azure DevOps. | Mejorar la trazabilidad del trabajo. | Responsable de cada historia |
| Validar las reglas de negocio y los casos límite de los cálculos de nómina. | Reducir inconsistencias en los resultados. | Responsables de las funcionalidades de nómina |
| Revisar la capacidad disponible antes de comprometer el alcance del siguiente Sprint. | Mantener compromisos realistas y sostenibles. | Todo el equipo |

## 6. Compromisos para el Sprint 06

Para la siguiente iteración se establecen los siguientes compromisos de mejora:

1. Revisar las dependencias entre las historias antes de iniciar el desarrollo.
2. Incorporar las pruebas y la validación dentro de la planificación de cada historia.
3. Mantener actualizada la información de seguimiento en Azure DevOps.
4. Verificar la consistencia de los cálculos y resultados relacionados con la nómina.
5. Revisar el alcance propuesto y distribuir las actividades de acuerdo con la capacidad del equipo.

Estos compromisos buscan mantener el nivel de cumplimiento alcanzado y mejorar la coordinación y la calidad de los incrementos entregados.

## 7. Conclusiones

El Sprint 05 finalizó con las siete historias de usuario completadas, alcanzando un cumplimiento del 100 % del alcance planificado. Se avanzó en la consolidación de los procesos de cálculo automático, gestión de conceptos de nómina, preliquidación, liquidación, exportación en PDF y consulta de indicadores.

Como oportunidad de mejora, se destaca la importancia de coordinar las funcionalidades que dependen unas de otras, incorporar las pruebas en la estimación del trabajo y mantener una trazabilidad clara de las actividades.

Las acciones propuestas se tomarán como referencia para la planificación del Sprint 06, con el propósito de mantener la continuidad del desarrollo y fortalecer la calidad y mantenibilidad de SISGAL.
