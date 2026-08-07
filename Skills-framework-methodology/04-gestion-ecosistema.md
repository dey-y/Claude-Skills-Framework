# Documento 4 — Gestión del ecosistema

## Objetivo
Con múltiples skills, el riesgo no es la calidad individual sino la interacción: dos skills que compiten por el mismo trigger, o triggers ambiguos frente a tareas límite.

## Registro central

Tabla viva (ver `registry.md`) con columnas: `nombre — dominio — descripción resumida — estado`.

Se consulta **antes** de crear cualquier skill nueva, para verificar el criterio "Delimitable" (Documento 1) de forma mecánica, no solo declarativa.

## Regla de no-solapamiento de dominio

Un `[dominio]` (Documento 2) solo puede tener una skill "dueña".

**Excepción válida — segmentación por fase:**
Dos skills pueden compartir dominio si están segmentadas por verbo/fase distinta (ej. una skill de *lectura* de un tipo de archivo y otra distinta de *creación/edición* del mismo tipo). No es solapamiento real, es división de responsabilidad por operación. En este caso, ambas `description` deben declarar explícitamente su fase para evitar ambigüedad de trigger.

Si una tarea cruza dos dominios distintos (ej. PDF + Excel) sin ser una segmentación de fase, no se crea una skill híbrida. Se elige el dominio principal según el output final, y la skill puede referenciar la otra dentro de su cuerpo si es necesario.

## Resolución de ambigüedad de trigger

Si dos `description` podrían activarse para el mismo prompt:

1. Gana la skill cuyo dominio coincide con el tipo de archivo o herramienta del **output final** invocado.
2. Si ninguna de las dos es claramente el output final (ambas son intermedias), no se fuerza una ganadora — se aplica la excepción de segmentación por fase, ajustando ambas `description` para declarar su fase explícitamente.

## Auditoría periódica

Revisar el registro central cuando el catálogo crece, buscando descriptions que se solapan en la práctica (no solo en teoría), aunque en el diseño original no lo parecieran.

## Relación con el resto del framework

- Opera directamente sobre el vocabulario de Documento 1 (Delimitable) y Documento 2 (dominio único) — no introduce conceptos nuevos, los hace verificables.
- El registro central es el único punto que requiere mantenimiento activo continuo.
