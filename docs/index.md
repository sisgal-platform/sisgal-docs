# SISGAL

Bienvenido a la documentación oficial de **SISGAL** (Sistema de Gestión de Asistencia y Liquidación de Nómina).

SISGAL es una plataforma web desarrollada para automatizar el registro de asistencia y el cálculo de la nómina en pequeñas y medianas empresas del sector gastronómico colombiano. El sistema integra el control de asistencia mediante dispositivos biométricos con el procesamiento automatizado de la jornada laboral, permitiendo calcular de forma precisa los diferentes conceptos asociados a la liquidación de nómina conforme a la legislación colombiana vigente.

La documentación se organiza en dos recorridos: el **manual de usuario**, centrado en las tareas realizadas desde la aplicación, y el **manual técnico**, dirigido al desarrollo y operación del sistema. La arquitectura, el dominio, la API y las decisiones técnicas se conservan dentro del recorrido técnico.

---

## Objetivos

SISGAL tiene como propósito:

- Automatizar el registro de asistencia de los empleados.
- Reducir errores en el cálculo de la nómina.
- Garantizar la trazabilidad de la información laboral.
- Facilitar el cumplimiento de la normativa laboral colombiana.
- Proporcionar una plataforma modular, mantenible y escalable.

---

## Tecnologías principales

| Componente | Tecnología |
|------------|------------|
| Frontend | React + TypeScript |
| Backend | NestJS |
| Base de datos | PostgreSQL |
| ORM | Prisma |
| Contenedores | Docker |
| Control de versiones | GitHub |
| Documentación | MkDocs Material |

---

## Documentación

- [Manual de usuario](user-guide/index.md): acceso, empleados, asistencia, nómina y reportes.
- [Manual técnico](technical-guide/index.md): entorno, configuración, operación, mantenimiento, seguridad y contribución.

Las secciones de arquitectura, dominio, API, ADR, deployment y backlog están disponibles dentro del menú **Manual técnico**.

---

## Estado del proyecto

Actualmente SISGAL se encuentra en desarrollo como parte del trabajo de grado de Ingeniería de Sistemas.

La documentación evolucionará junto con el proyecto y será actualizada conforme se incorporen nuevas funcionalidades o se tomen nuevas decisiones arquitectónicas.
