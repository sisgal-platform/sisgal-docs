# Diagrama de contexto (C4)

El diagrama presenta los actores que usan SISGAL y los sistemas externos que intercambian información con la plataforma.

```plantuml
@startuml C4_Context
!include https://raw.githubusercontent.com/plantuml-stdlib/C4-PlantUML/master/C4_Context.puml

Person(admin, "Administrador", "Gestiona empleados, configura reglas y genera nómina")
Person(employee, "Empleado", "Registra asistencia")

System(system, "Sistema de Gestión de Asistencia y Nómina", "Permite registrar asistencia, calcular nómina y gestionar reglas laborales")

System_Ext(biometric, "Dispositivo Biométrico", "Envía registros de asistencia")
System_Ext(external_api, "Sistemas externos", "Consumen información vía API")

Rel(admin, system, "Usa el sistema")
Rel(employee, system, "Registra asistencia")

Rel(system, biometric, "Recibe datos de asistencia")
Rel(system, external_api, "Expone API REST")

@enduml
```
