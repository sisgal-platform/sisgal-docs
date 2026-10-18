# Visión general de la arquitectura

## Introducción

SISGAL es una aplicación web orientada a automatizar la gestión de asistencia y liquidación de nómina. La solución reúne el frontend, el Backend Core y la base PostgreSQL principal alojada en Supabase.

## Estilo arquitectónico

El Backend Core adopta una arquitectura de monolito modular: sus módulos funcionales comparten una base de código y se despliegan como una aplicación integrada. Es el único backend implementado actualmente.

La integración con el dispositivo biométrico no está implementada. La arquitectura futura y el lugar de esa integración se definirán cuando se diseñe el flujo.

## Principios de diseño

Durante el diseño del sistema se definieron los siguientes principios arquitectónicos:

- Alta cohesión entre componentes de un mismo módulo.
- Bajo acoplamiento entre módulos.
- Separación entre lógica de negocio e infraestructura.
- Modularidad.
- Escalabilidad horizontal futura.
- Trazabilidad de la información.
- Seguridad desde el diseño.

## Organización general

La solución implementada contempla:

- Frontend desarrollado en React.
- Backend Core desarrollado en NestJS y organizado como monolito modular.
- Base de datos principal PostgreSQL alojada en Supabase.
- Supabase Auth para la autenticación del frontend.

El frontend se comunica con el Backend Core mediante una API REST y no accede directamente a la base de datos. La persistencia del core utiliza TypeORM.

Se prevé una base PostgreSQL independiente para auditoría y un módulo transversal reutilizable. Ninguno está conectado al sistema actualmente.

## Arquitectura de alto nivel

- [Diagrama de contexto (C4, Nivel 1)](../diagrams/context.md)
- [Diagrama de contenedores (C4, Nivel 2)](../diagrams/containers.md)
- [Componentes (C4, Nivel 3)](../diagrams/components.md)
- [Vista de despliegue prevista](../diagrams/deployment.md)

## Componentes principales

| Componente | Responsabilidad |
|---|---|
| Frontend | Interfaz de usuario; autenticación mediante Supabase Auth; consume la API del core. |
| Backend Core | API REST y lógica principal de negocio en módulos. |
| Base de datos principal | Persistencia relacional del sistema; PostgreSQL en Supabase. |
| Base de datos de auditoría | Diseño independiente en PostgreSQL, aún no conectado. |
| Integración biométrica | No implementada; flujo futuro por definir. |

## Módulos funcionales

La lógica del negocio se organiza en módulos funcionales, incluidos autenticación, empleados, asistencia, jornadas laborales, liquidación de nómina y configuración.

Se propone un módulo transversal de auditoría, pero su alcance e integración todavía están por definir.

## Calidad de la arquitectura

El diseño arquitectónico fue guiado por atributos de calidad priorizados durante la etapa de análisis. Entre ellos se encuentran mantenibilidad, seguridad, disponibilidad, rendimiento, escalabilidad y modificabilidad. Las tácticas y escenarios deben mantenerse alineados con la implementación vigente.
