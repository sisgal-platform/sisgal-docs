# Arquitectura del Backend

## Introducción

El backend de SISGAL se compone de dos servicios: el **backend core**, que implementa la lógica principal de negocio y la API REST consumida por el frontend, y un **microservicio de integración biométrica**, dedicado a la conexión con el dispositivo. El core fue desarrollado con **NestJS**, cuya organización modular y el uso de inyección de dependencias facilitan la mantenibilidad y evolución de sus funcionalidades.

La decisión de monolito modular aplica únicamente al core; el servicio de integración es independiente.

---

## Principios de diseño

El backend core fue diseñado siguiendo los siguientes principios:

- Separación de responsabilidades.
- Bajo acoplamiento entre módulos.
- Alta cohesión.
- Inversión de dependencias.
- Encapsulamiento de reglas de negocio.
- Reutilización de componentes.

---

## Organización del sistema

El backend core adopta una arquitectura de monolito modular. Sus módulos funcionales incluyen autenticación, empleados, asistencia, jornadas laborales, nómina y configuración.

Cada módulo contiene sus controladores, casos de uso, servicios, entidades, repositorios y DTOs, según corresponda a su responsabilidad.

Se propone implementar un módulo transversal de auditoría reutilizable en el sistema. Su alcance, los eventos que registrará y la conexión con la base de datos de auditoría están pendientes de definición; la documentación no lo presenta como una funcionalidad ya implementada.

---

## Persistencia

La arquitectura contempla dos bases de datos independientes, ambas PostgreSQL: la base principal para los datos del sistema y las marcaciones biométricas, y una base de auditoría cuyo uso está por definir. La persistencia del core se implementa mediante TypeORM.

El acceso a la base principal se encuentra encapsulado en la capa de infraestructura, evitando dependencias directas desde la lógica del negocio.

---

## Comunicación

La comunicación entre el frontend y el backend core se realiza mediante una API REST utilizando JSON.

El microservicio de integración recibe las marcaciones del dispositivo biométrico y las registra en la base de datos principal. El servicio es independiente del core.

---

## Seguridad

El backend core implementará mecanismos de autenticación y autorización mediante JWT.

Las operaciones del core serán protegidas utilizando Guards y Roles definidos por el sistema.

---

## Diagramas

- [Componentes del Backend Core (C4, Nivel 3)](../diagrams/components-backend.md).
- [Contenedores (C4, Nivel 2)](../diagrams/containers.md).
- [Vista de despliegue](../diagrams/deployment.md).
