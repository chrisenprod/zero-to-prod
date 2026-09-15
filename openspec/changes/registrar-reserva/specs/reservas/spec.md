## ADDED Requirements

### Requirement: Registrar una reserva válida

La aplicación SHALL permitir guardar cliente y servicio no vacíos, fecha y hora
válidas, asignando un identificador a cada reserva confirmada por el backend.

#### Scenario: Guardar datos válidos

- **WHEN** el profesional completa todos los campos válidos y guarda
- **THEN** el backend confirma la creación y la reserva aparece en la lista
- **AND** la interfaz muestra la zona horaria acordada para interpretar la cita

### Requirement: Rechazar entradas inválidas

El backend SHALL rechazar campos obligatorios vacíos o compuestos solo de espacios,
fechas inexistentes y horas fuera de rango sin crear registros incompletos.

#### Scenario: Cliente vacío

- **WHEN** se envía una reserva cuyo cliente contiene solo espacios
- **THEN** el backend rechaza el guardado y la interfaz indica el campo a corregir
- **AND** la lista y la base conservan sus registros anteriores sin añadir uno nuevo

#### Scenario: Fecha u hora inválida

- **WHEN** se envía una fecha inexistente o una hora como 25:70
- **THEN** el backend rechaza el dato e indica qué corregir sin crear la reserva

### Requirement: Recuperar reservas persistentes

La aplicación SHALL recuperar desde el backend las reservas guardadas al abrirse
y mantenerlas después de reiniciar el backend usando la misma base local.

#### Scenario: Recargar después de guardar

- **WHEN** se recarga la página después de guardar una reserva
- **THEN** se ve la misma reserva con sus datos e identificador

#### Scenario: Reiniciar el backend

- **WHEN** se reinicia el backend con la misma base SQLite y se abre la aplicación
- **THEN** las reservas guardadas siguen disponibles

#### Scenario: Lista inicialmente vacía

- **WHEN** se abre la app sin reservas registradas
- **THEN** se muestra un estado vacío que invita a crear la primera reserva

### Requirement: Mostrar fallos de guardado sin confirmar éxito

La aplicación SHALL informar cuando el backend no confirma el guardado y conservar
los datos introducidos para permitir corregir o reintentar.

#### Scenario: Backend no disponible

- **WHEN** el profesional intenta guardar mientras el backend no está disponible
- **THEN** ve un mensaje de error y conserva los datos del formulario
- **AND** no se muestra confirmación de éxito ni una reserva nueva en la lista
