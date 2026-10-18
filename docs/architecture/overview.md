# Visión general de la arquitectura

## Introducción

SISGAL fue diseñado como una aplicación web orientada a automatizar el proceso de gestión de asistencia y liquidación de nómina para pequeñas organizaciones del sector gastronómico colombiano.

La solución integra en una única plataforma los procesos de registro de asistencia, administración de empleados y cálculo de la nómina, reduciendo la dependencia de procesos manuales y mejorando la precisión de los resultados.

---

## Estilo arquitectónico

El **backend core** de SISGAL adopta una arquitectura de monolito modular: sus módulos funcionales comparten una base de código y se despliegan como una aplicación integrada. El core implementa la lógica principal del sistema.

La conexión con el dispositivo biométrico se realiza mediante un microservicio de backend independiente. Por tanto, SISGAL tiene dos servicios de backend, pero la decisión de monolito modular aplica solamente al core.

---

## Principios de diseño

Durante el diseño del sistema se definieron los siguientes principios arquitectónicos:

- Alta cohesión entre componentes de un mismo módulo.
- Bajo acoplamiento entre módulos.
- Separación entre lógica de negocio e infraestructura.
- Modularidad.
- Escalabilidad horizontal futura.
- Trazabilidad de la información.
- Seguridad desde el diseño.

---

## Organización general

La solución contempla estas aplicaciones y servicios:

- Frontend desarrollado en React.
- Backend core desarrollado en NestJS, organizado como monolito modular.
- Microservicio de backend dedicado a la conexión con el dispositivo biométrico.

El frontend se comunica con el core mediante una API REST.

Los datos del sistema y las marcaciones se persisten en la base principal PostgreSQL mediante TypeORM. La base de auditoría es independiente y también utiliza PostgreSQL; su flujo de escritura está pendiente de definición.

---

## Arquitectura de alto nivel

- [Diagrama de contexto (C4, Nivel 1)](../diagrams/context.md)
- [Diagrama de contenedores (C4, Nivel 2)](../diagrams/containers.md)
- [Componentes (C4, Nivel 3)](../diagrams/components.md)
- [Vista de despliegue](../diagrams/deployment.md)

## Componentes principales

Actualmente el sistema está compuesto por los siguientes componentes:

| Componente | Responsabilidad |
|------------|-----------------|
| Frontend | Interfaz de usuario |
| Backend core | Procesamiento de las reglas principales de negocio mediante módulos funcionales |
| Base de datos principal | Persistencia del sistema y de las marcaciones biométricas |
| Base de datos de auditoría | Almacenamiento independiente; integración aún por definir |
| Microservicio de integración biométrica | Conexión con el dispositivo biométrico |

## Módulos funcionales

La lógica del negocio se organiza en módulos independientes.

Entre los principales módulos se encuentran:

- Autenticación
- Empleados
- Asistencia
- Jornadas laborales
- Liquidación de nómina
- Configuración


Se propone un módulo transversal de auditoría, pero su alcance e integración todavía están por definir.

Cada módulo encapsula sus casos de uso, entidades, reglas de negocio y mecanismos de persistencia según corresponda.

La comunicación entre módulos se realiza mediante interfaces bien definidas, evitando dependencias innecesarias entre ellos.

## Calidad de la arquitectura

El diseño arquitectónico fue guiado por atributos de calidad priorizados durante la etapa de análisis.

Los principales atributos considerados fueron:

- Mantenibilidad
- Seguridad
- Disponibilidad
- Rendimiento
- Escalabilidad
- Modificabilidad

Estos atributos dieron origen a las tácticas arquitectónicas implementadas y a las decisiones de diseño descritas en las siguientes secciones.