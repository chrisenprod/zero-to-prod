## Why

El primer flujo del PRD permite guardar y recuperar una cita acordada sin buscar
sus detalles en una conversación. La iteración usa datos ficticios localmente.

## What Changes

- Crear formulario y lista de reservas en `app/`.
- Validar cliente, servicio, fecha y hora en el backend.
- Guardar en SQLite y recuperar registros al recargar la interfaz.
- Excluir pagos, acceso multiusuario, despliegue público, automatización de WhatsApp,
  disponibilidad, edición y cancelación.

## Capabilities

### New Capabilities

- `reservas`: registrar y consultar reservas persistentes.

### Modified Capabilities

Ninguna; todavía no hay especificaciones vigentes.

## Impact

Afecta frontend, API, esquema y pruebas dentro de `app/`. Usa React/Vite,
TypeScript, Express, Drizzle y SQLite según el PRD. No modifica la landing.
