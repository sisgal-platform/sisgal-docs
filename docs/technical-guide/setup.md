# Instalación y entorno de desarrollo

Esta guía recoge los scripts declarados en los manifiestos de frontend y backend core. Ejecuta los comandos desde la carpeta que contiene el `package.json` correspondiente. El gestor indicado es npm y el runtime es Node.js.

## Tecnologías y herramientas declaradas

| Área | Tecnologías |
|---|---|
| Frontend | React `^19.2.8`, React Router `^7.18.3`, TypeScript `~6.0.2`, Vite `^8.2.2`, Tailwind CSS `^3.4.19`, Axios `^1.20.0`, Supabase JS `^2.116.0` (autenticación), Radix UI, Recharts y Lucide React |
| Pruebas frontend | Vitest `^5.0.0`, Testing Library, jsdom y `@vitest/coverage-v8` |
| Backend core | NestJS `^12.0.3`, TypeORM `^1.1.1`, PostgreSQL driver `pg ^8.23.0`, jose `^6.2.12`, Swagger, class-validator, class-transformer y Winston |
| Pruebas backend core | Jest `^30.0.0`, ts-jest `^29.2.5` y Supertest |

El frontend usa `@supabase/supabase-js` solo para autenticación; no accede directamente a la base de datos. React Hook Form no aparece en el manifiesto compartido y no se documenta como dependencia.

La versión exacta de Node.js y npm aún debe fijarse. Usa la versión acordada por el equipo y el lockfile incluido en cada repositorio; si el repositorio contiene `package-lock.json`, instala dependencias con `npm ci`.

## Frontend

| Comando | Función |
|---|---|
| `npm run dev` | Inicia el servidor de desarrollo de Vite. |
| `npm run build` | Ejecuta `tsc -b` y genera la compilación de producción con Vite. |
| `npm run preview` | Sirve localmente la compilación generada para revisión. |
| `npm run lint` | Ejecuta ESLint. |
| `npm run test` | Ejecuta Vitest una vez. |
| `npm run test:watch` | Ejecuta Vitest en modo interactivo. |
| `npm run test:coverage` | Ejecuta las pruebas y calcula cobertura. |

## Backend Core

| Comando | Función |
|---|---|
| `npm run start:dev` | Inicia NestJS en modo observación. |
| `npm run start:debug` | Inicia NestJS con depuración y observación. |
| `npm run build` | Compila el backend con Nest CLI. |
| `npm run start:prod` | Ejecuta el artefacto compilado desde `dist/main`. |
| `npm run lint` | Ejecuta ESLint con `--fix`; puede modificar archivos. |
| `npm run format` | Aplica Prettier a los archivos TypeScript de `src` y `test`; modifica archivos. |
| `npm run test` | Ejecuta Jest. |
| `npm run test:watch` | Ejecuta Jest en modo observación. |
| `npm run test:cov` | Ejecuta Jest con cobertura. |
| `npm run test:e2e` | Ejecuta las pruebas de extremo a extremo con `test/jest-e2e.json`. |

El script `test:debug` también está disponible para depurar Jest con Node Inspector.

## Alcance actual

El backend documentado es el Backend Core. No hay un microservicio biométrico implementado ni un manifiesto separado que requiera instrucciones propias.

## Pendiente de completar

- Versiones exactas de Node.js y npm que se fijarán para desarrollo y pipelines.
- Confirmar la existencia de `package-lock.json` en cada repositorio y mantenerlo versionado.
- Creación y migración de bases de datos, una vez verificados los comandos disponibles en el repositorio del core.
