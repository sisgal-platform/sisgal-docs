# Reglas del Negocio

## 1. Objetivo

Este documento reúne las reglas funcionales que orientan los procesos de asistencia, clasificación de horas trabajadas, gestión de novedades y liquidación de nómina de SISGAL.

Estas reglas deben aplicarse de forma consistente en el backend para garantizar que los cálculos y las operaciones del sistema respeten las condiciones definidas para el negocio y la normativa laboral colombiana aplicable.

## 2. Principios generales

1. Las reglas de negocio deben centralizarse en el backend y no depender exclusivamente de validaciones de la interfaz.
2. Los datos necesarios para realizar cálculos deben validarse antes de procesarlos.
3. Los parámetros laborales y económicos deben poder consultarse según su vigencia cuando corresponda.
4. Los cálculos deben ser trazables y permitir identificar los datos y parámetros utilizados.
5. Las modificaciones de las reglas deben reflejarse en las pruebas y en la documentación.
6. Los resultados de una liquidación deben corresponder al período, empleado, novedades y parámetros aplicables.

## 3. Gestión de empleados

- Cada empleado debe contar con un identificador único.
- La información obligatoria debe validarse antes de registrar o modificar un empleado.
- Las operaciones relacionadas con la nómina deben asociarse al empleado correspondiente.
- La consulta de empleados debe permitir identificar los registros de acuerdo con los criterios de búsqueda implementados.
- La modificación o desactivación de un empleado no debe alterar automáticamente los registros históricos que deban conservarse.

## 4. Registro y consulta de asistencia

El sistema debe gestionar las marcaciones de entrada y salida utilizadas para determinar los intervalos de tiempo trabajados.

### Reglas generales

- Las marcaciones deben asociarse al empleado correspondiente.
- Las fechas y horas recibidas deben validarse.
- Las marcaciones deben procesarse cronológicamente.
- Los intervalos incompletos, duplicados o inconsistentes deben identificarse y tratarse según las validaciones definidas.
- El tiempo trabajado debe calcularse a partir de las marcaciones válidas y las reglas de jornada aplicables.
- Los registros originales deben conservarse cuando sea necesario para la trazabilidad y auditoría.

Cuando las marcaciones provengan de un dispositivo biométrico, la integración debe validar la identificación del empleado y la información recibida antes de incorporar el registro al proceso de asistencia.

## 5. Clasificación de horas trabajadas

El sistema debe clasificar los intervalos trabajados de acuerdo con la jornada configurada y las reglas laborales aplicables.

La clasificación debe considerar, según corresponda:

- Horas ordinarias diurnas.
- Horas ordinarias nocturnas.
- Horas extras diurnas.
- Horas extras nocturnas.
- Horas trabajadas en domingos y festivos.
- Horas extras en domingos y festivos, diferenciadas por franja horaria.

Los intervalos que atraviesen un cambio de franja horaria, el inicio o final de una jornada o un límite de calendario deben dividirse cuando sea necesario para aplicar el tratamiento correcto a cada segmento.

Los horarios de jornada y los límites entre franjas diurnas y nocturnas deben obtenerse de la configuración vigente, no de valores duplicados arbitrariamente en distintos componentes.

## 6. Cálculo del valor de la hora ordinaria

Como referencia para los cálculos de nómina, el valor de la hora ordinaria se obtiene mediante la siguiente expresión:

**Valor hora ordinaria = salario base mensual / 30 / horas ordinarias diarias configuradas**

La fórmula debe aplicarse de acuerdo con el modelo salarial y la jornada correspondientes al empleado y al período liquidado.

Antes de utilizar el resultado, el sistema debe validar que el salario y las horas configuradas sean valores válidos.

## 7. Recargos y horas extras

Los multiplicadores utilizados por SISGAL deben administrarse mediante la configuración de recargos laborales y aplicarse según el tipo de hora clasificada.

Los multiplicadores de referencia registrados para el proyecto son:

| Tipo de hora | Multiplicador de referencia |
|---|---:|
| Hora extra diurna | 1,25 |
| Hora extra nocturna | 1,75 |
| Hora dominical o festiva diurna | 1,75 |
| Hora dominical o festiva nocturna | 2,10 |
| Hora extra dominical o festiva diurna | 2,00 |
| Hora extra dominical o festiva nocturna | 2,50 |

Estos valores representan la configuración de referencia del proyecto y **deben verificarse frente a la normativa vigente y la fecha del período liquidado** antes de considerarse definitivos para producción. Cuando la regulación establezca porcentajes diferentes según la fecha, el sistema debe utilizar la configuración correspondiente a la vigencia aplicable.

El valor de una hora con recargo se calcula a partir del valor de la hora ordinaria y del multiplicador configurado para el tipo de hora.

La implementación debe evitar aplicar dos veces el mismo recargo o confundir un multiplicador total con un porcentaje adicional.

## 8. Jornada laboral y límites de horas extras

La clasificación y validación de las horas trabajadas deben considerar los límites legales aplicables y los parámetros de jornada configurados.

Como referencia del diseño del proyecto, se han contemplado límites de dos horas extras diarias y doce semanales. Estos límites deben validarse frente a la normativa vigente y a las excepciones que correspondan antes de su uso definitivo.

El sistema debe distinguir entre:

- La jornada ordinaria configurada.
- Las horas efectivamente trabajadas.
- Las horas que exceden la jornada ordinaria.
- Los límites máximos permitidos.
- Las alertas o inconsistencias que requieran revisión.

La configuración de los límites debe contar con vigencias cuando los cambios normativos o de política laboral lo requieran.

## 9. Auxilio de transporte

Para determinar la elegibilidad del auxilio de transporte, el sistema debe comparar el salario base del empleado con el límite de dos salarios mínimos legales mensuales vigentes, de acuerdo con las condiciones legales aplicables.

Los parámetros económicos de referencia son:

- `MINIMUM_WAGE`: salario mínimo mensual vigente.
- `TRANSPORT_ALLOWANCE`: valor del auxilio de transporte vigente.

El cálculo debe utilizar los valores correspondientes al período liquidado y validar las condiciones de elegibilidad antes de incorporar el concepto a la base de liquidación.

La elegibilidad y el valor reconocido deben ajustarse a la normativa aplicable y a las condiciones del empleado. No debe asumirse que todos los empleados reciben automáticamente el auxilio.

## 10. Deducciones legales

El sistema contempla las deducciones de salud y pensión como parte del proceso de liquidación.

Como regla de referencia definida para el proyecto:

| Concepto | Porcentaje de referencia |
|---|---:|
| Salud a cargo del empleado | 4 % |
| Pensión a cargo del empleado | 4 % |

Estos porcentajes deben aplicarse sobre la base correspondiente a cada concepto, después de determinar correctamente los valores que la integran.

La base de cotización, las exclusiones, los topes, las reglas de redondeo y cualquier condición especial deben verificarse de acuerdo con la normativa vigente y el tipo de vinculación del empleado.

El sistema debe evitar realizar deducciones sobre bases incorrectas o duplicar una deducción durante la generación de la liquidación.

## 11. Gestión de novedades

SISGAL contempla novedades que pueden afectar el cálculo de la nómina, entre ellas préstamos e incapacidades.

### Préstamos

- Cada préstamo debe asociarse al empleado correspondiente.
- Deben registrarse los datos necesarios para determinar las cuotas y su estado.
- El descuento de una cuota debe realizarse según las condiciones definidas para el préstamo.
- El sistema debe evitar descontar dos veces una misma cuota en el mismo proceso de liquidación.
- Las cuotas pendientes, pagadas y las demás condiciones de estado deben mantenerse consistentes.

### Incapacidades

- Cada incapacidad debe asociarse al empleado correspondiente.
- Deben validarse sus fechas y la información requerida para el registro.
- La novedad debe considerarse según el período afectado y las reglas aplicables.
- Su tratamiento económico debe ajustarse a la normativa vigente y a las condiciones del caso.

Las reglas específicas de cálculo y los estados permitidos deben mantenerse alineados con la implementación de los módulos correspondientes.

## 12. Preliquidación y liquidación de nómina

### Preliquidación

La preliquidación permite calcular valores preliminares para un período determinado antes de confirmar la liquidación definitiva.

Debe considerar, según corresponda:

- Empleados incluidos en el proceso.
- Período de liquidación.
- Horas ordinarias y extras clasificadas.
- Recargos aplicables.
- Auxilio de transporte, cuando corresponda.
- Deducciones legales.
- Novedades que afecten el período.
- Otros conceptos configurados para la nómina.

El resultado debe permitir revisar los valores calculados y detectar inconsistencias antes de generar la liquidación definitiva.

### Liquidación definitiva

La liquidación debe consolidar los valores correspondientes al período y a los empleados incluidos, de acuerdo con las reglas vigentes.

Antes de confirmar una liquidación, deben validarse los datos y cálculos necesarios. Una liquidación confirmada debe conservar la información que permita consultar sus resultados y generar el comprobante correspondiente.

Las modificaciones posteriores deben seguir las reglas de actualización y trazabilidad definidas para el sistema.

## 13. Primas y otros conceptos

El sistema contempla el cálculo de primas y otros conceptos asociados a la nómina.

Su cálculo debe utilizar el período correspondiente, la información salarial, los días o factores aplicables y las reglas legales vigentes para el concepto.

Las fórmulas definitivas, las bases de cálculo, las condiciones de proporcionalidad y las fechas de causación deben documentarse en las historias de usuario o especificaciones funcionales correspondientes y verificarse mediante pruebas.

No se deben reutilizar automáticamente las fórmulas de otros conceptos cuando sus bases o condiciones legales sean diferentes.

## 14. Precisión y redondeo

Los cálculos monetarios deben utilizar tipos numéricos adecuados para representar valores decimales y evitar errores derivados de la precisión binaria de los números de punto flotante.

El sistema debe definir de manera consistente:

- La precisión de los cálculos intermedios.
- El momento en que se redondean los valores.
- El número de decimales del resultado final.
- La forma de consolidar los conceptos por empleado y período.

La política de redondeo debe aplicarse uniformemente y validarse con casos de prueba representativos.

## 15. Configuración y vigencia de los parámetros

Los parámetros laborales y económicos susceptibles de cambios deben administrarse de forma centralizada.

Cuando corresponda, cada configuración debe identificar su fecha de inicio de vigencia y su fecha de finalización. Esto permite aplicar los valores correctos a los períodos históricos y evitar que una actualización modifique indebidamente los resultados anteriores.

Las configuraciones deben validarse para prevenir períodos de vigencia incompatibles o ambiguos.

## 16. Trazabilidad y auditoría

Las operaciones relevantes deben permitir identificar, según el alcance implementado:

- El empleado y el período afectados.
- Los datos utilizados para el cálculo.
- Los parámetros y vigencias aplicados.
- El resultado generado.
- Las modificaciones realizadas y su responsable, cuando corresponda.

Los registros de auditoría deben protegerse de modificaciones no autorizadas y conservarse de acuerdo con las políticas de seguridad y retención del sistema.

## 17. Pruebas de las reglas de negocio

Cada regla de negocio debe validarse mediante pruebas apropiadas. Se deben contemplar, como mínimo:

- Casos válidos y casos con datos incompletos.
- Intervalos que atraviesan límites de jornada o de calendario.
- Cambios de parámetros por fecha de vigencia.
- Empleados que cumplen o no las condiciones de elegibilidad.
- Cálculos con valores límite y resultados decimales.
- Novedades que afectan parcialmente un período.
- Prevención de descuentos o conceptos duplicados.
- Consistencia entre la preliquidación y la liquidación definitiva.

Las pruebas deben actualizarse cuando cambien las reglas, la configuración o la normativa aplicable.

## 18. Mantenimiento

Este documento debe actualizarse cuando se incorporen nuevas reglas, se modifiquen las fórmulas o se ajusten las condiciones legales.

Los valores presentados como referencias no sustituyen la validación de la normativa colombiana vigente. Antes de liberar cambios relacionados con nómina, deben revisarse las reglas aplicables al período correspondiente y verificarse mediante pruebas.
