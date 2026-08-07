# Documento 5 — Ciclo de vida

## Objetivo
Cerrar el circuito completo: cómo nace, se valida, se publica y se retira una skill. Incluye el checklist de calidad como fase de validación (no como documento separado) y el versionado (referenciado desde Documento 2).

## Fases

### 1. Borrador
Aplica los criterios de scope (Documento 1) y consulta el registro central (Documento 4) antes de escribir nada.

### 2. Redacción
Sigue la guía de autoría (Documento 3): frontmatter + cuerpo.

### 3. Validación — checklist (gate obligatorio antes de publicar)

- [ ] ¿Pasa las 3 condiciones de scope (Documento 1)?
- [ ] ¿`description` cubre variantes de contexto, no solo el caso literal?
- [ ] ¿SKILL.md tiene menos de 500 líneas o está correctamente derivado a `references/`?
- [ ] ¿El naming cumple Documento 2 y el dominio está libre (o la excepción de fase está declarada) en el registro (Documento 4)?
- [ ] ¿Se probó con 2-3 prompts realistas y el resultado es el esperado?

### 4. Publicación
Se añade la skill al registro central (Documento 4).

### 5. Versionado
- Cambios internos (mejoras de redacción, fixes) **no** cambian el nombre ni la carpeta.
- Cambios de comportamiento/output relevantes se documentan en un changelog dentro del propio SKILL.md (sección final). Si crece demasiado, se mueve a `references/changelog.md`.

### 6. Deprecación
- Se marca en el registro como `deprecated`.
- La carpeta se conserva con una nota indicando la skill sustituta si aplica.
- No se borra en frío — mantiene trazabilidad histórica y evita romper referencias externas.

## Relación con el resto del framework

Cada fase cita explícitamente los documentos anteriores (1, 2, 3, 4) sin repetir su contenido — solo los referencia y los convierte en pasos ejecutables.
