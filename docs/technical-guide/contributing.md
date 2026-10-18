# Desarrollo y contribución

## Verificaciones locales

Ejecuta los scripts desde la raíz del frontend o del backend core, según el cambio. Las instrucciones completas están en [Instalación y entorno](setup.md).

Como comprobaciones locales están disponibles:

- **Frontend:** `npm run lint`, `npm run build`, `npm run test` y `npm run test:coverage`.
- **Backend Core:** `npm run lint`, `npm run build`, `npm run test:cov`; para pruebas de extremo a extremo, `npm run test:e2e`.

Los scripts backend `lint` y `format` modifican archivos; revisa los cambios producidos antes de confirmarlos.

## Pipelines

Los workflows de GitHub Actions aún no existen. El diseño previsto valida lint, pruebas, cobertura y Sonar; luego despliega la aplicación afectada a Vercel (frontend) o Render (Backend Core) bajo la condición de rama que acuerde el equipo. Consulta [GitHub Actions](../deployment/github-actions.md) para el diseño y las decisiones pendientes.

## Prácticas de contribución

- No incluyas secretos ni valores reales de configuración en los cambios.
- Actualiza las guías técnicas cuando cambien scripts, dependencias, variables de entorno o procedimientos.
- Consulta las convenciones de rama, commits, revisión y aprobación definidas por el equipo antes de asumir reglas adicionales; no están especificadas en esta documentación.
