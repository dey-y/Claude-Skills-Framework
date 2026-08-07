# Documento 1 — Criterios de scope

## Objetivo
Definir cuándo una tarea justifica crear una Skill y cuándo no, para evitar sobrecarga del ecosistema (skills duplicadas, demasiado granulares o innecesarias).

## Criterios de entrada

Una skill se justifica solo si cumple **las 3** condiciones:

1. **Repetible**: la tarea se repetirá con variaciones, no es un caso único.
2. **Procedimental**: existe una forma correcta/mejor de hacerlo que Claude no infiere de forma fiable por sí solo (herramienta específica, formato exacto, secuencia de pasos, convención de la organización).
3. **Delimitable**: se puede describir en una frase qué activa la skill sin ambigüedad frente a otras skills existentes (verificable contra el registro central — ver Documento 4).

## Señales de que NO debe ser skill

- Tarea que Claude ya resuelve bien sin instrucciones adicionales (conocimiento general).
- Caso de uso único, no repetible.
- Es en realidad una variante de una skill existente → va como `references/variante.md` dentro de la skill existente, no como skill nueva.

## Test de responsabilidad única

Si al describir la skill necesitas usar "y" para conectar dos acciones no relacionadas, son dos skills, no una.

## Relación con el resto del framework

- El criterio "Delimitable" se verifica mecánicamente contra el registro central (Documento 4).
- Este documento es el filtro de entrada; no define estructura (Documento 2) ni redacción (Documento 3).
