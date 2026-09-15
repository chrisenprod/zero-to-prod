# Ejemplo de proyecto · Reserva Simple

Caso ficticio para aprender a organizar tu proyecto durante el bootcamp. Avatar,
propuesta y decisiones son ejemplos pendientes de validar. No hay código implementado.

## Estructura

```text
zero-to-prod/                 ← raíz del repositorio
├── concepto.md               ← para quién y por qué
├── prd.md                    ← alcance del MVP
├── roadmap.md                ← entregas, decisiones y seguimiento
├── README.md
├── landing/                  ← sitio público HTML + CSS
├── app/                      ← aplicación
└── openspec/
    ├── config.yaml           ← contexto compartido
    ├── specs/                ← especificaciones vigentes
    └── changes/
        ├── publicar-landing/
        ├── registrar-reserva/
        └── archive/
```

Este repositorio contiene la base de ejemplo del proyecto del bootcamp. Para tu
producto, copia su contenido a tu propio repositorio y adapta el caso. `landing/`,
`app/` y `openspec/` quedan juntos en la raíz. Todo se guarda en un único repositorio
Git; `openspec/` contiene documentos y configuración. Ejecuta OpenSpec desde esta
raíz, no desde `app/`. Founder OS puede vivir en un repositorio independiente.

## Orden de trabajo en la sesión 2

1. Adaptar [concepto](concepto.md): avatar, problema y propuesta de valor.
2. Acordar el alcance del [PRD](prd.md), incluyendo el primer flujo útil.
3. Revisar las dos líneas de entrega del [roadmap](roadmap.md).
4. Revisar [publicar landing](openspec/changes/publicar-landing/proposal.md) y construirla.
5. En paralelo, preparar [registrar reserva](openspec/changes/registrar-reserva/proposal.md)
   y comenzar la app. No depende de que el dominio de la landing esté operativo.
6. Al cerrar: registrar qué funciona, evidencia, bloqueos y siguiente paso.

## Responsabilidad de cada documento

- Concepto: usuario, problema, propuesta e hipótesis. De aquí sale el mensaje de la landing.
- PRD: alcance y criterios de producto. Enlaza los cambios detallados.
- Roadmap: entregas y seguimiento. Las tareas detalladas viven en cada `tasks.md`.
- OpenSpec: propuesta, comportamiento, diseño y tareas de cada cambio concreto.
  Si cambia el alcance del producto, revisar también PRD y roadmap.

## Usar OpenSpec

La base incluida usa el esquema `spec-driven`. No se han generado integraciones
para asistentes ni ejecutado la implementación. Con la CLI instalada, desde la raíz de tu copia:

```sh
openspec init
openspec list
openspec validate --all --strict --no-interactive
```

En `init`, selecciona el asistente que usarás y revisa los archivos generados.
Pide al agente leer concepto, PRD y roadmap antes de trabajar en un cambio.
Revisa el plan, implementa, comprueba escenarios y marca solo tareas completadas.
Después sincroniza las especificaciones y archiva el cambio mediante OpenSpec;
actualiza su enlace en el roadmap.

`openspec/specs/` empieza vacío porque todavía no hay comportamiento implementado.
Los requisitos propuestos están en `changes/`.

Fuentes: [estructura y flujo oficial](https://github.com/Fission-AI/OpenSpec/blob/main/docs/getting-started.md)
y [configuración](https://github.com/Fission-AI/OpenSpec/blob/main/docs/customization.md).

## Adaptarlo

Sustituye el caso, las capacidades y los cambios por los de tu producto. No marques
hipótesis como validadas ni tareas como completadas por copiar la base. Acuerda fechas,
stack y acceso con el mentor. Publicar código, desplegar o contactar a personas
requiere autorización del dueño del proyecto. Usa datos ficticios durante el ejercicio.
