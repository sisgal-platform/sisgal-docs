# Empleados

## Descripción

El empleado representa a una persona vinculada a **JS Burguer Parrilla** cuya información laboral es gestionada mediante SISGAL.

El empleado constituye uno de los conceptos centrales del dominio, debido a que la información registrada sobre este se utiliza en procesos como la gestión de asistencia, novedades y liquidación de nómina.

## Información del empleado

SISGAL permite gestionar información básica y laboral del empleado.

Entre los principales datos se encuentran:

| Información | Descripción |
| --- | --- |
| **Tipo de documento** | Tipo de documento de identificación del empleado. |
| **Número de documento** | Identificador único del empleado. |
| **Nombres** | Nombres del empleado. |
| **Apellidos** | Apellidos del empleado. |
| **Fecha de nacimiento** | Fecha de nacimiento del empleado. |
| **Cargo** | Cargo desempeñado por el empleado dentro de la organización. |
| **Sucursal** | Sucursal a la que se encuentra asociado el empleado. |
| **Salario base** | Valor utilizado como referencia para determinados cálculos de nómina. |
| **Auxilio de transporte** | Información relacionada con el reconocimiento del auxilio de transporte cuando corresponda. |
| **Estado** | Indica si el empleado se encuentra activo o inactivo. |

> La información exacta gestionada por el sistema puede ampliarse de acuerdo con las necesidades del negocio.

## Relaciones

El empleado se relaciona con diferentes conceptos del dominio:

```text
                  ┌─────────────┐
                  │   Cargo     │
                  └──────┬──────┘
                         │
                         │
┌─────────────┐     ┌───▼───────┐     ┌─────────────┐
│   Sucursal  │────►│ Empleado  │◄────│  Asistencia │
└─────────────┘     └─────┬─────┘     └─────────────┘
                          │
             ┌────────────┼────────────┐
             │            │            │
             ▼            ▼            ▼
        ┌─────────┐ ┌────────────┐ ┌─────────────┐
        │Préstamo │ │Incapacidad │ │   Nómina    │
        └─────────┘ └────────────┘ └─────────────┘
```

Un empleado puede:

- Estar asociado a un cargo.
- Estar asociado a una sucursal.
- Tener múltiples registros de asistencia.
- Tener préstamos registrados.
- Tener incapacidades registradas.
- Participar en diferentes procesos de liquidación de nómina.

## Gestión del empleado

La gestión de empleados contempla principalmente:

### Registro

Permite incorporar un nuevo empleado al sistema con la información requerida para su identificación y gestión laboral.

Durante el registro se debe asociar el empleado con los elementos de parametrización correspondientes, como cargo y sucursal.

### Consulta

Permite consultar la información de los empleados registrados.

La consulta puede realizarse utilizando diferentes criterios, de acuerdo con las necesidades de los usuarios administrativos.

### Visualización del detalle

Permite consultar la información completa de un empleado seleccionado, incluyendo sus datos personales y laborales.

### Actualización

Permite modificar la información del empleado cuando se presentan cambios en sus datos o condiciones laborales.

### Estado del empleado

El sistema debe permitir identificar si un empleado se encuentra activo o inactivo.

La modificación del estado debe conservar la información histórica asociada al empleado cuando esta sea necesaria para procesos posteriores.

## Empleado y asistencia

Las marcaciones de asistencia se encuentran asociadas a un empleado.

Estas marcaciones permiten obtener información relacionada con:

- Hora de entrada.
- Hora de salida.
- Jornada trabajada.
- Horas adicionales.
- Recargos aplicables.

La información de asistencia puede utilizarse posteriormente en el proceso de liquidación de nómina.

## Empleado y novedades

Las novedades representan situaciones que pueden afectar la información utilizada durante la liquidación de nómina.

Entre las novedades contempladas por SISGAL se encuentran:

- Préstamos.
- Incapacidades.
- Horas extras.
- Recargos.

Las novedades deben estar asociadas al empleado correspondiente para que puedan ser consideradas dentro de los procesos que correspondan.

## Empleado y nómina

La información del empleado constituye una entrada para el proceso de liquidación de nómina.

Entre los datos utilizados se encuentran:

- Información laboral.
- Salario base.
- Auxilio de transporte cuando corresponda.
- Información de asistencia.
- Novedades.
- Deducciones.

El resultado de la liquidación permite determinar los valores correspondientes al empleado para el periodo procesado.

## Reglas relevantes

- Cada empleado debe contar con un documento de identificación.
- El empleado debe estar asociado a un cargo.
- El empleado debe estar asociado a una sucursal.
- La información histórica relacionada con asistencia y novedades debe conservar su asociación con el empleado.
- Un empleado inactivo no debe ser considerado como un nuevo empleado para procesos futuros, pero su información histórica debe permanecer disponible cuando sea necesaria.
