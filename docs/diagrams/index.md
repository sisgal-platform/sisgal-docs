# Diagramas

Esta sección reúne las vistas de arquitectura y los diagramas previstos de SISGAL.

## Vistas disponibles

- [Contexto (C4, Nivel 1)](context.md)
- [Contenedores (C4, Nivel 2)](containers.md)
- [Componentes (C4, Nivel 3)](components.md)
  - [Backend Core](components-backend.md)
  - [Frontend](components-frontend.md)
- [Despliegue de los contenedores](deployment.md)

## Vistas pendientes

- [Base de datos](database.md): falta incorporar y validar el esquema vigente.
- [Secuencia](sequence.md): faltan los flujos funcionales que se deben documentar.

Las vistas de componentes amplían el monolito modular del Backend Core y el frontend React. El microservicio biométrico se mantiene como servicio independiente. La vista de despliegue complementa C4 y documenta Vercel para el frontend y Render para ambos servicios de backend.
