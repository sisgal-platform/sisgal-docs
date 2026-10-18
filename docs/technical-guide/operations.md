# Operación y despliegue

Los pipelines de GitHub Actions aún no están implementados. El despliegue automático es el objetivo de trabajo y debe validar calidad, cobertura y Sonar antes de publicar cada aplicación.

## Destinos previstos

- **Frontend React:** Vercel.
- **Backend Core:** Render.
- **Base de datos principal:** PostgreSQL en Supabase.
- **Base de auditoría:** diseño PostgreSQL independiente; aún no está conectada al sistema.

La [vista de despliegue](../diagrams/deployment.md) muestra los servicios y dependencias que están confirmados. El flujo del dispositivo biométrico se documentará cuando se confirme su implementación.

## Flujo propuesto

1. En una solicitud de cambio, instalar dependencias usando Node.js, npm y el lockfile del repositorio.
2. Ejecutar lint, pruebas, generar el reporte de cobertura y compilar la aplicación afectada.
3. Ejecutar el análisis de Sonar y exigir que su Quality Gate sea aprobado.
4. Detener el flujo si falla una validación o no se alcanza la cobertura mínima acordada.
5. Al integrar cambios en `develop`, publicar solo la aplicación afectada en sus destinos de pruebas: frontend como Preview en Vercel o Backend Core en un servicio de pruebas de Render.
6. Revisar el resultado del despliegue y comprobar la aplicación desde la URL de su entorno.

Este es un diseño pendiente de implementación. La rama exacta, el umbral de cobertura, la instancia y proyectos de Sonar, los nombres de secretos, las condiciones de despliegue y los pasos de reversión deben confirmarse antes de activar los workflows.

## Operación y recuperación pendientes

- Definir entornos, responsables y URL de cada aplicación.
- Configurar endpoints de salud y criterios de aceptación posteriores al despliegue.
- Documentar y probar el procedimiento de rollback.
- Definir monitoreo, alertas y retención de registros.
- Definir respaldos y restauración de ambas bases cuando la auditoría esté conectada.
