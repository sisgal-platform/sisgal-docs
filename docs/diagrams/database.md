# Modelo de datos de auditoría

> **Estado del diseño:** el esquema de esta página transcribe el modelo compartido en el diagrama de referencia. La base de auditoría está prevista como PostgreSQL independiente, pero aún no está conectada a SISGAL. Las tablas, relaciones y tipos deben contrastarse con las migraciones cuando se implemente.

El modelo separa los eventos generales de auditoría de los detalles opcionales del evento. No se especifican todavía restricciones de nulabilidad, índices, reglas de retención ni comportamiento de borrado.

## Entidades

### AuditUser

Identifica al usuario asociado a eventos de auditoría.

| Campo | Tipo | Descripción |
|---|---|---|
| `id` | UUID, PK | Identificador del usuario de auditoría. |
| `username` | VARCHAR | Nombre de usuario. |
| `email` | VARCHAR | Correo electrónico. |
| `role` | VARCHAR | Rol registrado para el usuario. |

### AuditEvent

Registra el evento y su contexto de solicitud.

| Campo | Tipo | Descripción |
|---|---|---|
| `id` | UUID, PK | Identificador del evento. |
| `user_id` | UUID, FK | Referencia a AuditUser. |
| `action` | VARCHAR | Acción realizada. |
| `entity` | VARCHAR | Tipo o nombre de entidad afectada. |
| `entity_id` | VARCHAR | Identificador de la entidad afectada. |
| `status` | VARCHAR | Estado registrado para el evento. |
| `http_status` | INT | Código HTTP asociado, si aplica. |
| `ip_address` | VARCHAR | Dirección IP registrada. |
| `user_agent` | VARCHAR | Agente de usuario registrado. |
| `created_at` | TIMESTAMP | Fecha y hora del evento. |
| `correlation_id` | UUID | Identificador para correlacionar operaciones. |

### AuditFieldChange

Almacena los cambios de campos asociados con un evento.

| Campo | Tipo | Descripción |
|---|---|---|
| `id` | UUID, PK | Identificador del cambio. |
| `event_id` | UUID, FK | Referencia a AuditEvent. |
| `field_name` | VARCHAR | Campo modificado. |
| `old_value` | TEXT | Valor anterior. |
| `new_value` | TEXT | Valor nuevo. |

### AuditMetadata

Almacena pares de clave y valor adicionales para un evento.

| Campo | Tipo | Descripción |
|---|---|---|
| `id` | UUID, PK | Identificador del metadato. |
| `event_id` | UUID, FK | Referencia a AuditEvent. |
| `key` | VARCHAR | Nombre del dato adicional. |
| `value` | TEXT | Valor del dato adicional. |

### AuditError

Almacena detalles de error asociados con un evento.

| Campo | Tipo | Descripción |
|---|---|---|
| `id` | UUID, PK | Identificador del error. |
| `event_id` | UUID, FK | Referencia a AuditEvent. |
| `error_message` | TEXT | Mensaje de error. |
| `stack_trace` | TEXT | Traza de pila registrada. |

### AuditSnapshot

Almacena una representación completa del estado asociado con un evento.

| Campo | Tipo | Descripción |
|---|---|---|
| `id` | UUID, PK | Identificador de la instantánea. |
| `event_id` | UUID, FK | Referencia a AuditEvent. |
| `full_state` | JSON | Estado completo capturado. |

## Relaciones del modelo

- Un AuditUser puede estar asociado con cero o varios AuditEvent; cada AuditEvent se vincula con un AuditUser según la relación dibujada.
- Un AuditEvent puede tener cero o varios AuditFieldChange, AuditMetadata, AuditError y AuditSnapshot.
- Cada registro de detalle pertenece a un AuditEvent mediante `event_id`.
- El diagrama no establece una relación entre AuditUser y la identidad de Supabase Auth; esa correspondencia queda por definir.
- La base de auditoría aún no recibe escrituras de la aplicación. Estas relaciones describen el diseño, no una integración ya operativa.

## Aspectos por definir al implementarlo

Validar nulabilidad y restricciones, valores admitidos para `action`, `status` y `role`, índices para consultas por usuario/fecha/correlación, política de retención, protección de datos sensibles en valores y trazas, permisos de acceso y reglas de borrado. No aplicar estos aspectos sin validarlos con el modelo de negocio y los requisitos de seguridad.
