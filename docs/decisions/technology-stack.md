# Stack Tecnológico

## Introducción

El stack tecnológico de SISGAL está conformado por las tecnologías, frameworks, bibliotecas y herramientas seleccionadas para implementar el sistema de gestión de asistencia y liquidación de nómina.

La selección se realizó considerando las necesidades funcionales del proyecto, los atributos de calidad definidos, la experiencia técnica del equipo y la facilidad de mantenimiento y evolución de la solución.

## Tecnologías principales

| Capa | Tecnología | Propósito |
|---|---|---|
| **Frontend** | React | Desarrollo de la interfaz de usuario. |
| **Lenguaje frontend** | TypeScript | Tipado estático y desarrollo del frontend. |
| **Build tool** | Vite | Desarrollo y construcción de la aplicación frontend. |
| **UI** | Shadcn/ui | Construcción de componentes reutilizables de interfaz. |
| **Backend** | NestJS | Desarrollo de los servicios backend. |
| **Lenguaje backend** | TypeScript | Implementación de la lógica de negocio y servicios. |
| **API** | REST | Comunicación entre frontend y backend. |
| **Base de datos** | PostgreSQL | Persistencia de la información transaccional. |
| **Autenticación** | Supabase Auth | Gestión de autenticación y sesiones de usuario. |
| **Pruebas** | Jest | Ejecución de pruebas automatizadas. |
| **Control de versiones** | Git | Gestión del código fuente y control de cambios. |
| **Repositorio** | GitHub | Hospedaje de repositorios y colaboración. |
| **CI/CD** | GitHub Actions | Automatización de procesos de integración y despliegue. |
| **Contenedores** | Docker | Estandarización de entornos de ejecución. |
| **Documentación** | MkDocs Material | Generación y publicación de la documentación técnica. |
| **Gestión del trabajo** | Azure DevOps | Gestión de historias de usuario, tareas y seguimiento del proyecto. |

## Frontend

El frontend está desarrollado con **React y TypeScript**, utilizando Vite como herramienta de construcción y desarrollo.

La aplicación utiliza una organización orientada a funcionalidades, donde cada módulo concentra los componentes, servicios e interfaces relacionados con su responsabilidad funcional.

Los principales módulos contemplados son:

- Dashboard.
- Asistencia.
- Nómina.
- Novedades.
- Personal.
- Reportes.
- Configuración.

Para la construcción de la interfaz se utiliza Shadcn/ui junto con componentes propios organizados bajo un enfoque de reutilización y composición.

## Backend

El backend está desarrollado con **NestJS y TypeScript**.

NestJS proporciona una estructura modular para organizar los servicios y funcionalidades del sistema, permitiendo separar responsabilidades y facilitar el mantenimiento.

La API utiliza el estilo arquitectónico REST para exponer las operaciones requeridas por el frontend.

Entre las funcionalidades backend se encuentran:

- Autenticación.
- Gestión de empleados.
- Gestión de cargos.
- Gestión de sucursales.
- Gestión de asistencia.
- Gestión de préstamos.
- Gestión de incapacidades.
- Liquidación de nómina.
- Consultas y reportes.

## Persistencia

SISGAL utiliza **PostgreSQL** como sistema de gestión de base de datos.

La persistencia se organiza de acuerdo con las necesidades de los diferentes procesos del sistema, permitiendo separar la información relacionada con las marcaciones de asistencia de la información utilizada para los cálculos y resultados de nómina.

La base de datos permite mantener la información necesaria para:

- Empleados.
- Cargos.
- Sucursales.
- Marcaciones.
- Préstamos.
- Incapacidades.
- Procesos de nómina.
- Resultados de liquidación.
- Información de auditoría.

## Pruebas

Para las pruebas automatizadas se utiliza **Jest**.

Las pruebas se incorporan como mecanismo de validación de la lógica implementada y buscan verificar el comportamiento esperado de los componentes y servicios del sistema.

Los tipos de pruebas contemplados se documentan en la sección de pruebas del proyecto.

## Control de versiones

El código fuente se gestiona mediante **Git** y se aloja en **GitHub**.

El flujo de trabajo contempla ramas destinadas al desarrollo y a la integración de cambios, junto con mecanismos de protección para evitar modificaciones directas sobre las ramas principales.

## Integración y despliegue

**GitHub Actions** se utiliza para automatizar procesos asociados a integración y despliegue.

Entre los procesos automatizados se encuentra la generación y publicación de la documentación técnica mediante MkDocs.

## Documentación

La documentación técnica del proyecto se desarrolla utilizando **MkDocs Material**.

La documentación se mantiene en un repositorio independiente y se publica mediante GitHub Pages.

La estructura documental incluye:

- Arquitectura.
- Dominio.
- API.
- Decisiones técnicas.
- ADR.
- Diagramas.
- Deployment.
- Backlog.
- Sprints.

## Gestión del proyecto

**Azure DevOps** se utiliza para gestionar el backlog y realizar seguimiento al desarrollo.

La estructura de trabajo contempla:

```text
Tema
  ↓
Épica
  ↓
Historia de usuario
  ↓
Tarea
```

Las historias de usuario se relacionan con los Sprints y con las tareas técnicas necesarias para su implementación.

## Criterios de selección

La selección del stack tecnológico consideró principalmente:

- Compatibilidad con los requerimientos del sistema.
- Facilidad de mantenimiento.
- Modularidad.
- Disponibilidad de documentación y comunidad.
- Integración entre las tecnologías.
- Capacidad de evolución.
- Experiencia técnica del equipo.
- Compatibilidad con las necesidades de despliegue.
- Relación con la arquitectura

El stack tecnológico soporta las decisiones arquitectónicas definidas para SISGAL.

En particular:

- React permite implementar una interfaz modular y orientada a funcionalidades.
- NestJS proporciona una estructura modular para el backend.
- PostgreSQL proporciona persistencia relacional.
- REST establece el mecanismo principal de comunicación entre frontend y backend.
- Docker permite estandarizar los entornos de ejecución.
- GitHub Actions automatiza procesos de integración y despliegue.

Las decisiones arquitectónicas específicas se documentan en [Decisiones de Arquitectura](architecture-decisions.md).