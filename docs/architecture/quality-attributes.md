# Atributos de calidad

## Introducción

Durante el diseño de SISGAL se identificaron los atributos de calidad que mayor impacto tendrían sobre el éxito del sistema.

Estos atributos orientaron tanto las decisiones arquitectónicas como la selección de tecnologías y patrones de diseño.

---

## Mantenibilidad

El sistema debe facilitar la incorporación de nuevas funcionalidades y la modificación de reglas de negocio sin afectar el resto de la aplicación.

Para ello se priorizó:

- Modularidad.
- Bajo acoplamiento.
- Alta cohesión.
- Separación de responsabilidades.

---

## Seguridad

Debido a que SISGAL administra información laboral y datos personales, el sistema incorpora mecanismos para proteger la información mediante autenticación, autorización y control de acceso.

---

## Disponibilidad

El sistema debe permanecer operativo durante las jornadas laborales para garantizar el registro continuo de asistencia y la consulta de información.

---

## Rendimiento

Las operaciones más frecuentes deben responder en tiempos adecuados incluso cuando aumente el número de empleados registrados.

---

## Escalabilidad

La arquitectura permite incorporar nuevos módulos funcionales sin afectar la estructura existente.

---

## Modificabilidad

Las reglas laborales colombianas cambian con frecuencia.

Por esta razón el sistema fue diseñado para permitir la modificación de parámetros de negocio sin requerir cambios estructurales importantes.
