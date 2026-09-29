# Planning — Sprint 02

## Información general

| Campo | Información |
|---|---|
| **Fecha** | 14/09/2026 |
| **Sprint** | Sprint 02 |
| **Duración** | 2 semanas |
| **Duración de la sesión** | Aproximadamente 1 hora |
| **Involucrados** | Mario Ramos, Marisol Perez, Tatiana Sanchez |

## Objetivo del Sprint

Avanzar en las funcionalidades de gestión de empleados y parametrización de SISGAL, incorporando el registro y consulta de empleados, el modelo de base de datos y la administración de sucursales y cargos.

## Historias de usuario seleccionadas

| ID | Historia de usuario | Responsable |
|---|---|---|
| **HU21** | Registrar empleados | Mario Ramos |
| **HU39** | Consulta de información de empleados | Mario Ramos |
| **HT** | Creación del modelo de BD | Mario Ramos |
| **HU42** | Parametrización de sucursales | Tatiana Sanchez |
| **HU40** | Detalle de un empleado | Mario Ramos |
| **HU41** | Parametrización de cargos | Marisol Perez |

## Organización del trabajo

Para evitar que un integrante trabajara simultáneamente en varias historias de usuario, se estableció una ejecución secuencial de las historias asignadas a cada integrante.

### Mario Ramos

Las historias asignadas a Mario corresponden al flujo de gestión de empleados y al soporte de persistencia requerido. Se estableció la siguiente secuencia de trabajo:

1. **HT — Creación del modelo de BD**
2. **HU21 — Registrar empleados**
3. **HU39 — Consulta de información de empleados**
4. **HU40 — Detalle de un empleado**

La secuencia se definió considerando las dependencias entre las funcionalidades: primero se requiere disponer del modelo de datos, posteriormente registrar la información de los empleados, consultar dicha información y finalmente visualizar el detalle de un empleado.

### Tatiana Sanchez

- **HU42 — Parametrización de sucursales**

### Marisol Perez

- **HU41 — Parametrización de cargos**

## Dependencias identificadas

- La creación del modelo de base de datos constituye la base para las funcionalidades relacionadas con empleados.
- El registro de empleados depende de la disponibilidad del modelo de datos requerido.
- La consulta de información de empleados depende de la existencia de información registrada.
- La visualización del detalle de un empleado depende de la disponibilidad de la información del empleado.
- La parametrización de sucursales y cargos debe permitir posteriormente su utilización dentro de los formularios y procesos relacionados con empleados.

## Acuerdos

- Mantener el alcance definido para cada historia.
- Trabajar las historias de manera secuencial cuando una misma persona tenga varias asignadas.
- Utilizar los criterios de aceptación refinados como referencia para validar el cumplimiento de cada historia.
- Registrar cualquier impedimento que pueda afectar el cumplimiento del Sprint.

## Compromiso del Sprint

El equipo se comprometió a trabajar las seis historias de usuario seleccionadas durante el Sprint, manteniendo seguimiento periódico mediante las reuniones Daily.
