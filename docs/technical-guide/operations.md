# Operación y despliegue

SISGAL despliega sus aplicaciones mediante pipelines de **GitHub Actions** al detectar cambios en la rama `develop`. El flujo de despliegue comprende el frontend y los servicios de backend.

## Destinos de despliegue

- **Frontend React:** Vercel.
- **Backend Core:** Render.
- **Microservicio de integración biométrica:** Render.
- **Base de datos principal:** PostgreSQL en Supabase.
- **Base de auditoría:** PostgreSQL independiente; su alojamiento y su integración siguen pendientes de definir.

La [vista de despliegue](../diagrams/deployment.md) muestra la topología y el flujo de las marcaciones.

## Verificación de un despliegue

1. Revisa el resultado del pipeline de GitHub Actions asociado al cambio en `develop`.
2. Comprueba que los servicios publicados en Vercel y Render finalicen el despliegue correctamente.
3. Verifica la aplicación y las rutas principales desde sus URL configuradas.
4. Revisa los registros de los servicios ante errores de inicio o comunicación.

Los nombres de workflows, verificaciones automáticas, endpoints de salud y pasos de reversión deben documentarse al confirmar los archivos de workflow y la configuración de cada plataforma. Esta guía no presupone comandos manuales de publicación.

## Pendiente de completar

- Responsables y URL de cada entorno.
- Flujo exacto de cada workflow, incluyendo filtros de cambios y condiciones de publicación.
- Validaciones posteriores al despliegue y criterios de aceptación.
- Procedimiento probado de rollback.
- Monitoreo, alertas y retención de registros.
- Pasos de operación y recuperación de las bases de datos.
