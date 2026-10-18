# Stack Tecnológico

## 1. Objetivo

Este documento registra las principales tecnologías y herramientas declaradas para SISGAL. Los rangos de versión corresponden a los manifiestos de frontend y backend core compartidos para la documentación.

## 2. Tecnologías principales

| Componente | Tecnología | Responsabilidad |
|---|---|---|
| Frontend | React `^19.2.8`, React DOM `^19.2.8` | Construcción de la interfaz de usuario. |
| Navegación | React Router `^7.18.3` | Gestión de rutas del frontend. |
| Herramienta de construcción | Vite `^8.2.2` | Servidor de desarrollo y generación de la compilación. |
| Lenguaje del frontend | TypeScript `~6.0.2` | Tipado estático del cliente. |
| Estilos y UI | Tailwind CSS `^3.4.19`, Radix UI | Estilos y primitivas de interfaz. |
| Cliente HTTP | Axios `^1.20.0` | Consumo de la API REST del backend core. |
| Autenticación frontend | `@supabase/supabase-js ^2.116.0` | Autenticación. El frontend no accede directamente a la base de datos. |
| Backend Core | NestJS `^12.0.3` | API y lógica de negocio organizada en módulos. |
| Lenguaje del backend | TypeScript `^5.7.3` | Tipado del servidor. |
| Persistencia | PostgreSQL y driver `pg ^8.23.0` | Almacenamiento relacional del sistema y de la base independiente de auditoría. |
| Acceso a datos | TypeORM `^1.1.1` | Persistencia utilizada por el backend core. |
| Pruebas frontend | Vitest `^5.0.0`, Testing Library | Pruebas unitarias y de componentes del frontend. |
| Pruebas backend | Jest `^30.0.0`, Supertest `^7.0.0` | Pruebas del backend core y de extremo a extremo. |

## 3. Herramientas complementarias

| Herramienta | Uso |
|---|---|
| Vercel | Despliegue del frontend. |
| Render | Despliegue de los dos servicios de backend. |
| GitHub Actions | Pipelines de despliegue activados por cambios en la rama `develop`. |
| Git y GitHub | Control de versiones, repositorios y colaboración. |
| Supabase | Autenticación del frontend y alojamiento de la base PostgreSQL principal. |
| MkDocs Material | Organización y publicación de la documentación técnica. |

La librería React Hook Form no aparece en el manifiesto frontend compartido y no se registra como dependencia vigente. La base de datos de auditoría continúa en PostgreSQL; su alojamiento y el uso del módulo de auditoría están por definir.

## 4. Configuración

El frontend utiliza `VITE_SUPABASE_URL`, `VITE_SUPABASE_ANON_KEY` y `VITE_API_URL`. El backend core utiliza `SUPABASE_DB_URL` y `SUPABASE_URL`. Consulta el [Manual técnico de configuración](../technical-guide/configuration.md) para su propósito y tratamiento.

Las versiones soportadas de Node.js y el gestor de paquetes deben verificarse en los repositorios de aplicación; no se han especificado aquí.
