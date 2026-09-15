## Context

Página estática para el concepto Reserva Simple. App todavía no implementada.

## Goals / Non-Goals

Mostrar propuesta, estado del proyecto y contacto. Fuera: formularios, frameworks,
backend y afirmaciones de ventas o clientes que no existen.

## Decisions

- Crear `landing/index.html`, `landing/styles.css` y assets con rutas relativas.
- Tomar el mensaje de `concepto.md`; no anunciar una app terminada.
- Usar un enlace `wa.me` con el número internacional autorizado, solo dígitos.
- Publicar únicamente los archivos del sitio en una carpeta dedicada del VPS.
- Comprobar Nginx antes de recargar y después verificar dominio y HTTPS.

## Risks / Trade-offs

DNS o acceso pueden bloquear publicación; la revisión local permite avanzar,
pero no equivale a una URL final. La app puede comenzar de forma independiente.

## Migration Plan

No hay datos que migrar. Antes del deploy autorizado, registrar destino y conservar
la versión anterior si existe. Si falla la comprobación, restaurar esa versión.

## Open Questions

Número de contacto, dominio, VPS, acceso y carpeta de destino por acordar con el mentor.
