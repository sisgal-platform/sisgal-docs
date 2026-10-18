# Arquitectura del Frontend

## Introducción

El frontend de SISGAL ofrece la interfaz de usuario y está organizado por funcionalidades (Feature-Based Architecture). Está desarrollado con React y TypeScript.

## Tecnologías y librerías

- **React `^19.2.8` y React DOM `^19.2.8`:** componentes e interfaz.
- **React Router `^7.18.3`:** navegación y rutas.
- **Vite `^8.2.2`:** servidor de desarrollo y compilación.
- **TypeScript `~6.0.2`:** tipado estático.
- **Tailwind CSS `^3.4.19`:** estilos.
- **Axios `^1.20.0`:** llamadas HTTP a la API REST del backend core.
- **Supabase JS `^2.116.0`:** autenticación.
- **Radix UI:** primitivas de interfaz.
- **Recharts `^3.10.1` y Lucide React `^1.44.0`:** gráficos e iconografía.
- **Vitest `^5.0.0`, Testing Library y jsdom:** pruebas frontend.

La librería React Hook Form no está incluida en el manifiesto actual y no se documenta como dependencia.

## Organización

La aplicación se organiza por funcionalidades. Cada feature agrupa sus componentes, páginas, servicios y lógica de presentación relacionados.

Los componentes compartidos y las utilidades de interfaz se construyen con React, Tailwind CSS y las librerías UI incluidas en el manifiesto.

## Comunicación y autenticación

El frontend consume la API REST del backend core mediante Axios. El cliente `@supabase/supabase-js` se usa para autenticación; no se utiliza para consultar directamente las bases de datos de SISGAL.

La navegación se implementa con React Router. Las rutas protegidas responden al estado de autenticación definido por la aplicación.

## Comandos principales

Los scripts del frontend permiten ejecutar el servidor de desarrollo, compilar, validar lint y correr pruebas con Vitest. Consulta [Instalación y entorno](../technical-guide/setup.md) para la lista exacta de comandos.
