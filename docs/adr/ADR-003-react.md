# ADR-003 — React

## Estado

Aceptado.

## Contexto

SISGAL requiere una interfaz web que permita a los usuarios interactuar con las funcionalidades de gestión de empleados, asistencia, novedades y nómina. La interfaz debe facilitar la consulta de información, la ejecución de operaciones administrativas y la visualización de resultados de manera clara y consistente.

Debido a que el sistema incorpora diferentes módulos funcionales, se necesita una tecnología que permita organizar la interfaz mediante componentes reutilizables, mantener una estructura de desarrollo comprensible y facilitar la evolución progresiva de las pantallas.

También se requiere separar la presentación de la lógica de negocio del backend, de modo que la interfaz consuma las funcionalidades del sistema mediante una API y no implemente directamente las operaciones de persistencia.

## Alternativas consideradas

**Angular:** es un framework para el desarrollo de aplicaciones web que proporciona una estructura definida, mecanismos de inyección de dependencias y herramientas integradas para organizar aplicaciones de gran tamaño.

**React:** es una biblioteca de JavaScript para construir interfaces de usuario mediante componentes. Permite desarrollar elementos reutilizables y organizar la interfaz en unidades que pueden componerse para construir pantallas y funcionalidades más complejas.

**Vue:** es un framework progresivo para construir interfaces web que ofrece un modelo declarativo y un sistema de componentes, con posibilidades de integración gradual en diferentes tipos de aplicaciones.

## Decisión

Se selecciona **React con TypeScript para el desarrollo del frontend de SISGAL**.

La interfaz se organiza mediante componentes reutilizables y módulos funcionales, buscando mantener una separación clara entre la presentación, el estado de la interfaz y la interacción con los servicios del backend.

El frontend se comunica con el backend de NestJS mediante una API REST. Esta separación permite que la interfaz consuma las operaciones expuestas por el servidor sin asumir directamente las responsabilidades de las reglas de negocio ni del acceso a la base de datos.

## Justificación

React permite construir interfaces a partir de componentes reutilizables, lo que favorece la consistencia visual y reduce la duplicación de elementos compartidos entre las diferentes pantallas.

Su modelo de composición facilita la organización de funcionalidades relacionadas con la gestión de empleados, la asistencia, los préstamos, las incapacidades y la nómina. Además, TypeScript permite definir tipos para los datos utilizados en la interfaz y detectar determinados errores durante el desarrollo.

La separación entre frontend y backend también contribuye a mantener responsabilidades diferenciadas. React se encarga de la presentación y la interacción con el usuario, mientras que NestJS centraliza la lógica de negocio y la comunicación con la persistencia.

Esta decisión es coherente con la necesidad de desarrollar SISGAL de manera incremental, incorporando nuevas pantallas y funcionalidades sin tener que construir la interfaz completa como una única unidad indivisible.

## Consecuencias

**Consecuencias positivas:**

- Permite crear componentes reutilizables para formularios, tablas, paneles y elementos de navegación.
- Favorece la organización de las funcionalidades mediante módulos de frontend.
- Facilita la evolución gradual de la interfaz conforme se incorporan historias de usuario.
- TypeScript permite definir contratos de datos y mejorar la detección temprana de errores.
- La separación mediante API REST permite mantener diferenciadas las responsabilidades del frontend y del backend.

**Consecuencias y limitaciones:**

- La organización de la aplicación requiere definir convenciones para los componentes, los módulos y el manejo del estado.
- El consumo de la API exige gestionar adecuadamente los estados de carga, los errores y las respuestas del servidor.
- La biblioteca no proporciona por sí sola todas las herramientas de una aplicación completa; las necesidades adicionales deben resolverse mediante las herramientas y bibliotecas seleccionadas para el proyecto.
- La consistencia visual y la accesibilidad dependen de las decisiones de diseño y de la implementación de los componentes.

## Relación con otras decisiones

Esta decisión complementa la arquitectura de monolito modular del backend y la selección de PostgreSQL para la persistencia. React proporciona la interfaz de usuario, NestJS expone las operaciones mediante la API REST y PostgreSQL almacena la información administrada por el sistema.

En conjunto, estas tecnologías permiten separar las responsabilidades de presentación, lógica de negocio y persistencia, favoreciendo la organización y el mantenimiento de SISGAL.
