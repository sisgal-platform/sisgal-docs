# ADR-001 — Monolito modular

## Estado

Aceptado.

## Contexto

SISGAL requiere integrar diferentes funcionalidades relacionadas con la gestión de empleados, el registro y consulta de asistencia, la administración de novedades y el cálculo y liquidación de nómina. Aunque estos procesos tienen responsabilidades diferenciadas, necesitan intercambiar información para garantizar la coherencia de los resultados del sistema.

Para organizar estas funcionalidades se requiere una arquitectura que permita separar las responsabilidades del software, facilitar su mantenimiento y controlar las dependencias entre los componentes. Adicionalmente, el proyecto cuenta con un equipo de tres desarrolladores y un alcance que debe implementarse de manera incremental dentro del periodo académico establecido.

En este contexto, se consideró necesario adoptar una arquitectura que facilite la organización modular del backend sin introducir la complejidad operativa asociada con la administración de múltiples servicios independientes.

## Alternativas consideradas

**Monolito tradicional:** consiste en desarrollar la aplicación como una unidad integrada, sin establecer necesariamente límites claros entre sus componentes funcionales. Aunque puede simplificar el despliegue inicial, una separación insuficiente de responsabilidades puede dificultar el mantenimiento y aumentar el acoplamiento interno.

**Arquitectura de microservicios:** propone dividir el sistema en servicios independientes, cada uno con responsabilidades específicas y mecanismos de comunicación entre ellos. Esta alternativa permite desplegar y escalar servicios por separado, pero introduce complejidad adicional en la comunicación, el despliegue, la observabilidad y la gestión de datos distribuidos.

**Monolito modular:** organiza la aplicación como una unidad desplegable, dividida internamente en módulos con responsabilidades delimitadas y dependencias controladas. Esta alternativa permite mantener la integración de la solución y, al mismo tiempo, establecer una estructura que favorezca la mantenibilidad.

## Decisión

Se adopta una **arquitectura de monolito modular para el backend de SISGAL**, desarrollado con NestJS y TypeScript.

La aplicación se organiza en módulos funcionales que agrupan responsabilidades relacionadas con el dominio. Cada módulo debe mantener límites claros y exponer únicamente las operaciones necesarias para la interacción con otros módulos.

La estructura interna se apoya en la separación de responsabilidades entre dominio, aplicación e infraestructura, según las necesidades de cada módulo. Esta organización busca evitar que las reglas de negocio dependan directamente de los detalles técnicos de persistencia o comunicación.

La comunicación entre los módulos se realizará de manera directa y síncrona, mediante los mecanismos internos de la aplicación. No se adopta una arquitectura basada en microservicios ni se requiere introducir sistemas de mensajería asíncrona para la comunicación interna del monolito.

## Justificación

La arquitectura de monolito modular se considera adecuada porque permite mantener una solución integrada y, simultáneamente, organizar el código de acuerdo con las responsabilidades funcionales de SISGAL.

La elección favorece la separación de responsabilidades, facilita la comprensión del sistema y permite desarrollar y probar módulos de manera diferenciada sin asumir la complejidad operativa de una infraestructura distribuida.

Asimismo, la arquitectura es coherente con el alcance académico del proyecto, el tamaño del equipo y la necesidad de integrar funcionalidades que comparten información y reglas de negocio, especialmente durante el cálculo y la liquidación de nómina.

## Consecuencias

**Consecuencias positivas:**

- Se establecen límites funcionales que facilitan la organización y el mantenimiento del código.
- Se favorece la reutilización de componentes y servicios internos.
- Se simplifica la comunicación entre funcionalidades que comparten información.
- Se reduce la complejidad operativa frente a una arquitectura distribuida de microservicios.
- Se facilita la ejecución de pruebas por módulo y la integración progresiva de funcionalidades.

**Consecuencias y limitaciones:**

- La aplicación se despliega como una unidad integrada, por lo que no se obtiene escalado independiente por módulo.
- Un problema que afecte a la aplicación puede comprometer el funcionamiento de varios módulos.
- La arquitectura exige mantener límites internos claros para evitar que los módulos se conviertan en componentes fuertemente acoplados.
- Los cambios que requieran desplegar el backend pueden afectar a la aplicación completa, aunque el cambio esté concentrado en un solo módulo.

## Relación con otras decisiones

Esta decisión se relaciona con la selección de NestJS para el backend, PostgreSQL para la persistencia relacional y React para la interfaz de usuario. En conjunto, estas tecnologías permiten mantener una separación entre la presentación, la lógica de negocio y el acceso a los datos.
