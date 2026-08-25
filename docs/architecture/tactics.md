# Tácticas arquitectónicas

## Introducción

Las tácticas arquitectónicas representan decisiones de diseño orientadas a satisfacer los atributos de calidad priorizados para SISGAL.

Cada táctica responde a uno o varios escenarios de calidad definidos durante el análisis arquitectónico.

---

## Modularidad

El sistema se divide en módulos funcionales independientes.

Beneficios:

- Facilita el mantenimiento.
- Reduce el acoplamiento.
- Favorece la reutilización.

---

## Inyección de dependencias

NestJS proporciona un mecanismo de inversión de dependencias que facilita la sustitución de implementaciones y simplifica las pruebas.

---

## Configuración centralizada

Los parámetros del sistema se administran desde tablas de configuración evitando modificar código para adaptar reglas laborales.

---

## Separación entre dominio e infraestructura

Las reglas de negocio permanecen independientes de la base de datos y de tecnologías externas.

---

## Validación de entrada

Toda la información recibida por la API es validada antes de ingresar al dominio.

---

## Registro y auditoría

Las operaciones críticas generan información de auditoría para facilitar la trazabilidad del sistema.

---

## Manejo de errores

Las excepciones son gestionadas mediante mecanismos centralizados para garantizar respuestas consistentes.
