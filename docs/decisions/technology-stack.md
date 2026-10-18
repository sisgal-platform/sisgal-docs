# Stack Tecnológico

## 1. Objetivo

Este documento describe las principales tecnologías y herramientas utilizadas para desarrollar SISGAL, así como su responsabilidad dentro de la solución.

## 2. Tecnologías principales

| Componente | Tecnología | Responsabilidad |
|---|---|---|
| Frontend | React | Construcción de la interfaz de usuario. |
| Lenguaje del frontend | TypeScript | Incorporar tipado estático y mejorar la mantenibilidad del código. |
| Herramienta de construcción del frontend | Vite | Ejecutar el entorno de desarrollo y generar los artefactos de compilación. |
| Backend | NestJS | Implementar la API y la lógica del servidor mediante módulos y servicios. |
| Lenguaje del backend | TypeScript | Mantener tipado y consistencia en la implementación del servidor. |
| Persistencia relacional | PostgreSQL | Almacenar información estructurada del sistema. |
| Acceso a datos | TypeORM | Mapear entidades y gestionar operaciones sobre la base de datos desde el backend. |
| Comunicación | API REST | Permitir la comunicación entre el frontend y el backend mediante solicitudes HTTP. |

## 3. Herramientas complementarias

| Herramienta | Uso |
|---|---|
| Git | Control de versiones del código fuente. |
| GitHub | Hospedaje de repositorios y colaboración en el desarrollo. |
| Tailwind CSS | Aplicación de estilos mediante clases utilitarias, según la configuración del frontend. |
| MkDocs Material | Organización y publicación de la documentación técnica del proyecto. |
| Supabase | Servicio utilizado para alojar y administrar la base de datos PostgreSQL, según la configuración del entorno. |

La configuración exacta de cada herramienta debe verificarse en los archivos del proyecto y en los entornos utilizados por el equipo.

## 4. Criterios de selección

Las tecnologías se seleccionan teniendo en cuenta los siguientes criterios:

- **Mantenibilidad:** facilitar la lectura, modificación y evolución del código.
- **Modularidad:** permitir organizar las funcionalidades en componentes con responsabilidades definidas.
- **Tipado:** detectar errores durante el desarrollo y mejorar la claridad de los contratos.
- **Integración:** facilitar la comunicación entre la interfaz, la API y la base de datos.
- **Persistencia e integridad:** contar con un modelo relacional para gestionar entidades y sus relaciones.
- **Documentación y soporte:** disponer de documentación técnica para resolver problemas y mantener la solución.

## 5. Lineamientos de uso

1. Mantener TypeScript en los componentes principales del frontend y del backend.
2. Gestionar las dependencias mediante el administrador de paquetes definido por cada aplicación.
3. Mantener las credenciales y variables de entorno fuera del código fuente.
4. Utilizar Git para registrar los cambios y facilitar su revisión.
5. Evitar incorporar dependencias nuevas sin evaluar su necesidad, compatibilidad y mantenimiento.
6. Mantener sincronizados los contratos de la API y las funcionalidades que los consumen.
7. Documentar cualquier cambio significativo en la selección o configuración de las tecnologías.

## 6. Entornos y despliegue

Las aplicaciones y sus servicios deben configurarse mediante variables de entorno para separar los parámetros de desarrollo, pruebas y producción.

La URL de la API, las credenciales de acceso a la base de datos y demás parámetros sensibles no deben codificarse directamente en el repositorio.

Los servicios de despliegue concretos y sus procedimientos deben documentarse en la sección correspondiente de [Despliegue](../deployment/), una vez confirmados para el entorno vigente.

## 7. Mantenimiento

Si se reemplaza una tecnología o se introduce un componente nuevo, se debe actualizar este documento y revisar los ADR relacionados cuando el cambio afecte una decisión arquitectónica previamente registrada.
