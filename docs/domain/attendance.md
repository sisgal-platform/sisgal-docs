# Asistencia

## Descripción

La asistencia representa la información relacionada con las marcaciones de entrada y salida de los empleados de **JS Burguer Parrilla**.

SISGAL utiliza esta información para realizar el seguimiento de las jornadas laborales y generar los datos necesarios para procesos posteriores, especialmente la liquidación de nómina.

Las marcaciones son obtenidas mediante los dispositivos biométricos dispuestos en las instalaciones de la organización.

## Marcaciones

Una marcación representa el registro de un evento de asistencia realizado por un empleado.

Cada marcación debe permitir identificar como mínimo:

| Información | Descripción |
|---|---|
| **Empleado** | Empleado que realizó la marcación. |
| **Fecha** | Fecha en la que se realizó la marcación. |
| **Hora** | Hora en la que se realizó la marcación. |
| **Tipo de marcación** | Identifica si corresponde a una entrada o salida. |
| **Dispositivo** | Dispositivo biométrico que generó el registro. |
| **Sucursal** | Ubicación asociada al registro de asistencia. |

## Origen de la información

Las marcaciones son generadas mediante dispositivos biométricos ubicados en las diferentes sucursales.

El flujo general es:

```text
Empleado
    │
    ▼
Dispositivo biométrico
    │
    │ Marcación
    ▼
SISGAL
    │
    ▼
Registro de asistencia
    │
    ▼
Procesamiento
    │
    ▼
Información de jornada
```

Los registros provenientes de los dispositivos deben ser procesados por SISGAL antes de ser utilizados en los procesos de consulta y liquidación.

## Jornada laboral

A partir de las marcaciones de un empleado se obtiene la información correspondiente a su jornada laboral.

De acuerdo con los registros disponibles, se pueden determinar:

- Hora de entrada.
- Hora de salida.
- Tiempo trabajado.
- Horas adicionales.
- Condiciones asociadas a la jornada.
- Información necesaria para determinar recargos.

La determinación de estos valores depende de las reglas de negocio definidas para el sistema.

## Consulta de asistencia

SISGAL permite consultar la información de asistencia de los empleados.

Entre las consultas contempladas se encuentra el historial de asistencia por empleado, mediante el cual un usuario administrativo puede revisar los registros correspondientes a diferentes periodos.

La consulta debe permitir identificar la información relevante de cada registro y facilitar el seguimiento de la asistencia del empleado.

## Ingresos del día

SISGAL contempla la visualización de los ingresos registrados durante la jornada actual.

Esta funcionalidad permite consultar las marcaciones de entrada realizadas durante el día y disponer de información actualizada sobre los empleados que han ingresado.

El objetivo es proporcionar al usuario administrativo una vista de seguimiento de los ingresos registrados durante la jornada.

## Asistencia y nómina

La información de asistencia constituye uno de los insumos para la liquidación de nómina.

El procesamiento puede generar información relacionada con:

- Tiempo trabajado.
- Horas extras.
- Trabajo nocturno.
- Trabajo en domingos y festivos.
- Recargos aplicables.

Esta información posteriormente puede ser considerada dentro del proceso de liquidación.

```
              Marcaciones
                   │
                   ▼
             Procesamiento
                   │
                   ▼
                Jornada
                   │
          ┌────────┼────────┐
          │        │        │
          ▼        ▼        ▼
      Horas      Horas    Recargos
     trabajadas  extras
          │        │        │
          └────────┼────────┘
                   ▼
                 Nómina
```

## Relación con el empleado

Cada registro de asistencia debe estar asociado a un empleado.

Esto permite mantener el historial de las marcaciones y utilizar la información correspondiente durante las consultas y procesos de liquidación.

```
Empleado
    │
    └─── 1:N ───► Marcaciones
```

Un empleado puede tener múltiples marcaciones a lo largo del tiempo.

## Consideraciones del dominio

- Las marcaciones deben conservar la fecha y hora en que fueron registradas.
- Cada marcación debe poder asociarse con el empleado correspondiente.
- La información de asistencia debe conservarse para permitir consultas históricas.
- Las marcaciones provenientes de los dispositivos biométricos deben ser procesadas antes de utilizarse para cálculos de nómina.
- La información utilizada para liquidación debe mantener trazabilidad hacia los registros de asistencia que la originaron.
- Las reglas utilizadas para determinar horas extras y recargos se encuentran documentadas en las reglas de negocio del sistema.

## Reglas relacionadas

Las reglas específicas para el procesamiento de asistencia y su impacto en la liquidación se documentan en:

[Reglas del negocio](../decisions/business-rules.md)
[Nómina](../decisions/payroll.md)