# Escenarios de calidad

## Introducción

Los escenarios de calidad permiten evaluar si la arquitectura satisface los atributos priorizados durante el análisis.

Cada escenario describe una situación esperada y la respuesta del sistema.

---

## Escenario 1 — Modificabilidad

**Fuente:** Desarrollador

**Estímulo:** Cambio en la legislación laboral.

**Respuesta esperada:**

El sistema permite actualizar los parámetros correspondientes sin afectar otros módulos.

---

## Escenario 2 — Rendimiento

**Fuente:** Usuario.

**Estímulo:** Consulta simultánea de información por múltiples usuarios.

**Respuesta esperada:**

La aplicación mantiene tiempos de respuesta aceptables.

---

## Escenario 3 — Seguridad

**Fuente:** Usuario no autorizado.

**Estímulo:** Intento de acceder a información protegida.

**Respuesta esperada:**

El sistema rechaza la operación y registra el evento.

---

## Escenario 4 — Disponibilidad

**Fuente:** Usuario.

**Estímulo:** Registro de asistencia durante la jornada laboral.

**Respuesta esperada:**

La aplicación permanece disponible y registra correctamente la información.

---

## Escenario 5 — Mantenibilidad

**Fuente:** Equipo de desarrollo.

**Estímulo:** Incorporación de un nuevo módulo.

**Respuesta esperada:**

La nueva funcionalidad puede integrarse sin afectar los módulos existentes.
