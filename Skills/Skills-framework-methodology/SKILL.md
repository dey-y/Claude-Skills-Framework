---
name: skills-framework-methodology
description: >
  Metodología propia del usuario para crear, estructurar, redactar, gestionar y
  versionar Skills de Claude. Úsala cuando el usuario pida crear una skill nueva,
  decidir si una tarea merece convertirse en skill, definir el naming o estructura
  de carpeta de una skill, redactar o mejorar un SKILL.md, resolver solapamientos
  o ambigüedad de trigger entre skills existentes, o gestionar el ciclo de vida
  (borrador, validación, publicación, versionado, deprecación) de una skill. Activa
  esta skill siempre que la tarea sea sobre el propio sistema de skills, no sobre
  el contenido final que la skill vaya a producir.
---

# Claude Skills Framework

Metodología del usuario para gestionar el ciclo de vida completo de sus Skills.
Este archivo es un índice. Antes de crear, editar o evaluar una skill, consulta
el/los documentos de `references/` que correspondan a la fase en la que estás.

## Índice de referencias

- **`references/01-criterios-scope.md`** — Consúltalo primero, siempre, antes de
  decidir si una tarea justifica crear una skill nueva. Define las 3 condiciones
  de entrada (repetible, procedimental, delimitable) y el test de responsabilidad
  única.

- **`references/02-estructura-naming.md`** — Consúltalo al definir la carpeta y
  el nombre de una skill nueva. Define estructura de carpeta, patrones de naming
  (formato/herramienta vs. conceptual) y la regla de exclusividad de dominio.

- **`references/03-guia-autoria-skillmd.md`** — Consúltalo al redactar el
  `SKILL.md` (frontmatter + cuerpo) de una skill nueva o al mejorar una existente.
  Define cómo escribir `description` (sesgo "pushy") y el cuerpo (límite de
  líneas, estilo imperativo, cuándo usar `references/`).

- **`references/04-gestion-ecosistema.md`** — Consúltalo cuando haya (o pueda
  haber) más de una skill compitiendo por el mismo trigger, o dudas sobre si una
  skill nueva solapa dominio con una existente. Define el registro central, la
  regla de no-solapamiento y su excepción (segmentación por fase), y cómo
  resolver ambigüedad de trigger.

- **`references/05-ciclo-vida.md`** — Consúltalo para seguir el proceso completo
  de principio a fin: borrador → redacción → validación (checklist) → publicación
  → versionado → deprecación.

## Registro central (registry.md)

El `registry.md` es un estado vivo (lista de skills creadas y su estado), no
metodología estática — por eso vive fuera de esta skill, en el proyecto del
usuario, y no dentro de `references/`. Pídeselo al usuario o localízalo en el
proyecto antes de crear cualquier skill nueva; es necesario para aplicar de
forma mecánica el criterio "Delimitable" (Documento 1) y la gestión de
ecosistema (Documento 4).

## Cómo aplicar esta metodología

1. Identifica en qué fase del ciclo de vida está la tarea (ver Documento 5).
2. Carga solo el/los documentos de `references/` relevantes para esa fase — no
   cargues los 5 si solo necesitas uno.
3. Sigue el proceso de `documentation-architect` si el usuario también ha
   activado ese rol (analizar → proponer → desarrollar → autoevaluar → corregir
   → esperar aprobación). Esta skill aporta el *contenido* metodológico; no
   sustituye el proceso de trabajo documento-por-documento.
