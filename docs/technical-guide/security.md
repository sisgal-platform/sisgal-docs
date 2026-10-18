# Seguridad

## Variables y credenciales

- No guardes valores de variables de entorno, cadenas de conexión ni secretos en Git.
- `SUPABASE_DB_URL` es una credencial del backend; protégela en los entornos donde se ejecute el core.
- Las variables `VITE_*` se incluyen en el código cliente compilado y son visibles desde el navegador. No las uses para secretos.
- `VITE_SUPABASE_ANON_KEY` es una clave pública de cliente, no una clave de servicio. La exposición pública requiere políticas RLS bien configuradas y permisos mínimos. Nunca incluyas una clave `service_role` o `secret` en el frontend.
- La clave `anon` usada actualmente es legada; consulta la nota de migración en [Configuración](configuration.md).

Consulta las recomendaciones oficiales de [Vite](https://vite.dev/guide/env-and-mode) y [Supabase](https://supabase.com/docs/guides/database/secure-data).

## Autenticación y datos

La arquitectura describe autenticación con JWT, guards y roles, pero esta guía no confirma todavía el comportamiento implementado ni el mecanismo de emisión y renovación de tokens. Completa esta sección desde la configuración efectiva del backend.

SISGAL maneja información de empleados, asistencia, nómina y marcaciones biométricas. Documenta las políticas reales de acceso, las reglas RLS de Supabase, la retención de datos y el manejo de incidentes una vez verificadas en el código y los entornos.

El módulo de auditoría transversal está propuesto; no se debe presentar como un control de seguridad ya implementado.
