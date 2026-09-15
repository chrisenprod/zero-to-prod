# PRD · Reserva Simple

Estado: alcance didáctico propuesto, sin implementación.
Contexto de usuario y propuesta: [concepto](concepto.md).

## Objetivo de la primera versión

Un profesional registra una reserva y la encuentra después de recargar la app.
La primera iteración de la app funciona localmente con datos ficticios.

## Flujo principal

1. Abrir la aplicación y consultar la lista.
2. Completar cliente, servicio, fecha y hora.
3. Guardar; si un dato falta o es inválido, corregirlo con ayuda del mensaje.
4. Ver la reserva y recuperarla al recargar.

## Alcance y aceptación

| Frente | Incluye | Estará listo cuando |
|---|---|---|
| Landing | Propuesta, estado del proyecto y enlace a WhatsApp. | URL HTTPS usable en móvil y botón que abre el contacto acordado. |
| App | Alta manual y lista de reservas persistentes. | Guarda un registro válido, lo recupera al recargar y rechaza entradas inválidas. |

### Datos mínimos

Cliente y servicio (texto obligatorio), fecha y hora válidas. El sistema genera un
identificador. Se usa una única zona horaria acordada con el mentor, visible en
pantalla; no se convierte entre zonas ni se comprueba disponibilidad.

### Fuera de la primera iteración

Pagos, mensajes automáticos, API de WhatsApp, calendario externo, edición,
cancelación, comprobación de solapamientos y acceso de múltiples usuarios.
La reserva registra un acuerdo previo; no confirma disponibilidad automáticamente.

## Decisiones técnicas del ejemplo

- Landing independiente: HTML + CSS y assets locales.
- App: React + Vite + TypeScript, Node.js + Express y SQLite con Drizzle.
- SQLite es la elección para este ejemplo local; no implementamos dos motores.
- Landing pública: VPS + Nginx + dominio y HTTPS.
- App local: antes de exponer reservas reales o desplegar para clientes, definir
  autenticación, autorización y operación de los datos.

## Cambios de implementación

- [Publicar landing](openspec/changes/publicar-landing/proposal.md).
- [Registrar reserva](openspec/changes/registrar-reserva/proposal.md).

Los escenarios detallados y tareas viven en esos cambios. Fechas y avances están
en el [roadmap](roadmap.md).
