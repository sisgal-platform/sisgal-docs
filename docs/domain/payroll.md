# Nómina

## Descripción

La nómina corresponde al proceso mediante el cual SISGAL determina los valores que deben ser considerados para la liquidación de cada empleado durante un periodo determinado.

El proceso utiliza información laboral del empleado, registros de asistencia y novedades que pueden afectar los valores de la liquidación.

## Información utilizada

La liquidación de nómina utiliza información proveniente de diferentes conceptos del dominio:

```text
                    Empleado
                       │
          ┌────────────┼────────────┐
          │            │            │
          ▼            ▼            ▼
       Cargo       Sucursal    Salario base
          │            │            │
          └────────────┼────────────┘
                       │
                       ▼
                  Información
                   laboral
                       │
          ┌────────────┼────────────┐
          │            │            │
          ▼            ▼            ▼
      Asistencia   Préstamos   Incapacidades
          │            │            │
          └────────────┼────────────┘
                       ▼
                  Liquidación
                       │
                       ▼
                  Resultado
```

## Componentes de la liquidación

La liquidación puede involucrar diferentes conceptos agrupados principalmente en:

### Devengados

Corresponden a los valores que se generan a favor del empleado durante el periodo liquidado.

Entre ellos pueden encontrarse:

- Salario.
- Horas extras.
- Recargos.
- Auxilio de transporte, cuando corresponda.
- Otros conceptos definidos por las reglas de negocio.

### Deducciones

Corresponden a valores que se descuentan de la liquidación del empleado.

Entre ellos pueden encontrarse:

- Aportes correspondientes al empleado.
- Descuentos por préstamos.
- Otras deducciones aplicables.

Las deducciones consideradas dependen de las reglas de negocio y de las novedades registradas para el empleado.

### Asistencia y liquidación

La información de asistencia puede generar conceptos que afectan la liquidación.

A partir de las marcaciones y su procesamiento pueden identificarse situaciones como:

- Horas trabajadas.
- Horas extras diurnas.
- Horas extras nocturnas.
- Trabajo nocturno.
- Trabajo en domingos.
- Trabajo en días festivos.

Los valores resultantes son utilizados por el proceso de liquidación de acuerdo con las reglas de negocio establecidas.

## Novedades

Las novedades representan situaciones que pueden modificar el resultado de la liquidación.

SISGAL contempla, entre otras:

### Préstamos

Los préstamos registrados para un empleado pueden generar descuentos periódicos durante la liquidación.

La información del préstamo debe permitir identificar:

- Empleado.
- Valor del préstamo.
- Periodicidad.
- Información necesaria para controlar los descuentos correspondientes.

### Incapacidades

Las incapacidades representan periodos durante los cuales un empleado presenta una ausencia asociada a una incapacidad registrada.

La información de la incapacidad puede afectar los valores considerados durante la liquidación, de acuerdo con las reglas de negocio aplicables.

## Proceso de liquidación

De manera general, el proceso de liquidación contempla:

```
1. Identificar empleados
          │
          ▼
2. Obtener información laboral
          │
          ▼
3. Obtener información de asistencia
          │
          ▼
4. Obtener novedades
          │
          ▼
5. Determinar conceptos de devengados
          │
          ▼
6. Determinar deducciones
          │
          ▼
7. Calcular resultado de liquidación
          │
          ▼
8. Generar información de nómina
```

El detalle de cada cálculo depende de las reglas de negocio definidas para SISGAL.

## Resultado de la liquidación

El resultado de la liquidación contiene los valores calculados para el empleado durante el periodo correspondiente.

Entre la información que puede formar parte del resultado se encuentra:

| Concepto         | Descripción                                                          |
| ---------------- | -------------------------------------------------------------------- |
| **Empleado**     | Identificación del empleado liquidado.                               |
| **Periodo**      | Periodo de nómina procesado.                                         |
| **Salario base** | Valor base utilizado en la liquidación.                              |
| **Devengados**   | Total de conceptos generados a favor del empleado.                   |
| **Deducciones**  | Total de conceptos descontados.                                      |
| **Neto a pagar** | Resultado final después de aplicar las deducciones correspondientes. |

## Comprobante de nómina

SISGAL contempla la generación de información para el comprobante de nómina.

El comprobante debe permitir identificar al empleado y presentar los principales valores utilizados en la liquidación.

Entre la información contemplada se encuentra:

- Nombre del empleado.
- Cargo.
- Identificación.
- Salario base.
- Conceptos de devengados.
- Deducciones.

## Resultado de la liquidación.

El formato final del comprobante debe mantener correspondencia con la información calculada durante el proceso de liquidación.

## Trazabilidad

La liquidación debe conservar la relación con la información que dio origen a sus resultados.

```
Liquidación
     │
     ├── Empleado
     │
     ├── Asistencia
     │     ├── Marcaciones
     │     ├── Horas extras
     │     └── Recargos
     │
     ├── Préstamos
     │
     └── Incapacidades
```

Esta trazabilidad permite consultar y verificar los datos utilizados durante el procesamiento.

## Reglas de negocio

Las reglas específicas relacionadas con porcentajes, límites, aportes, recargos y demás cálculos de nómina se encuentran documentadas en:

[Reglas del negocio](../decisions/business-rules.md)

Entre las reglas contempladas por SISGAL se encuentran las relacionadas con:

- Horas extras.
- Recargos nocturnos.
- Trabajo en domingos y festivos.
- Aportes de seguridad social.
- Descuentos.
- Préstamos.
- Incapacidades.

## Relación con otros conceptos del dominio

La nómina constituye un proceso transversal que utiliza información de diferentes elementos del dominio:

| Concepto        | Relación con nómina                                                                  |
| --------------- | ------------------------------------------------------------------------------------ |
| **Empleado**    | Proporciona la información laboral necesaria para la liquidación.                    |
| **Asistencia**  | Proporciona información sobre las jornadas y conceptos derivados de las marcaciones. |
| **Préstamo**    | Puede generar deducciones durante la liquidación.                                    |
| **Incapacidad** | Puede modificar los conceptos considerados durante el periodo.                       |
| **Cargo**       | Forma parte de la información laboral del empleado y del comprobante de nómina.      |
| **Sucursal**    | Permite identificar la ubicación organizacional del empleado.                        |
