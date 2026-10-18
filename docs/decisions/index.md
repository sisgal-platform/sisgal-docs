# Decisiones Técnicas

## Introducción

Esta sección documenta las principales decisiones tomadas durante el diseño y desarrollo de SISGAL. Su propósito es registrar los criterios utilizados para seleccionar tecnologías, definir aspectos arquitectónicos y establecer reglas de negocio que afectan el comportamiento del sistema.

Las decisiones documentadas buscan proporcionar trazabilidad sobre la evolución del proyecto y servir como referencia para el equipo durante las etapas de implementación, pruebas y mantenimiento.

## Tipos de decisiones

Las decisiones se organizan en tres categorías principales:

| Categoría | Descripción |
|---|---|
| **Stack tecnológico** | Tecnologías, herramientas y frameworks seleccionados para la implementación del sistema. |
| **Arquitectura** | Decisiones relacionadas con la estructura del sistema, distribución de responsabilidades y comunicación entre componentes. |
| **Reglas de negocio** | Reglas y parámetros que determinan el comportamiento funcional de la gestión de asistencia, novedades y liquidación de nómina. |

## Documentos

### Stack tecnológico

[Stack Tecnológico](technology-stack.md)

Documenta las tecnologías, frameworks, herramientas y servicios seleccionados para el desarrollo de SISGAL.

### Decisiones de arquitectura

[Decisiones de Arquitectura](architecture-decisions.md)

Documenta las principales decisiones relacionadas con la arquitectura del sistema y los criterios considerados para adoptarlas.

### Reglas de negocio

[Reglas de Negocio](business-rules.md)

Documenta las reglas y parámetros funcionales utilizados en los procesos de asistencia, novedades y liquidación de nómina.

## Relación con otras secciones

Las decisiones técnicas se relacionan con diferentes partes de la documentación:

```text
Requisitos
    ↓
Historias de usuario
    ↓
Decisiones técnicas
    ↓
Arquitectura
    ↓
Implementación
    ↓
Pruebas
```

Las decisiones arquitectónicas se complementan con la documentación de la sección Arquitectura, mientras que las reglas de negocio se relacionan con los conceptos descritos en la sección Dominio.

## Trazabilidad

Las decisiones registradas en esta sección deben poder relacionarse con:

- Requisitos y historias de usuario.
- Atributos y escenarios de calidad.
- Componentes arquitectónicos.
- Implementaciones realizadas.
- Pruebas del sistema.
- Cambios posteriores en el diseño.

Esta trazabilidad permite justificar las decisiones tomadas durante el desarrollo y facilita su revisión y mantenimiento.
