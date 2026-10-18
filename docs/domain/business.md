# Negocio

## Contexto

SISGAL (Sistema de Gestión de Asistencia y Liquidación de Nómina) es una solución orientada a apoyar la gestión administrativa de los empleados de **JS Burguer Parrilla**, centralizando la información relacionada con asistencia y liquidación de nómina.

El sistema busca reducir la dependencia de procesos manuales y facilitar la consulta, gestión y procesamiento de la información utilizada para la liquidación de los empleados.

## Actores del dominio

| Actor | Descripción |
|---|---|
| **Administrador** | Usuario encargado de gestionar la información del sistema y realizar operaciones administrativas. |
| **Empleado** | Persona cuya información laboral, asistencia y liquidación son gestionadas por el sistema. |
| **Dispositivo biométrico** | Dispositivo utilizado para registrar las marcaciones de entrada y salida de los empleados. |

## Procesos del negocio

### Gestión de empleados

Permite administrar la información básica y laboral de los empleados, incluyendo su relación con cargos y sucursales.

### Registro de asistencia

Las marcaciones realizadas por los empleados son registradas mediante los dispositivos biométricos y posteriormente procesadas por SISGAL.

### Procesamiento de asistencia

Las marcaciones son utilizadas para determinar la información asociada a las jornadas laborales y los conceptos que puedan afectar la liquidación.

### Liquidación de nómina

La información laboral, las jornadas, las novedades y demás conceptos aplicables son utilizados para realizar la liquidación correspondiente a cada empleado.

## Parametrización

SISGAL contempla información parametrizable utilizada por otros procesos del sistema.

Entre los principales elementos de parametrización se encuentran:

- Sucursales.
- Cargos.

La parametrización permite mantener catálogos utilizados en los formularios y procesos administrativos del sistema.

## Novedades

Las novedades corresponden a situaciones que pueden modificar el resultado de la liquidación de un empleado.

Entre ellas se contemplan:

- Préstamos.
- Incapacidades.
- Horas extras.
- Recargos.
- Otras novedades definidas por las reglas de negocio.

## Flujo general del negocio

```text
Empleado
    │
    ├── Cargo
    ├── Sucursal
    │
    ▼
Marcaciones
    │
    ▼
Asistencia
    │
    ├── Jornada
    ├── Horas extras
    └── Recargos
    │
    ▼
Novedades
    │
    ├── Préstamos
    └── Incapacidades
    │
    ▼
Liquidación de nómina
    │
    ▼
Resultado de pago
```

## Reglas de negocio

Las reglas específicas utilizadas para el procesamiento de asistencia y liquidación se documentan en:

[Reglas del negocio](../decisions/business-rules.md)

Estas reglas constituyen la referencia para determinar el comportamiento esperado de los procesos de SISGAL.
