# Documento 3 — Guía de autoría de SKILL.md

## Objetivo
El frontmatter (`description`) decide si la skill se activa. El cuerpo decide si Claude ejecuta bien la tarea una vez activada. Son responsabilidades distintas pero inseparables en redacción.

## Frontmatter

- `description`: incluye QUÉ hace la skill y CUÁNDO usarla, en la misma frase.
- Sesgo intencional hacia "pushy": Claude tiende a infratriggerar skills por defecto. La description debe mencionar sinónimos y contextos indirectos, no solo el caso obvio y literal.
- Todo el criterio de "cuándo usar" vive en `description`. Nunca duplicarlo o esconderlo en el cuerpo.

## Cuerpo (SKILL.md)

- Límite recomendado: menos de 500 líneas. Si se acerca al límite, extraer contenido a `references/` con un puntero explícito de cuándo leerlo.
- Redacción en forma imperativa, no narrativa.
- Explicar el *porqué* detrás de cada instrucción, no solo el *qué*. Evitar MUSTs rígidos en mayúsculas salvo casos realmente no negociables (ej. seguridad).
- Definir formatos de salida con plantilla exacta cuando el output deba ser consistente.
- Incluir 1-2 ejemplos input→output cuando el formato no sea obvio solo con la descripción.

## Relación con el resto del framework

- `description` no debe repetir el naming (Documento 2), debe explicarlo en lenguaje natural.
- El sesgo "pushy" en `description` no contradice el criterio "Delimitable" (Documento 1): pushy es sobre cobertura de contextos, no sobre invadir el dominio de otra skill.
- Si dos skills necesitan overlap parcial de contexto, la resolución no se define aquí — se traslada al Documento 4 (gestión del ecosistema).
