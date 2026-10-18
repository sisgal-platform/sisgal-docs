# Configuración

Configura las variables en el entorno que corresponda a cada aplicación. No incluyas valores reales, credenciales ni cadenas de conexión en Git o en esta documentación.

## Frontend

| Variable | Uso | Tratamiento |
|---|---|---|
| `VITE_SUPABASE_URL` | URL del proyecto Supabase usada por el cliente de autenticación. | Visible en el navegador; no es una credencial secreta. |
| `VITE_SUPABASE_ANON_KEY` | Clave pública anon que el cliente Supabase usa para autenticación. | Vite la incorpora al código cliente; no es secreta. |
| `VITE_API_URL` | URL base de la API REST del backend core. | Visible en el navegador; no es una credencial secreta. |

El frontend usa `@supabase/supabase-js` para autenticación. **No consulta directamente las bases de datos de SISGAL**; las operaciones de datos se envían al backend core mediante la API.

Vite expone las variables con prefijo `VITE_` en el código de cliente durante la compilación. No pongas contraseñas, claves privadas ni claves de servicio en variables con ese prefijo. Consulta la [guía de variables de Vite](https://vite.dev/guide/env-and-mode).

La clave `anon` es el formato legado de clave pública de Supabase. Supabase anunció su migración a claves `publishable` y `secret` y la retirada de las claves legadas hacia finales de 2026. Se conserva aquí el nombre que usa actualmente SISGAL; planifica la migración antes de cambiar la configuración. Consulta la [guía de claves de Supabase](https://supabase.com/docs/guides/getting-started/api-keys).

## Backend Core

| Variable | Uso | Tratamiento |
|---|---|---|
| `SUPABASE_DB_URL` | Cadena de conexión PostgreSQL utilizada por el backend core. | Secreta; configúrala como credencial protegida del entorno. |
| `SUPABASE_URL` | URL del proyecto Supabase. | No es una contraseña; evita publicar configuraciones internas innecesarias. |

## Archivos y entornos

Para desarrollo local, utiliza el mecanismo de configuración local del repositorio y comprueba qué archivos están excluidos de Git. En despliegue, define las variables en el entorno de compilación o ejecución que consume cada pipeline y servicio. La ubicación concreta de los secretos y la separación entre desarrollo, pruebas y producción debe coincidir con la configuración activa de GitHub Actions, Vercel y Render.

La configuración de variables del microservicio biométrico está pendiente de documentar a partir de su manifiesto y su código.
