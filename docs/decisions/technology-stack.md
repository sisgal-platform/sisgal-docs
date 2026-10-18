# Stack Tecnológico

## 1. Objetivo

Este documento registra las principales tecnologías y herramientas declaradas para SISGAL. Los rangos de versión corresponden a los manifiestos de frontend y Backend Core compartidos para la documentación.

## 2. Tecnologías principales

| Componente | Tecnología | Responsabilidad |
|---|---|---|
| Frontend | React `^19.2.8`, React DOM `^19.2.8` | Construcción de la interfaz de usuario. |
| Navegación | React Router `^7.18.3` | Gestión de rutas del frontend. |
| Herramienta de construcción | Vite `^8.2.2` | Servidor de desarrollo y generación de la compilación. |
| Lenguaje del frontend | TypeScript `~6.0.2` | Tipado estático del cliente. |
| Estilos y UI | Tailwind CSS `^3.4.19`, Radix UI | Estilos y primitivas de interfaz. |
| Cliente HTTP | Axios `^1.20.0` | Consumo de la API REST del Backend Core. |
| Autenticación frontend | `@supabase/supabase-js ^2.116.0` | Autenticación; el frontend no accede directamente a la base de datos. |
| Backend Core | NestJS `^12.0.3` | API y lógica de negocio organizada en módulos. |
| Lenguaje del backend | TypeScript `^5.7.3` | Tipado estático del servidor. |
| Persistencia | PostgreSQL y driver `pg ^8.23.0` | Almacenamiento relacional principal. |
| Acceso a datos | TypeORM `^1.1.1` | Persistencia utilizada por el Backend Core. |
| Pruebas frontend | Vitest `^5.0.0`, Testing Library | Pruebas unitarias y de componentes. |
| Pruebas backend | Jest `^30.0.0`, Supertest `^7.0.0` | Pruebas del Backend Core y de extremo a extremo. |
| Runtime y gestor de paquetes | Node.js y npm | Entorno de ejecución e instalación de dependencias; versiones exactas pendientes de fijar. |

## 3. Herramientas complementarias

| Herramienta | Uso |
|---|---|
| Vercel | Plataforma de destino del frontend. |
| Render | Plataforma de destino del Backend Core. |
| GitHub Actions | Plataforma elegida para pipelines de validación y despliegue; workflows aún no implementados. |
| Git y GitHub | Control de versiones, repositorios y colaboración. |
| Supabase | Autenticación del frontend y alojamiento de la base PostgreSQL principal. |
| MkDocs Material | Organización y publicación de la documentación técnica. |
| SonarQube Cloud | Propuesta para análisis estático; cuenta/proyectos aún no configurados. |

React Hook Form no aparece en el manifiesto frontend compartido y no se registra como dependencia vigente. La base de auditoría PostgreSQL está diseñada como independiente, pero todavía no está conectada a SISGAL. No hay un microservicio biométrico implementado.

## 4. Configuración

El frontend utiliza `VITE_SUPABASE_URL`, `VITE_SUPABASE_ANON_KEY` y `VITE_API_URL`. El Backend Core utiliza `SUPABASE_DB_URL` y `SUPABASE_URL`. Consulta el [Manual técnico de configuración](../technical-guide/configuration.md).

## 5. Pipelines

Se proponen workflows separados para el frontend y el Backend Core. Cada uno validará lint, pruebas, cobertura mínima global de líneas de 80%, compilación y Quality Gate de Sonar antes de desplegar la aplicación correspondiente. Consulta [Pipelines con GitHub Actions](../deployment/github-actions.md).

La versión exacta de Node.js, el umbral de cobertura de Sonar y las credenciales de publicación se deben configurar antes de activar los workflows.
