# Diagrama de contexto (C4)

El diagrama presenta SISGAL desde fuera: quién interactúa con la plataforma y qué sistemas externos intercambian información con ella. Este nivel ayuda a delimitar el alcance del sistema, sin describir sus módulos internos.

![Diagrama de contexto C4 de SISGAL](images/context.svg)

[Ver fuente PlantUML](source/context.puml)

## Elementos

- **Administrador:** gestiona empleados, configura reglas y genera nómina.
- **Empleado:** registra asistencia.
- **SISGAL:** sistema que reúne el registro de asistencia, el cálculo de nómina y la gestión de reglas laborales.
- **Dispositivo biométrico:** envía registros de asistencia.
- **Sistemas externos:** consumen información mediante la API expuesta por SISGAL.

## Relaciones

- El administrador y el empleado usan SISGAL para las tareas descritas en sus responsabilidades.
- SISGAL expone una API REST para que sistemas externos consuman información.
- La integración con el dispositivo biométrico permite recibir registros de asistencia.

> **Punto por confirmar:** en el diagrama, la flecha de la relación de asistencia va de SISGAL hacia el dispositivo, aunque su etiqueta dice que SISGAL recibe datos. El sentido de la flecha y el texto no coinciden; conviene confirmar cuál debe corregirse.
