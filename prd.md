# PRD · [Nombre del proyecto]

Documento de requisitos del producto: define qué debe hacer la primera versión.

**Estado:** [Borrador / alcance acordado / en revisión].
**Última actualización:** [Fecha].
**Contexto:** [Concepto, avatar y propuesta de valor](concepto.md).

## Cómo construir este documento

**Pregunta que responde:** ¿Qué debe hacer la primera versión y cómo sabremos que funciona?

**Antes de empezar:** lee [concepto.md](concepto.md), revisa lo que ya existe del
producto y acuerda cuánto puedes construir en esta primera iteración.

1. Elige un resultado útil del concepto y conviértelo en un primer flujo completo:
   desde la acción inicial del usuario hasta el resultado que recibe.
2. Define qué incluye esa versión y qué queda fuera. Describe también el papel de
   la landing y su acción principal.
3. Escribe criterios observables. Por ejemplo, «al recargar sigue viendo el dato
   guardado» permite comprobar una entrega; «funciona bien» no basta.
4. Aclara datos, validaciones, acceso, errores y estados vacíos según el flujo.
5. Acuerda las decisiones técnicas necesarias. Si una pieza no hace falta, indícalo;
   si falta una decisión, registra qué bloquea en lugar de inventarla.
6. Revisa el alcance con el dueño del proyecto. Después enlaza los cambios OpenSpec
   que desarrollen cada capacidad; no necesitas crearlos para redactar este PRD.

### Co-crearlo en conversación

Sigue el proceso interactivo del [README](README.md) y parte del concepto ya
trabajado. Explica PRD como «lo que debe hacer la primera versión».

- **Resultado:** ¿Qué única tarea debería poder completar el primer usuario?
- **Recorrido:** ¿Dónde empieza, qué hace y qué debería obtener al terminar?
- **Límites:** ¿Qué es indispensable y qué podemos dejar para después?
- **Reglas:** ¿Qué datos necesita? ¿Qué debería pasar si falta algo o hay un error?
  ¿Quién puede consultar o modificar la información, si corresponde?
- **Comprobación:** ¿Qué tendríamos que observar para decir que funciona?

Haz de una a tres preguntas por turno; utiliza las respuestas para proponer el
siguiente bloque. Ayuda a reducir el alcance cuando sea necesario y explica las
opciones técnicas en función del flujo. No exijas al usuario conocer el stack.
Al cerrar, revisa flujo, exclusiones y aceptación con él antes de pasar al roadmap.
Conserva las decisiones sin resolver en «Preguntas abiertas».

**Encargo para tu agente:**

> Lee concepto.md y el estado actual del proyecto. Ayúdame a completar prd.md para
> una primera versión pequeña y útil. Pregunta por las decisiones que cambien el
> comportamiento del producto. Propón un flujo, sus límites y criterios observables,
> incluidos los errores relevantes. Mantén las incertidumbres explícitas y presenta
> el alcance para revisión antes de implementar.

**Listo para continuar cuando:** otra persona entiende el primer flujo, sus reglas,
lo que queda fuera y cómo comprobarlo. Las decisiones que bloqueen el primer cambio
están resueltas; las de entregas posteriores pueden seguir identificadas como pendientes.

**Cuándo actualizarlo:** cuando cambie el comportamiento o alcance acordado.
El orden, las fechas y el avance van en [roadmap.md](roadmap.md). El diseño detallado,
los escenarios y las tareas de cada cambio se desarrollan en OpenSpec.

Los campos siguientes definen tu producto; los ejemplos de esta guía no son requisitos.

## 1. Objetivo de la primera versión

> Al finalizar, **[usuario]** podrá **[acción concreta]** para conseguir **[resultado útil]**.

## 2. Primer flujo útil

1. [Dónde empieza el usuario y qué necesita para entrar].
2. [Qué información introduce o qué acción realiza].
3. [Qué valida y hace el sistema].
4. [Qué resultado recibe y cómo lo vuelve a consultar, si corresponde].

## 3. Alcance y criterios de aceptación

| Frente | Qué incluye | Cómo comprobaremos que está listo |
|---|---|---|
| Landing | [Mensaje, contenido y acción principal] | [Resultado observable desde la web pública] |
| App / MVP | [Primer flujo completo y funciones imprescindibles] | [Acción del usuario y resultado esperado] |

### Fuera de esta primera versión

- [Función o integración que dejaremos para después].
- [Límite acordado para mantener la entrega realizable].

## 4. Datos y reglas principales

- **Información necesaria:** [Campos mínimos y su propósito].
- **Validaciones:** [Qué entradas se aceptan y cuáles se rechazan].
- **Persistencia:** [Qué debe guardarse y recuperarse después].
- **Acceso:** [Quién puede ver o modificar cada dato, cuando corresponda].
- **Errores y estados vacíos:** [Qué verá el usuario si falta información o algo falla].

## 5. Decisiones técnicas

Completar con el mentor antes de implementar; no hay stack seleccionado por esta plantilla.

| Pieza | Decisión | Motivo / pendiente |
|---|---|---|
| Landing | [Tecnología] | [Motivo] |
| Interfaz de la app | [Tecnología] | [Motivo] |
| Backend | [Tecnología o no requerido] | [Motivo] |
| Datos | [Motor o no requerido] | [Motivo] |
| Entorno inicial | [Local / otro] | [Condiciones para probar] |
| Publicación | [Destino previsto] | [Acceso y decisiones pendientes] |

## 6. Cambios de implementación

Después de acordar el alcance, crea cada cambio concreto en `openspec/changes/`
y registra su enlace aquí. Sus especificaciones desarrollan los escenarios detallados.

| Cambio | Qué parte del alcance implementa | Enlace OpenSpec |
|---|---|---|
| [Nombre del primer cambio] | [Flujo o capacidad] | Pendiente de crear |

## 7. Preguntas abiertas

- [Decisión que falta, quién la resuelve y qué parte bloquea].

Entregas, fechas y avances: [roadmap](roadmap.md).
