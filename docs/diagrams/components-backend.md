# Componentes del Backend Core (C4, Nivel 3)

Este diagrama amplía el único backend implementado en SISGAL: el Backend Core, organizado como monolito modular. La integración con el dispositivo biométrico no está implementada.

![Diagrama de componentes del Backend Core](images/components-backend.svg)

[Ver fuente PlantUML](source/components-backend.puml)

## Componentes

- **API Controllers:** expone los endpoints REST que consume el frontend.
- **Auth Module:** gestiona autenticación y autorización según la estructura documentada.
- **Attendance Module:** consulta y gestiona la asistencia.
- **Payroll Module:** calcula la nómina.
- **Configuration Module:** gestiona la configuración y las reglas.
- **Audit Module (propuesto):** módulo transversal cuya implementación e integración están pendientes.

## Flujo de datos

El Backend Core atiende las solicitudes REST del frontend y usa la base principal PostgreSQL para las operaciones del sistema. El frontend usa Supabase JS para autenticación y no accede directamente a la base de datos.

El diseño de auditoría se describe en [Modelo de datos de auditoría](database.md), pero la base independiente aún no está conectada y no se dibuja persistencia activa desde el módulo propuesto.

No se representa una base de integración biométrica ni un Attendance Processor. Tampoco se representa un servicio biométrico independiente, porque esa integración no está implementada.
