# Decisiones Técnicas

## 1. Introducción

Esta sección documenta las principales decisiones técnicas adoptadas durante el diseño y desarrollo de **SISGAL (Sistema de Gestión de Asistencia y Liquidación de Nómina)**, una aplicación web orientada a apoyar la administración de empleados, el registro de asistencia y el cálculo de la nómina de JS Burguer Parrilla.

El propósito de esta documentación es mantener criterios técnicos consistentes, facilitar el mantenimiento de la aplicación y proporcionar una referencia para los integrantes del equipo de desarrollo.

## 2. Objetivos

- Documentar las tecnologías utilizadas en el desarrollo de SISGAL.
- Explicar los criterios técnicos que orientan la estructura de la aplicación.
- Establecer lineamientos para implementar y mantener las funcionalidades.
- Identificar las reglas de negocio que deben respetarse en los procesos de asistencia y nómina.
- Facilitar la incorporación de nuevos desarrolladores al proyecto.

## 3. Documentos de esta sección

| Documento | Descripción |
|---|---|
| [Stack Tecnológico](technology-stack.md) | Presenta las tecnologías, herramientas y componentes utilizados en el sistema. |
| [Arquitectura](architecture-decisions.md) | Describe las decisiones relacionadas con la organización y comunicación de los componentes de SISGAL. |
| [Reglas del Negocio](business-rules.md) | Documenta las reglas funcionales que orientan los procesos de asistencia, novedades y liquidación de nómina. |

## 4. Relación con los ADR

Los documentos de esta sección complementan los registros de decisiones arquitectónicas (ADR).

Mientras que los ADR registran el contexto, las alternativas evaluadas y la justificación de una decisión arquitectónica, esta sección reúne lineamientos técnicos y reglas de implementación que sirven como referencia para el desarrollo cotidiano.

Para consultar las decisiones arquitectónicas formales, visita la sección [Architecture Decision Records (ADR)](../adr/).

## 5. Mantenimiento de la documentación

Esta documentación debe actualizarse cuando se incorporen nuevas tecnologías, se modifique la arquitectura, cambien las reglas de negocio o se adopten criterios técnicos que afecten el funcionamiento del sistema.

Las decisiones documentadas deben mantenerse alineadas con la implementación real de SISGAL. Las tecnologías o funcionalidades planeadas que aún no estén implementadas deben identificarse como pendientes y no como características finalizadas.
