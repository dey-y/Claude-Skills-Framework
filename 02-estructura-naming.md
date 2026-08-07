# Documento 2 — Estructura y naming

## Estructura de carpeta

Basada en el mecanismo real de carga de Skills (progressive disclosure: metadata → SKILL.md → recursos bajo demanda).

```
skill-name/
├── SKILL.md          (obligatorio)
├── scripts/           (opcional — código ejecutable determinista)
├── references/         (opcional — docs cargados bajo demanda; índice si hay más de 1 archivo o >300 líneas)
└── assets/             (opcional — plantillas, iconos, archivos usados en el output)
```

## Naming

### Subtipo A — Skills de formato/herramienta
Patrón: `[dominio]-[acción]`
- `[dominio]` = formato o herramienta principal (pdf, docx, xlsx, pptx...), único en todo el catálogo.
- `[acción]` = opcional, solo si la skill no cubre todo el dominio (ej. `pdf-merge` vs. `pdf` a secas si cubre todo lo relacionado con PDF).

### Subtipo B — Skills conceptuales o de comportamiento
No tienen dominio-formato ni acción clara (guías de estilo, conocimiento de producto, rutinas). 
- Nombre único descriptivo, una o dos palabras, sin patrón forzado.
- Debe ser inequívoco y no genérico.

### Reglas comunes
- `name` del frontmatter debe coincidir exactamente con el nombre de la carpeta (kebab-case).
- Prohibidos nombres genéricos: `helper`, `utils`, `tools`.
- **Nunca incluir versión en el nombre** (rompe el matching de trigger y duplica entradas en el catálogo). El versionado se gestiona internamente (ver Documento 5).

## Exclusividad de dominio

Un `[dominio]` solo puede tener una skill "dueña", **salvo excepción válida**: dos skills pueden compartir dominio si están segmentadas por fase/verbo distinto (ej. lectura vs. escritura de un mismo tipo de archivo). En ese caso, ambas `description` deben declarar explícitamente su fase para evitar ambigüedad de trigger (ver Documento 4).

## Escalado de `references/`

Si `references/` tiene más de un archivo, el archivo principal o el propio SKILL.md debe incluir un índice indicando cuándo leer cada uno. Evita que Claude cargue todo por defecto.

## Relación con el resto del framework

- Ancla el criterio "Delimitable" (Documento 1) a una regla mecánica y verificable.
- Base para la detección de solapamiento del registro central (Documento 4).
- El versionado queda delegado completamente a Documento 5.
