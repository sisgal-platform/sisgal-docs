# Arquitectura del Backend

## Introducción

El Backend Core de SISGAL implementa la lógica principal de negocio y expone la API REST consumida por el frontend. Está desarrollado con NestJS y organizado como monolito modular. No hay un microservicio biométrico implementado.

## Principios de diseño

El backend core sigue estos principios arquitectónicos:

- Separación de responsabilidades.
- Bajo acoplamiento entre módulos.
- Alta cohesión.
- Inversión de dependencias.
- Encapsulamiento de reglas de negocio.
- Reutilización de componentes.

## Organización del sistema

El Backend Core adopta una arquitectura de monolito modular. Sus módulos funcionales documentados incluyen autenticación, empleados, asistencia, jornadas laborales, nómina y configuración.

Cada módulo puede contener controladores, casos de uso, servicios, entidades, repositorios y DTOs según la responsabilidad que refleje la implementación. Las clases concretas deben verificarse en el repositorio del core.

Se propone implementar un módulo transversal de auditoría reutilizable. Su alcance y su integración están pendientes; el modelo de datos previsto se describe en el [diagrama de base de datos](../diagrams/database.md). La base de auditoría PostgreSQL es independiente y todavía no está conectada.

## Persistencia

La base principal utiliza PostgreSQL en Supabase y el Backend Core usa TypeORM para acceder a los datos. La base independiente de auditoría también está prevista en PostgreSQL; su conexión y persistencia no están implementadas.

## Comunicación

El frontend se comunica con el Backend Core mediante una API REST que usa JSON. El frontend utiliza Supabase JS para autenticación y no accede directamente a la base de datos.

La integración con el dispositivo biométrico no se documenta como servicio independiente porque no existe un microservicio implementado. El modo de conexión del dispositivo queda pendiente de confirmar.

## Seguridad

La arquitectura contempla autenticación backend con JWT, guards y roles. Su configuración efectiva y el flujo de emisión/validación de tokens deben verificarse en el código antes de describirlos como implementados.

## Diagramas

- [Componentes del Backend Core (C4, Nivel 3)](../diagrams/components-backend.md).
- [Contenedores (C4, Nivel 2)](../diagrams/containers.md).
- [Vista de despliegue](../diagrams/deployment.md).
