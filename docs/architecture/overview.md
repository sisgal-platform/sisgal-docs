# Visión general de la arquitectura

## Introducción

SISGAL fue diseñado como una aplicación web orientada a automatizar el proceso de gestión de asistencia y liquidación de nómina para pequeñas organizaciones del sector gastronómico colombiano.

La solución integra en una única plataforma los procesos de registro de asistencia, administración de empleados y cálculo de la nómina, reduciendo la dependencia de procesos manuales y mejorando la precisión de los resultados.

---

## Estilo arquitectónico

SISGAL adopta una **arquitectura de monolito modular**, en la que el sistema se organiza mediante módulos funcionales independientes que comparten una única base de código y un único proceso de ejecución.

Cada módulo encapsula sus responsabilidades, reglas de negocio y componentes de infraestructura, favoreciendo la mantenibilidad y reduciendo el acoplamiento entre funcionalidades.

Este enfoque permite obtener muchas de las ventajas de una arquitectura modular sin asumir la complejidad operativa que implica una arquitectura basada en microservicios.

---

## Principios de diseño

Durante el diseño del sistema se definieron los siguientes principios arquitectónicos:

- Alta cohesión entre componentes de un mismo módulo.
- Bajo acoplamiento entre módulos.
- Separación entre lógica de negocio e infraestructura.
- Modularidad.
- Escalabilidad horizontal futura.
- Trazabilidad de la información.
- Seguridad desde el diseño.

---

## Organización general

El sistema se encuentra dividido en dos aplicaciones principales:

- Frontend desarrollado en React.
- Backend desarrollado en NestJS.

Ambas aplicaciones se comunican mediante una API REST.

La información es persistida en PostgreSQL mediante Prisma ORM.

---

## Arquitectura de alto nivel

> **Pendiente:** Diagrama de contexto (C4 - Nivel 1)

## Componentes principales

Actualmente el sistema está compuesto por los siguientes componentes:

| Componente | Responsabilidad |
|------------|-----------------|
| Frontend | Interfaz de usuario |
| Backend | Procesamiento de reglas de negocio |
| Base de datos | Persistencia de información |
| Servicio biométrico | Integración con dispositivos de asistencia |

## Módulos funcionales

La lógica del negocio se organiza en módulos independientes.

Entre los principales módulos se encuentran:

- Autenticación
- Empleados
- Asistencia
- Jornadas laborales
- Liquidación de nómina
- Configuración
- Auditoría

Cada módulo encapsula sus casos de uso, entidades, reglas de negocio y mecanismos de persistencia.

La comunicación entre módulos se realiza mediante interfaces bien definidas, evitando dependencias innecesarias entre ellos.

## Calidad de la arquitectura

El diseño arquitectónico fue guiado por atributos de calidad priorizados durante la etapa de análisis.

Los principales atributos considerados fueron:

- Mantenibilidad
- Seguridad
- Disponibilidad
- Rendimiento
- Escalabilidad
- Modificabilidad

Estos atributos dieron origen a las tácticas arquitectónicas implementadas y a las decisiones de diseño descritas en las siguientes secciones.