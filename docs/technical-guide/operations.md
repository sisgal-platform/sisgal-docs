# Operación y despliegue

Los pipelines de GitHub Actions aún no están implementados. El despliegue automático es el objetivo de trabajo y debe validar calidad, cobertura y Sonar antes de publicar cada aplicación.

## Destinos previstos

- **Frontend React:** Vercel Preview para cambios integrados en `develop`.
- **Backend Core:** servicio de pruebas en Render enlazado a `develop`.
- **Producción:** separada de esos destinos de pruebas; su flujo de publicación está pendiente de definir.
- **Base de datos principal:** PostgreSQL en Supabase.
- **Base de auditoría:** diseño PostgreSQL independiente; aún no está conectada al sistema.

La [vista de despliegue](../diagrams/deployment.md) muestra los servicios y dependencias que están confirmados. El flujo del dispositivo biométrico se documentará cuando se confirme su implementación.

## Flujo propuesto

1. En una solicitud de cambio hacia `develop`, instalar dependencias usando Node.js, npm y el lockfile del repositorio.
2. Ejecutar lint, pruebas, generar el reporte de cobertura y compilar la aplicación afectada.
3. Exigir cobertura mínima de líneas del 80%.
4. Ejecutar el análisis de Sonar y exigir que su Quality Gate sea aprobado.
5. Detener el flujo si falla una validación.
6. Al integrar cambios en `develop), publicar solo la aplicación afectada en su destino de pruebas: frontend como Preview en Vercel o Backend Core en el servicio de pruebas de Render.
7. Revisar el resultado del despliegue y comprobar la aplicación desde la URL de su entorno.

Este es un diseño pendiente de implementación. Aún deben configurarse la versión exacta de Node.js, la organización y los proyectos de Sonar, los secretos de despliegue, los checks obligatorios, y los pasos de reversión y verificación de salud.

## Operación y recuperación pendientes

- Definir entornos, responsables y URL de cada aplicación.
- Configurar endpoints de salud y criterios de aceptación posteriores al despliegue.
- Documentar y probar el procedimiento de rollback.
- Definir monitoreo, alertas y retención de registros.
- Definir respaldos y restauración de ambas bases cuando la auditoría esté conectada.
