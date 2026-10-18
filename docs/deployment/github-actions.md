# Pipelines con GitHub Actions

## Estado

Los workflows de CI/CD aún no se han añadido a los repositorios de las aplicaciones. Esta guía y los archivos de ejemplo son plantillas para incorporar después al repositorio del frontend y al del Backend Core. No se ejecutan desde este repositorio de documentación.

Se recomienda **SonarQube Cloud** como punto de partida porque todavía no hay una instancia SonarQube configurada. Si el equipo elige SonarQube Server, habrá que configurar también `SONAR_HOST_URL`.

## Flujo propuesto

Cada aplicación tiene su propio workflow:

1. En un Pull Request hacia `develop`, ejecuta análisis estático local, pruebas con cobertura mínima de líneas del 80%, compilación y análisis Sonar.
2. La validación de Sonar espera el Quality Gate. Si falla una validación, el workflow falla.
3. En un push a `develop`, cuando todas las validaciones pasen, se publica solo la aplicación correspondiente:
   - Frontend React en Vercel.
   - Backend Core NestJS en Render.
4. El microservicio biométrico no se incluye porque no está implementado.

Las plantillas se encuentran en [frontend-ci.yml](examples/frontend-ci.yml) y [backend-ci.yml](examples/backend-ci.yml). Están preparadas para repositorios con una aplicación en su raíz; se deben adaptar si las aplicaciones viven en un monorepo.

## Configuración necesaria antes de usarlas

### Node.js y npm

- Define la variable de repositorio `NODE_VERSION` con la versión exacta de Node.js acordada por el equipo.
- Usa npm y conserva `package-lock.json` en el repositorio para que `npm ci` pueda instalar dependencias de forma reproducible.
- La versión exacta de Node.js todavía no está fijada en los manifiestos compartidos.

### Cobertura

Las plantillas aplican un mínimo global de **80% en cobertura de líneas**:

- Frontend: Vitest genera el reporte LCOV para Sonar y falla si las líneas cubiertas son inferiores al umbral.
- Backend Core: Jest recibe el umbral global mediante `coverageThreshold` y genera `coverage/lcov.info`.

El 80% es una condición de las pruebas del workflow. Si el equipo también quiere usar el mismo mínimo como condición de Sonar, debe crear o ajustar el Quality Gate para exigir al menos 80% de cobertura en código nuevo. El umbral de cobertura de Sonar se configura en SonarQube Cloud, no en el YAML.

### SonarQube Cloud

1. Crear la cuenta/organización de SonarQube Cloud e importar cada repositorio de GitHub como proyecto.
2. Crear un token de análisis y guardarlo como secreto `SONAR_TOKEN` en cada repositorio.
3. Crear estas variables de repositorio para cada aplicación:
   - `SONAR_ORGANIZATION`: clave de la organización de Sonar.
   - `SONAR_PROJECT_KEY`: clave del proyecto Sonar.
   - `SONAR_SOURCES`: rutas reales del código fuente que se deben analizar; validar este valor con la estructura de cada repositorio.
4. Configurar el Quality Gate y vincular el proyecto con GitHub.
5. Añadir el estado de Sonar y el job de validación a los checks obligatorios de la rama `develop).

El token de Sonar y los tokens de despliegue son secretos. No deben escribirse en los archivos YAML.

### Vercel

Para el job del frontend, agrega al entorno de GitHub Actions usado por el workflow:

- Secreto `VERCEL_TOKEN`.
- Variables `VERCEL_ORG_ID` y `VERCEL_PROJECT_ID`.

Las variables `VITE_SUPABASE_URL`, `VITE_SUPABASE_ANON_KEY` y `VITE_API_URL` deben estar configuradas en Vercel y como variables de repositorio de GitHub para que el job de validación pueda compilar. Son valores públicos de cliente; no agregues la clave de servicio de Supabase al frontend.

El ejemplo despliega como Preview desde `develop`. Para Render, el Deploy Hook debe apuntar a un servicio de pruebas enlazado a `develop`, separado del servicio de producción.

### Render

Para el job del Backend Core, crea un Deploy Hook del servicio Render y almacena su URL como secreto `RENDER_DEPLOY_HOOK_URL`. Vincula el servicio Render a la rama `develop` y desactiva su despliegue automático por push si GitHub Actions será el único mecanismo de publicación; así se evitan despliegues duplicados.

Las variables `SUPABASE_DB_URL` y `SUPABASE_URL` permanecen configuradas en el entorno de ejecución del servicio Render. No se imprimen ni se transfieren como valores de salida del pipeline.

## Detalles que faltan para activar despliegues

- Versión exacta de Node.js.
- Proyectos y token de SonarQube Cloud.
- IDs y token del proyecto Vercel.
- Deploy Hook de Render y confirmación de la rama/environment de destino.
- Reglas de protección de `develop` y aprobación de despliegues.
- Procedimiento de rollback y verificación de salud del servicio.
- Confirmar que Vercel no esté generando despliegues automáticos duplicados para los mismos cambios.

Para configurar secretos y limitar su acceso a un entorno, usa la configuración de [GitHub Actions Environments y secrets](https://docs.github.com/en/actions/concepts/workflows-and-actions/deployment-environments) y sigue las guías oficiales de [SonarQube Cloud](https://docs.sonarsource.com/sonarqube-cloud/analyzing-source-code/test-coverage/javascript-typescript-test-coverage), [Vercel con GitHub Actions](https://vercel.com/kb/guide/how-can-i-use-github-actions-with-vercel) y [Deploy Hooks de Render](https://render.com/docs/deploy-hooks).
