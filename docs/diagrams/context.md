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
- El dispositivo biométrico envía registros de asistencia a SISGAL.
