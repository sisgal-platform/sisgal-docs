# Diagrama de contenedores (C4)

El diagrama presenta los contenedores principales de SISGAL y sus relaciones con las personas usuarias, el dispositivo biométrico y las bases de datos. El backend core es un monolito modular; el servicio biométrico es un microservicio independiente.

![Diagrama de contenedores C4 de SISGAL](images/containers.svg)

[Ver fuente PlantUML](source/containers.puml)

## Contenedores y responsabilidades

- **Frontend Web (React):** presenta la interfaz para el administrador y el empleado.
- **Backend Core (Node.js/NestJS):** expone la API REST y contiene los módulos funcionales del sistema. La arquitectura de monolito modular aplica únicamente a este servicio.
- **Servicio de Integración (Node.js/NestJS):** se comunica con el dispositivo biométrico y escribe sus marcaciones en la base de datos principal.
- **Base de datos principal (PostgreSQL/Supabase):** almacena los datos del sistema y las marcaciones biométricas.
- **Base de datos de auditoría (PostgreSQL):** es independiente de la principal. El alcance de su integración aún está por definir.
- **Dispositivo Biométrico:** genera y envía registros de asistencia.

## Relaciones principales

1. El administrador y el empleado usan el frontend.
2. El frontend consume la API REST del backend core mediante HTTPS y JSON.
3. El servicio de integración recibe marcaciones del dispositivo y las registra en la base principal.
4. El backend core consulta y administra los datos del sistema en la base principal.

> **Auditoría:** existe una base PostgreSQL independiente. Se propone incorporar un módulo de auditoría transversal en el core, pero aún no se han definido su integración ni el flujo de persistencia. Por eso, el diagrama no atribuye escrituras a la base de auditoría.

La vista de despliegue propuesta se documenta por separado en [Despliegue de los contenedores](deployment.md).
