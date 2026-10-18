# Mantenimiento

## Dependencias y calidad

Revisa las actualizaciones de dependencias en los manifiestos y lockfiles de cada servicio antes de incorporarlas. Para las verificaciones locales, consulta los comandos documentados en [Instalación y entorno](setup.md).

En el backend core, `npm run lint` aplica correcciones con ESLint y `npm run format` reescribe archivos con Prettier. Revisa los cambios producidos antes de confirmarlos.

## Esquema y migraciones

El backend core usa TypeORM y PostgreSQL. Antes de modificar el esquema:

1. Revisa las entidades y migraciones existentes en el repositorio del core.
2. Confirma el comando disponible para generar, revisar y ejecutar migraciones.
3. Valida el cambio en un entorno no productivo.
4. Documenta el resultado y el procedimiento de reversión.

El manifiesto compartido no declara scripts de migración; por eso esta guía no inventa comandos de TypeORM. Confirma además si la base de auditoría tiene migraciones y ciclo de cambios independientes.

## Respaldos y recuperación

La base principal está en Supabase y la base de auditoría es PostgreSQL independiente. El proveedor, la frecuencia, la retención, las pruebas de restauración y los responsables del respaldo de auditoría no están definidos aquí. Registra estos datos después de verificarlos en los entornos reales.

## Diagnóstico

Usa los registros de los servicios de Render y el historial del pipeline de GitHub Actions para investigar fallos de despliegue. Los dashboards, alertas, niveles de log y periodos de retención deben añadirse cuando estén configurados y confirmados.
