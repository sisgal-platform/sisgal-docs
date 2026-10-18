# Seguridad

## Variables y credenciales

- No guardes valores de variables de entorno, cadenas de conexión ni secretos en Git.
- `SUPABASE_DB_URL` es una credencial del backend; protégela en los entornos donde se ejecute el core.
- Las variables `VITE_*` se incluyen en el código cliente compilado y son visibles desde el navegador. No las uses para secretos.
- `VITE_SUPABASE_ANON_KEY` es una clave pública que el frontend utiliza para autenticación. No es una clave de servicio. Nunca incluyas una clave `service_role` o `secret` en el frontend.
- El frontend no accede directamente a la base de datos; las operaciones de datos se realizan a través del backend core.
- La clave `anon` usada actualmente es legada; consulta la nota de migración en [Configuración](configuration.md).

Consulta las recomendaciones oficiales de [Vite](https://vite.dev/guide/env-and-mode) y [Supabase](https://supabase.com/docs/guides/getting-started/api-keys).

## Autenticación y datos

El frontend utiliza `@supabase/supabase-js` para autenticación. El backend core expone la API de SISGAL y es el punto de acceso a los datos.

La arquitectura describe autenticación backend con JWT, guards y roles, pero esta guía no confirma todavía su comportamiento implementado ni el mecanismo de emisión y renovación de tokens. Completa esta sección desde la configuración efectiva del backend.

SISGAL maneja información de empleados, asistencia, nómina y marcaciones biométricas. Documenta las políticas reales de acceso, las reglas aplicadas por el backend, la retención de datos y el manejo de incidentes una vez verificadas en el código y los entornos.

El módulo de auditoría transversal está propuesto; no se debe presentar como un control de seguridad ya implementado.
