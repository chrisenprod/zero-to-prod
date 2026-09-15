# Zero to Prod · Plantilla de proyecto

Base para comenzar un proyecto desde cero durante el bootcamp De 0 a Producción
con IA. Completa el contexto de tu producto, define su primera versión y construye
la landing y la aplicación con un seguimiento compartido.

## Estructura

```text
mi-proyecto/                  ← raíz de tu repositorio
├── concepto.md               ← avatar, problema y propuesta de valor
├── prd.md                    ← alcance y requisitos de la primera versión
├── roadmap.md                ← entregas, decisiones y seguimiento
├── README.md
├── landing/                  ← web pública
├── app/                      ← aplicación / MVP
└── openspec/
    ├── config.yaml           ← contexto y reglas de trabajo
    ├── specs/                ← especificaciones vigentes
    └── changes/              ← propuestas de cambios
        └── archive/          ← cambios completados
```

Todo vive en un único repositorio Git. `openspec/` contiene documentos y
configuración; no es otro repositorio. Founder OS y otros productos pueden vivir
en repositorios independientes.

## Comienza aquí: construye el proyecto conversando con tu agente

Copia esta base a tu propio repositorio y ábrelo con tu agente de código. Si la
recibiste dentro de `proyecto/` en el material del curso, copia su contenido a la
raíz del repo del producto.

La interacción ocurre en la conversación con tu agente. Este README le da el
procedimiento; los tres documentos guardan lo que van definiendo juntos. No tienes
que responder un formulario completo antes de empezar.

### Mensaje para comenzar

Copia este mensaje en la conversación:

> Lee el README de este repositorio y acompáñame a definir mi proyecto mediante
> el proceso de co-creación que describe. Revisa primero concepto.md, prd.md y
> roadmap.md para saber qué está completo y qué falta. Hazme de una a tres preguntas
> por turno, espera mis respuestas y ayúdame a concretar lo que todavía no sé.
> Construyamos primero el concepto, después el PRD y luego el roadmap. Propón el
> texto de cada bloque a partir de mis respuestas y revísalo conmigo antes de
> guardarlo como acordado. No completes todo de una vez ni inventes decisiones.
> Comienza por lo que ya tengo, para quién quiero construir y qué problema veo.

### Instrucciones para el agente facilitador

1. **Ubica el punto de partida.** Lee los documentos y las fuentes que el usuario
   indique. Si ya hay contenido, resume lo definido y pregunta por los vacíos;
   continúa desde ahí sin repetir preguntas resueltas ni borrar trabajo previo.
2. **Conversa por bloques.** Haz de una a tres preguntas relacionadas por turno.
   Usa lenguaje sencillo y explica un término cuando sea necesario. Espera la
   respuesta antes de continuar; no entregues toda la entrevista en un mensaje.
3. **Ayuda a decidir.** Si el usuario no sabe, ofrece dos o tres opciones con una
   explicación breve o pide un ejemplo de su trabajo. Una recomendación tuya sigue
   siendo una propuesta hasta que el usuario la acepte. Si falta información,
   pueden dejarla pendiente e indicar qué bloquea.
4. **Devuelve lo entendido.** Resume las respuestas y propón el texto del bloque.
   Pregunta si lo refleja bien o qué ajustaría. Usa sus correcciones para escribir.
   Si pide guardar un borrador, consérvalo identificado como tal.
5. **Guarda con contexto.** Actualiza el documento correspondiente con lo acordado,
   su fecha, hipótesis y pendientes. No conviertas ejemplos en requisitos ni
   afirmaciones del usuario en evidencia verificada sin una fuente que las respalde.
6. **Cierra una etapa antes de abrir la siguiente.** Presenta una síntesis y los
   pendientes relevantes. Pregunta si el usuario quiere ajustar algo o continuar;
   no tomes el silencio como respuesta. Si ya indicó continuar, respeta esa decisión.
7. **Retoma sin empezar de cero.** Al cerrar o pausar, resume qué quedó definido,
   dónde se guardó y la siguiente pregunta o decisión. Usa las secciones de
   pendientes del concepto/PRD y el siguiente paso del roadmap para conservarlo.

### Recorrido de la conversación

| Etapa | Qué explorar con el usuario | Qué guardar |
|---|---|---|
| 1. Concepto | Situación, avatar, problema, alternativa actual, resultado, propuesta e hipótesis. | [concepto.md](concepto.md) |
| 2. PRD | Primer flujo útil, alcance, exclusiones, reglas y cómo comprobar el resultado. | [prd.md](prd.md) |
| 3. Roadmap | Estado actual, tiempo disponible, dependencias, entregas y próxima acción. | [roadmap.md](roadmap.md) |
| 4. Primer cambio | Qué entrega comenzará, comportamiento esperado, diseño y tareas. | Un cambio en `openspec/changes/`, cuando se decida crearlo. |

Cada documento incluye preguntas de apoyo. Elige solo las relevantes según las
respuestas: no son un cuestionario para enviar completo. Las decisiones técnicas
se conversan después de entender el flujo; no son un requisito para describir la idea.

Al terminar la definición, el agente presenta lo acordado y pregunta con qué
entrega comenzar. Completar los documentos no implica implementar, publicar ni
desplegar automáticamente; esas acciones siguen el encargo del usuario.

## Landing y MVP en paralelo

La landing toma su mensaje del concepto. La app se construye a partir del PRD.
Ambas comparten roadmap y pueden avanzar en paralelo; el primer flujo de la app
no depende de que la landing ya tenga dominio y HTTPS.

Cada carpeta empieza con un README. Todavía no hay código, dependencias instaladas,
funciones implementadas ni un producto o stack elegido.

## Cómo repartir la información

| Lugar | Pregunta que responde | Qué mantener aquí |
|---|---|---|
| [Concepto](concepto.md) | ¿Para quién y por qué? | Usuario, problema, propuesta de valor e hipótesis. |
| [PRD](prd.md) | ¿Qué debe hacer el producto? | Flujos, alcance, exclusiones y criterios de aceptación del MVP. |
| [Roadmap](roadmap.md) | ¿Qué entregamos primero y cómo vamos? | Entregas, orden, estado, evidencia, bloqueos y próxima tarea. |
| OpenSpec | ¿Qué cambia en esta iteración y cómo lo implementamos? | Propuesta, especificaciones, diseño y tareas de cada cambio concreto. |

Cada uno de los tres documentos comienza con instrucciones: información de partida,
pasos para completarlo, un encargo que puedes dar a tu agente, criterios para avanzar
y cuándo actualizarlo. Trabájalos en este orden: concepto → PRD → roadmap → primer
cambio OpenSpec. Después se mantienen conectados a medida que aprendes y construyes.

El roadmap es único. Las tareas detalladas de implementación viven en OpenSpec.
Si una decisión cambia el alcance del producto, actualiza también el PRD.

## Preparar OpenSpec

La plantilla incluye `config.yaml` con el esquema `spec-driven`. Las carpetas de
especificaciones y cambios empiezan vacías; no hay propuestas predefinidas ni
integraciones de asistentes generadas.

Con la CLI instalada, ejecuta desde la raíz del proyecto:

```sh
openspec init
```

Selecciona el asistente que usarás y revisa los archivos generados. Pide al agente
que lea concepto, PRD y roadmap antes de proponer el primer cambio. Revisa alcance,
comportamiento esperado y tareas antes de implementar.

Cuando exista un cambio, puedes consultar y validar sus documentos desde la terminal:

```sh
openspec list
openspec validate --all --strict --no-interactive
```

La validación comprueba los documentos; también tendrás que probar lo construido.
Al completar un cambio, sincroniza sus especificaciones y archívalo mediante
OpenSpec. Registra la evidencia y actualiza el enlace en el roadmap.

Guías oficiales: [instalación](https://github.com/Fission-AI/OpenSpec/blob/main/docs/installation.md),
[flujo de trabajo](https://github.com/Fission-AI/OpenSpec/blob/main/docs/getting-started.md)
y [configuración](https://github.com/Fission-AI/OpenSpec/blob/main/docs/customization.md).

## Al cerrar cada sesión

Registra en el roadmap qué funciona, cómo lo comprobaste, qué bloquea el avance y
cuál es la próxima tarea. Marca completado solo lo que puedas demostrar.

Mantén secretos y datos privados fuera de Git. Acuerda con el dueño del proyecto
la publicación de código, los despliegues y los contactos con personas.
