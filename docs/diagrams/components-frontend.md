# Componentes del Frontend (C4, Nivel 3)

El diagrama desglosa el frontend React en sus responsabilidades de navegación, presentación, funcionalidades y comunicación con la API. Refleja las tecnologías confirmadas: React Router, Tailwind CSS, Axios y React Hook Form.

![Diagrama de componentes del Frontend](images/components-frontend.svg)

[Ver fuente PlantUML](source/components-frontend.puml)

## Componentes

- **Pages / Routing:** organiza las páginas y rutas mediante React Router.
- **Layout & Navigation:** estructura compartida, navegación y elementos comunes de la interfaz.
- **UI Components:** componentes reutilizables construidos con React y Tailwind CSS.
- **Feature Modules:** agrupa las funcionalidades de autenticación, asistencia, nómina y configuración.
- **State Management:** administra el estado de la interfaz; la librería no está especificada en este diagrama.
- **Forms:** gestiona formularios con React Hook Form.
- **API Services:** centraliza las llamadas HTTP con Axios.
- **Auth Handling:** controla el estado de autenticación y la protección de rutas.

## Relaciones principales

Las páginas componen el layout y cargan funcionalidades. Las funcionalidades usan componentes visuales, formularios, el manejo de estado y los servicios de API. Los servicios REST se comunican con el Backend Core mediante HTTPS/JSON.
