## Context

Primer flujo local de Reserva Simple, con datos ficticios y sin usuarios reales.

## Goals / Non-Goals

Guardar y recuperar una reserva; explicar errores sin guardar registros incompletos.
Fuera: disponibilidad, pagos, multiusuario y despliegue público.

## Decisions

- Frontend React/Vite y backend Express en TypeScript dentro de `app/`.
- SQLite con Drizzle y una migración para reservas; archivo persistente fuera de Git.
- Modelo: id generado, cliente, servicio, fecha y hora. Zona horaria única acordada
  con el mentor y visible en pantalla. No convertir entre zonas en este ejercicio.
- `POST /api/reservas` valida texto tras quitar espacios y fecha/hora válidas;
  devuelve 201 con el registro o 400 con campos a corregir. Un fallo de almacenamiento
  devuelve un error genérico, sin detalles internos ni confirmación de éxito.
- `GET /api/reservas` devuelve la lista ordenada por fecha y hora; vacía al inicio.
- Mostrar éxito solo tras confirmar guardado. Ante error, conservar el formulario
  para corregir o reintentar; no añadir una fila ficticia a la lista.
- Servidores de desarrollo accesibles solo desde el equipo local en esta iteración.

## Risks / Trade-offs

Sin autenticación ni aislamiento entre usuarios, esta iteración no sirve todavía
para alojar reservas reales públicamente. SQLite simplifica el ejercicio; operación
remota y copias de seguridad se definirán antes del despliegue de la app.

## Migration Plan

Inicializar esquema local sin datos previos. Conservar cualquier base existente
antes de aplicar cambios. No incluir bases de datos ni secretos en commits.

## Open Questions

Confirmar zona horaria y setup del participante. Adaptar campos al proyecto real
antes de implementar; los comandos de arranque se documentarán tras comprobarlos.
