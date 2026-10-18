# Architecture Decision Records (ADR)

## Introducción

Los Architecture Decision Records (ADR) son documentos que permiten registrar las decisiones arquitectónicas relevantes tomadas durante el desarrollo de un sistema de software. Su propósito es conservar la justificación de las decisiones, las alternativas evaluadas y las consecuencias que estas generan sobre el diseño, la implementación y la evolución de la solución.

En el proyecto SISGAL, los ADR se utilizan para documentar las decisiones que orientan la construcción del Sistema de Gestión de Asistencia y Liquidación de Nómina para JS Burguer Parrilla. Estos registros contribuyen a mantener la trazabilidad de las decisiones técnicas y a facilitar su comprensión por parte de los integrantes del equipo y de quienes consulten o mantengan el sistema posteriormente.

Cada registro describe el contexto que motivó una decisión, las alternativas consideradas, la solución seleccionada y sus principales consecuencias. De esta manera, la documentación no se limita a describir las tecnologías utilizadas, sino que explica las razones que sustentan su elección.

## Decisiones arquitectónicas registradas

### ADR-001 — Monolito modular

Documenta la elección de una arquitectura de monolito modular para organizar las funcionalidades del backend de SISGAL en módulos con responsabilidades delimitadas, manteniendo una aplicación integrada y una comunicación interna directa.

### ADR-002 — PostgreSQL

Registra la selección de PostgreSQL como sistema gestor de bases de datos relacional, considerando las necesidades de persistencia, integridad y consulta de la información utilizada en los procesos de asistencia y nómina.

### ADR-003 — React

Documenta la selección de React para la construcción de la interfaz de usuario, teniendo en cuenta la organización de componentes, la reutilización de elementos visuales y la separación entre la presentación y la lógica de negocio del backend.

## Criterios de documentación

Los ADR se estructuran mediante las siguientes secciones: contexto, alternativas consideradas, decisión adoptada, justificación y consecuencias. Esta estructura permite comprender tanto la solución elegida como los factores que influyeron en la decisión.

Los registros se conservan como parte de la documentación técnica del proyecto. Si una decisión cambia de manera significativa, su justificación y sus consecuencias deberán revisarse y documentarse mediante la actualización del registro correspondiente o la creación de un nuevo ADR relacionado.

## Relación con la documentación técnica

Los ADR complementan los documentos de arquitectura, las decisiones técnicas, los diagramas y la documentación de implementación. Mientras los ADR explican por qué se seleccionó una solución, los documentos de arquitectura describen su estructura y los documentos técnicos detallan los aspectos necesarios para comprender su implementación.

## Índice de decisiones

- [ADR-001 — Monolito modular](ADR-001-modular-monolith.md)
- [ADR-002 — PostgreSQL](ADR-002-postgresql.md)
- [ADR-003 — React](ADR-003-react.md)