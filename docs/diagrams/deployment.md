# Despliegue de los contenedores

Esta vista complementa los diagramas C4 con las plataformas de despliegue indicadas: Vercel para el frontend React y Render para ambos servicios de backend. No sustituye el [diagrama C4 de contenedores](containers.md).

![Diagrama de despliegue de SISGAL](images/deployment.svg)

[Ver fuente PlantUML](source/deployment.puml)

## Elementos de despliegue

- **Vercel:** aloja el frontend React, construido con Vite.
- **Render:** aloja el Backend Core y el microservicio de integración biométrica.
- **Base de datos principal:** PostgreSQL alojado en Supabase, según la documentación del stack.
- **Base de datos de auditoría:** PostgreSQL independiente; su plataforma de alojamiento y su integración siguen por definir.
- **Dispositivo biométrico:** envía marcaciones al microservicio de integración.

## Flujos representados

El navegador accede al frontend en Vercel. El frontend consume la API REST del Backend Core en Render. El servicio de integración, también en Render, recibe las marcaciones y las escribe en la base de datos principal; el Backend Core consulta esa misma base. La relación de auditoría se marca como propuesta y pendiente de definición.
