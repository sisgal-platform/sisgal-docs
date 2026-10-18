# Arquitectura del Backend

## Introducción

El backend de SISGAL implementa la lógica de negocio relacionada con la gestión de asistencia, administración de empleados y liquidación de nómina. Fue desarrollado utilizando **NestJS**, aprovechando su arquitectura modular y el uso de inyección de dependencias para facilitar la mantenibilidad y escalabilidad del sistema.

La aplicación expone una API REST consumida por el frontend y es responsable de ejecutar todas las reglas de negocio asociadas al dominio.

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

La solución adopta una arquitectura de monolito modular.

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

La comunicación con el frontend se realiza mediante una API REST utilizando JSON.

Las integraciones con dispositivos biométricos serán realizadas mediante un servicio especializado encargado de transformar y registrar las marcaciones recibidas.

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
