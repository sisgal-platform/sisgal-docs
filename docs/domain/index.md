# Dominio

La capa de dominio de SISGAL representa los conceptos, procesos y reglas de negocio relacionados con la gestión de asistencia y liquidación de nómina de los empleados de **JS Burguer Parrilla**.

Esta sección describe el comportamiento del negocio independientemente de las tecnologías utilizadas para implementar el sistema.

## Alcance del dominio

El dominio de SISGAL comprende principalmente los procesos relacionados con:

- Gestión de empleados.
- Gestión de cargos.
- Gestión de sucursales.
- Registro y consulta de asistencia.
- Gestión de novedades que afectan la nómina.
- Liquidación de nómina.
- Gestión de préstamos.
- Gestión de incapacidades.
- Generación de información asociada a la liquidación.

## Principales conceptos

| Concepto | Descripción |
|---|---|
| **Empleado** | Persona vinculada a la organización que registra asistencia y recibe una liquidación de nómina. |
| **Sucursal** | Establecimiento o ubicación donde se encuentran asignados los empleados. |
| **Cargo** | Función o posición desempeñada por un empleado dentro de la organización. |
| **Asistencia** | Información relacionada con las marcaciones de entrada y salida de un empleado. |
| **Jornada** | Periodo de trabajo realizado por un empleado. |
| **Nómina** | Proceso mediante el cual se calculan los valores que corresponden al empleado durante un periodo determinado. |
| **Préstamo** | Obligación económica adquirida por un empleado y que puede generar descuentos en nómina. |
| **Incapacidad** | Novedad asociada a la ausencia temporal de un empleado por una condición reconocida por la organización. |
| **Liquidación** | Resultado del cálculo de los conceptos que componen el pago de un empleado. |

## Procesos principales

El dominio se organiza alrededor de tres procesos principales:

### Gestión de empleados

Comprende la creación, consulta y actualización de la información de los empleados, así como su relación con cargos y sucursales.

### Gestión de asistencia

Comprende la recepción, almacenamiento y procesamiento de las marcaciones de los empleados para determinar su jornada y las novedades asociadas.

### Liquidación de nómina

Utiliza la información del empleado, la asistencia y las novedades correspondientes para calcular los conceptos de la liquidación de nómina.

## Documentación del dominio

- [Negocio](business.md)
- [Empleados](employee.md)
- [Asistencia](attendance.md)
- [Nómina](payroll.md)
- [Glosario](glossary.md)
