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

## Comienza aquí

1. Copia esta base a tu propio repositorio. Si la recibiste dentro de `proyecto/`
   en el material del curso, copia su contenido a la raíz del repo del producto.
2. Completa [concepto.md](concepto.md): avatar, problema, propuesta e hipótesis.
3. Acuerda el primer flujo y los límites en [prd.md](prd.md).
4. Define las entregas de landing y app en [roadmap.md](roadmap.md).
5. Confirma las tecnologías y prepara OpenSpec desde la raíz del proyecto.
6. Define un primer cambio pequeño, revisa su plan y comienza a construir.

Los campos entre corchetes se completan con información del proyecto. Distingue
hipótesis de evidencia y registra lo que todavía no está decidido.

## Landing y MVP en paralelo

La landing toma su mensaje del concepto. La app se construye a partir del PRD.
Ambas comparten roadmap y pueden avanzar en paralelo; el primer flujo de la app
no depende de que la landing ya tenga dominio y HTTPS.

Cada carpeta empieza con un README. Todavía no hay código, dependencias instaladas,
funciones implementadas ni un producto o stack elegido.

## Cómo repartir la información

| Lugar | Qué mantener aquí |
|---|---|
| Concepto | Usuario, problema, propuesta de valor e hipótesis. |
| PRD | Flujos, alcance, exclusiones y criterios de aceptación del MVP. |
| Roadmap | Entregas, orden, estado, evidencia, bloqueos y próxima tarea. |
| OpenSpec | Propuesta, especificaciones, diseño y tareas de cada cambio concreto. |

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
