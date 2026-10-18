# Desarrollo y contribución

## Verificaciones locales

Ejecuta los scripts desde la raíz del frontend o del backend core, según el cambio. Las instrucciones completas están en [Instalación y entorno](setup.md).

Como comprobaciones locales están disponibles:

- **Frontend:** `npm run lint`, `npm run build`, `npm run test`.
- **Backend Core:** `npm run lint`, `npm run build`, `npm run test`; para pruebas de extremo a extremo, `npm run test:e2e`.

Los scripts backend `lint` y `format` modifican archivos; revisa el diff resultante antes de confirmar cambios.

## Pipelines

Los despliegues se realizan mediante pipelines de GitHub Actions activados por cambios en `develop`. El flujo debe mantenerse alineado con los scripts del proyecto y con la configuración de Vercel y Render.

## Prácticas de contribución

- No incluyas secretos ni valores reales de configuración en los cambios.
- Actualiza las guías técnicas cuando cambien scripts, dependencias, variables de entorno o procedimientos.
- Consulta las convenciones de rama, commits, revisión y aprobación definidas por el equipo antes de asumir reglas adicionales; no están especificadas en esta documentación.
