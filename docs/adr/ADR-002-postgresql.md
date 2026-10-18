# ADR-002 — PostgreSQL

## Estado

Aceptado.

## Contexto

SISGAL debe almacenar y consultar información relacionada con los empleados, sus horarios, las marcaciones de asistencia, las novedades laborales, los parámetros de nómina y los resultados de los procesos de cálculo y liquidación. La arquitectura contempla una base de datos principal y una base de datos de auditoría independiente; actualmente ambas están definidas con PostgreSQL.

Estos datos presentan relaciones entre diferentes entidades y requieren mecanismos que permitan mantener su integridad y consistencia. Por ejemplo, los préstamos deben asociarse con los empleados correspondientes, las liquidaciones deben relacionarse con los periodos procesados y los cálculos deben utilizar información coherente con los parámetros definidos para el sistema.

Por esta razón, se requiere un sistema gestor de bases de datos que permita modelar relaciones, definir restricciones de integridad y ejecutar consultas sobre información estructurada. También se busca disponer de una tecnología compatible con el backend desarrollado en NestJS y TypeScript.

## Alternativas consideradas

**MySQL:** es un sistema gestor de bases de datos relacional que permite almacenar información estructurada y establecer relaciones entre entidades. Constituye una alternativa viable para aplicaciones empresariales que requieren persistencia relacional.

**PostgreSQL:** es un sistema gestor de bases de datos relacional de código abierto que ofrece transacciones, restricciones de integridad, relaciones entre tablas y capacidades avanzadas de consulta. Estas características permiten representar dominios con relaciones y reglas de consistencia entre sus datos.

**MongoDB:** es una base de datos orientada a documentos que permite almacenar información con estructuras flexibles. Aunque puede ser adecuada para determinados tipos de datos, su modelo documental no representa la primera opción para el núcleo de SISGAL, donde predominan las relaciones entre empleados, asistencia, novedades y liquidaciones.

## Decisión

Se selecciona **PostgreSQL para la base de datos principal de SISGAL y para su base de datos de auditoría independiente**.

La elección responde a la necesidad de administrar información estructurada y relacionada, mantener restricciones de integridad y ejecutar operaciones transaccionales sobre los datos utilizados por los procesos de asistencia y nómina. PostgreSQL también permite almacenar datos JSON cuando ciertos eventos de auditoría requieren atributos variables.

La posible adopción de una base NoSQL para auditoría queda como alternativa por evaluar; no forma parte de esta decisión aceptada. Un cambio requeriría validar el formato y volumen de los eventos, las consultas, la retención, la seguridad y el costo operativo.

## Justificación

PostgreSQL permite representar mediante tablas y relaciones las entidades del dominio, establecer claves primarias y foráneas y definir restricciones que contribuyan a preservar la integridad de la información.

Las transacciones permiten agrupar operaciones relacionadas y mantener la consistencia de los cambios confirmados en la base de datos. Esta característica resulta relevante en procesos que involucran múltiples registros y deben evitar estados parciales inconsistentes.

Además, PostgreSQL dispone de capacidades de consulta que permiten recuperar y relacionar información para funcionalidades como la consulta del historial de asistencia, la revisión de préstamos, la generación de liquidaciones y la presentación de indicadores.

Su compatibilidad con el ecosistema de desarrollo utilizado en SISGAL permite integrarlo con el backend sin requerir un sistema de persistencia propietario.

## Consecuencias

**Consecuencias positivas:**

- Permite representar las relaciones entre las entidades del dominio mediante un modelo relacional.
- Proporciona mecanismos de integridad referencial y restricciones de datos.
- Ofrece soporte transaccional para operaciones que requieren consistencia.
- Facilita la consulta de información relacionada con asistencia, empleados y nómina.
- Puede integrarse con el backend desarrollado en NestJS mediante las herramientas de acceso a datos seleccionadas.

**Consecuencias y limitaciones:**

- El diseño del esquema requiere definir adecuadamente las entidades, relaciones, restricciones e índices.
- Los cambios en el modelo de datos deben gestionarse mediante migraciones controladas.
- Las consultas y operaciones deben diseñarse y probarse para evitar problemas de rendimiento a medida que aumenta el volumen de información.
- La consistencia de los datos también depende de la correcta implementación de las transacciones, las validaciones y las reglas de negocio en la aplicación.

## Relación con otras decisiones

Esta decisión complementa la arquitectura de monolito modular del core y define PostgreSQL para las bases independientes del sistema y de auditoría. También se relaciona con la selección de NestJS y con la organización de las entidades del dominio, cuyos datos deben almacenarse y consultarse de forma consistente.
