# Configuración

Configura las variables en el entorno que corresponda a cada aplicación. No incluyas valores reales, credenciales ni cadenas de conexión en Git o en esta documentación.

## Frontend

| Variable | Uso | Tratamiento |
|---|---|---|
| `VITE_SUPABASE_URL` | URL del proyecto Supabase utilizada por el cliente del frontend. | Es visible en el navegador; no es una credencial secreta. |
| `VITE_SUPABASE_ANON_KEY` | Clave anon usada por el frontend para identificar el proyecto en Supabase. | Vite la incorpora al código cliente. No es secreta; la protección de datos depende de RLS y permisos mínimos. |
| `VITE_API_URL` | URL base de la API del backend core. | Es visible en el navegador; no es una credencial secreta. |

Vite expone las variables con prefijo `VITE_` en el código de cliente durante la compilación. No pongas contraseñas, claves privadas ni claves de servicio en variables con ese prefijo. Consulta la [guía de variables de Vite](https://vite.dev/guide/env-and-mode).

La clave `anon` es el formato legado de clave pública de Supabase. Supabase anunció su migración a claves `publishable` y `secret` y la retirada de las claves legadas hacia finales de 2026. Se conserva aquí el nombre que usa actualmente SISGAL; planifica la migración antes de cambiar la configuración. Consulta la [guía de claves de Supabase](https://supabase.com/docs/guides/getting-started/api-keys).

## Backend Core

| Variable | Uso | Tratamiento |
|---|---|---|
| `SUPABASE_DB_URL` | Cadena de conexión PostgreSQL para el backend core. | Secreta; configúrala como credencial protegida del entorno. |
| `SUPABASE_URL` | URL del proyecto Supabase. | No es una contraseña; evita publicar configuraciones internas innecesarias. |

## Archivos y entornos

Para desarrollo local, utiliza el mecanismo de configuración local del repositorio y comprueba qué archivos están excluidos de Git. En despliegue, define las variables en el entorno de compilación o ejecución que consume cada pipeline y servicio. La ubicación concreta de los secretos y la separación entre desarrollo, pruebas y producción debe coincidir con la configuración activa de GitHub Actions, Vercel y Render.

La configuración de variables del microservicio biométrico está pendiente de documentar a partir de su manifiesto y su código.
