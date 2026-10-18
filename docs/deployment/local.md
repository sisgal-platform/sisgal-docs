# Desarrollo local

Esta página resume cómo iniciar las aplicaciones documentadas en un entorno local. Usa las versiones acordadas de Node.js y npm y el lockfile del repositorio. La versión exacta aún debe fijarse.

## Frontend

Desde la carpeta del frontend:

```bash
npm ci
npm run dev
```

Antes de iniciar, configura `VITE_SUPABASE_URL`, `VITE_SUPABASE_ANON_KEY` y `VITE_API_URL` en el entorno local. El cliente Supabase se utiliza para autenticación; las operaciones de datos se envían al Backend Core.

## Backend Core

Desde la carpeta del Backend Core:

```bash
npm ci
npm run start:dev
```

Configura `SUPABASE_DB_URL` y `SUPABASE_URL` para el entorno local. No uses credenciales de producción para pruebas locales.

## Pruebas y compilación

Consulta [Instalación y entorno](../technical-guide/setup.md) para los comandos disponibles de lint, pruebas, cobertura y compilación.

No hay un microservicio biométrico implementado. El procedimiento de conexión local con el dispositivo queda fuera del flujo actual.
