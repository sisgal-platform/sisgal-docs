# Mantenimiento

## Dependencias y calidad

Revisa las actualizaciones de dependencias en los manifiestos y lockfiles de cada aplicación antes de incorporarlas. Para las verificaciones locales, consulta los comandos documentados en [Instalación y entorno](setup.md).

En el Backend Core, `npm run lint` aplica correcciones con ESLint y `npm run format` reescribe archivos con Prettier. Revisa los cambios producidos antes de confirmarlos.

## Esquema y migraciones

El Backend Core usa TypeORM y PostgreSQL. Antes de modificar el esquema:

1. Revisa las entidades y migraciones existentes en el repositorio del core.
2. Confirma el comando disponible para generar, revisar y ejecutar migraciones.
3. Valida el cambio en un entorno no productivo.
4. Documenta el resultado y el procedimiento de reversión.

El manifiesto compartido no declara scripts de migración; por eso esta guía no inventa comandos de TypeORM.

## Auditoría

El modelo de auditoría de [base de datos](../diagrams/database.md) describe el diseño suministrado para las entidades AuditUser, AuditEvent, AuditFieldChange, AuditMetadata, AuditError y AuditSnapshot. La base de auditoría todavía no está conectada a SISGAL. No se deben asumir persistencia activa, migraciones, respaldos, política de retención o integración con el Backend Core hasta que esos mecanismos estén implementados y validados.

## Respaldos y recuperación

La base principal está en Supabase. La base de auditoría se diseñó como PostgreSQL independiente, pero todavía no está conectada ni se confirmó su proveedor de alojamiento. La frecuencia, retención, pruebas de restauración y responsables deben documentarse al configurar ese servicio.

## Diagnóstico

Una vez implementados los pipelines, sus ejecuciones de GitHub Actions servirán para investigar fallos de validación o despliegue. Usa además los registros de Vercel y Render para diagnosticar los servicios publicados.
