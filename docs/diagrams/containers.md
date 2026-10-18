# Diagrama de contenedores (C4)

El diagrama desglosa SISGAL en los contenedores principales indicados y muestra sus conexiones con las personas usuarias, el dispositivo biométrico y las bases de datos. Este nivel explica las responsabilidades visibles de cada parte, sin detallar componentes internos de cada contenedor.

![Diagrama de contenedores C4 de SISGAL](images/containers.svg)

[Ver fuente PlantUML](source/containers.puml)

## Contenedores y responsabilidades

- **Frontend Web (React):** presenta la interfaz que usan el administrador y el empleado.
- **Backend Core (Node.js/NestJS):** concentra la lógica de negocio, la API REST y los módulos internos.
- **Servicio de Integración (Node.js/NestJS):** gestiona la comunicación con el dispositivo biométrico.
- **Base de datos (PostgreSQL/Supabase):** almacena los datos del sistema.
- **Base de datos de auditoría (PostgreSQL):** registra eventos y trazabilidad, según lo representado en el diagrama.

## Relaciones principales

1. El administrador y el empleado usan el frontend.
2. El frontend consume la API REST del backend mediante HTTPS y JSON.
3. El backend lee y escribe en la base de datos del sistema y registra eventos en la base de auditoría.
4. El servicio de integración registra asistencia y logs en las bases indicadas.
5. El dispositivo biométrico envía registros de asistencia al servicio de integración.

> **Aclaración de arquitectura:** SISGAL tiene dos servicios de backend: el backend core, organizado como monolito modular, y el microservicio independiente dedicado a la conexión con el dispositivo biométrico. El monolito modular aplica solamente al core. Queda por confirmar si la base de datos de auditoría es independiente de la base de datos del sistema.
