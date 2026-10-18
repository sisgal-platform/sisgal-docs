# Producción

## Plataformas previstas

- Frontend React: Vercel.
- Backend Core NestJS: Render.
- Base principal PostgreSQL: Supabase.
- Base PostgreSQL de auditoría: independiente, diseñada pero todavía sin conexión a SISGAL.

Los pipelines y los procedimientos de publicación automática están en preparación. Los workflows de ejemplo en [GitHub Actions](github-actions.md) apuntan a una Preview de Vercel y al servicio Render enlazado con `develop`; no representan aún una configuración activa ni una aprobación de producción.

## Antes de habilitar producción

Confirma dominios, variables de entorno, rama asociada, secretos, roles de publicación, verificaciones posteriores al despliegue, respaldos y reversión. Configura los valores secretos directamente en Vercel, Render o el entorno protegido de GitHub Actions correspondiente. No los almacenes en la documentación ni en el repositorio.

El paso de `develop` a producción, el mecanismo de aprobación y el procedimiento de rollback siguen pendientes de definición.
