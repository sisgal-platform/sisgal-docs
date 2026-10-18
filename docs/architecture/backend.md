# Arquitectura del Backend

## Introducción

El backend de SISGAL se compone de dos servicios: el **backend core**, que implementa la lógica principal de negocio y la API REST consumida por el frontend, y un **microservicio de integración biométrica**, dedicado a la conexión con el dispositivo. El core fue desarrollado con **NestJS**, cuya organización modular y el uso de inyección de dependencias facilitan la mantenibilidad y evolución de sus funcionalidades.

La decisión de monolito modular aplica únicamente al core; el servicio de integración es independiente.

---

## Principios de diseño

El backend fue diseñado siguiendo los siguientes principios:

- Separación de responsabilidades.
- Bajo acoplamiento entre módulos.
- Alta cohesión.
- Inversión de dependencias.
- Encapsulamiento de reglas de negocio.
- Reutilización de componentes.

---

## Organización del sistema

El backend core adopta una arquitectura de monolito modular.

Cada módulo representa un dominio funcional independiente.

Ejemplos de módulos:

- Autenticación
- Empleados
- Asistencia
- Jornadas laborales
- Liquidación de nómina
- Configuración
- Auditoría

Cada módulo contiene sus propios:

- Controladores
- Casos de uso
- Servicios
- Entidades
- Repositorios
- DTOs

---

## Persistencia

La persistencia de la información se implementa mediante PostgreSQL utilizando Prisma ORM.

El acceso a la base de datos se encuentra encapsulado en la capa de infraestructura, evitando dependencias directas desde la lógica del negocio.

---

## Comunicación

La comunicación entre el frontend y el backend core se realiza mediante una API REST utilizando JSON.

La conexión con el dispositivo biométrico está a cargo del microservicio de integración, independiente del core.

---

## Seguridad

El backend implementará mecanismos de autenticación y autorización mediante JWT.

Las operaciones serán protegidas utilizando Guards y Roles definidos por el sistema.

---

## Próximos diagramas

- Diagrama de componentes.
- Diagrama de paquetes.
- Diagrama de dependencias.
- Diagrama de módulos.
