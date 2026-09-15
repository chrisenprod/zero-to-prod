## ADDED Requirements

### Requirement: Presentar el proyecto con claridad

La landing SHALL mostrar la propuesta de concepto.md, indicar que la aplicación
está en desarrollo y permitir leer el contenido desde un teléfono.

#### Scenario: Revisar la propuesta en móvil

- **WHEN** una persona abre la landing con un ancho de pantalla de 375 píxeles
- **THEN** puede leer propuesta y estado del proyecto sin desplazamiento horizontal
- **AND** las imágenes y estilos locales cargan sin rutas rotas

### Requirement: Iniciar contacto por WhatsApp

La landing SHALL incluir un botón «Hablar por WhatsApp» dirigido al contacto
acordado, sin enviar mensajes automáticamente.

#### Scenario: Abrir el contacto

- **WHEN** la persona pulsa el botón desde un teléfono con WhatsApp disponible
- **THEN** se abre la conversación con el número acordado
- **AND** ningún mensaje se envía sin una acción adicional de la persona

#### Scenario: Detectar un destino pendiente antes de publicar

- **WHEN** la revisión encuentra un número de ejemplo o un contacto sin confirmar
- **THEN** la entrega se mantiene pendiente de publicación hasta corregir el destino

### Requirement: Entregar una URL pública comprobada

La entrega SHALL abrir por HTTPS fuera del equipo local, con sus recursos disponibles.

#### Scenario: Verificar la publicación

- **WHEN** el participante abre la URL desde un teléfono usando datos móviles
- **THEN** la página carga con conexión HTTPS sin advertencias de certificado
- **AND** puede volver a comprobar el botón y sus recursos

#### Scenario: Dominio o HTTPS pendientes

- **WHEN** la página solo responde localmente o por IP sin HTTPS final
- **THEN** el roadmap registra el bloqueo y mantiene la entrega pública pendiente
