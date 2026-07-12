# Arquitectura del Frontend

## Introducción

El frontend de SISGAL proporciona la interfaz de usuario para la administración del sistema. Fue desarrollado utilizando React y TypeScript, organizando la aplicación mediante una arquitectura basada en características (Feature-Based Architecture).

---

## Objetivos

La arquitectura del frontend busca:

- Facilitar el mantenimiento.
- Favorecer la reutilización de componentes.
- Reducir el acoplamiento.
- Mejorar la experiencia del usuario.
- Simplificar el crecimiento del sistema.

---

## Tecnologías

- React
- TypeScript
- React Router
- Axios
- TanStack Query
- React Hook Form
- Tailwind CSS
- Jest

---

## Organización

La aplicación se organiza por funcionalidades.

Cada feature contiene sus propios componentes, páginas, servicios y lógica de negocio.

Esta estructura facilita la evolución del sistema conforme aumenten los módulos funcionales.

---

## Comunicación con el Backend

Toda la comunicación con el backend se realiza mediante API REST.

Las peticiones HTTP son administradas utilizando Axios y React Query para aprovechar funcionalidades como:

- Caché.
- Reintentos automáticos.
- Sincronización.
- Invalidación de consultas.

---

## Navegación

La navegación se implementa mediante React Router.

Las rutas protegidas estarán controladas por el estado de autenticación del usuario.

---

## Calidad

El frontend incorpora:

- ESLint.
- Prettier.
- Jest.
- GitHub Actions.
