# Anatomía de un skill

Un **skill** es una carpeta con instrucciones que Claude carga cuando la tarea lo requiere. Es una forma de empaquetar un buen prompt, con sus referencias y ejemplos, para reutilizarlo de forma consistente.

## Estructura

```
mi-skill/
  SKILL.md          Obligatorio: metadatos e instrucciones
  references/       Opcional: guías, tablas, criterios, glosarios
  examples/         Opcional: entradas y salidas de ejemplo (few-shot)
```

## El archivo SKILL.md

```markdown
---
name: nombre-del-skill
description: Qué hace y CUÁNDO usarlo. Claude lee esto para decidir si activar el skill.
---

# Nombre del skill

## Objetivo
## Entrada esperada
## Pasos
## Formato de salida
## Límites (qué NO hace)
## Ejemplos
```

## Claves para un buen skill

1. **La `description` decide la activación.** Incluyan palabras que el usuario usaría ("traduce este informe", "extrae los datos de esta mamografía").
2. **Formato de salida explícito.** Si quieren JSON, muestren el esquema exacto.
3. **Ejemplos concretos.** Uno o dos pares entrada/salida mejoran mucho la consistencia (few-shot).
4. **Límites explícitos.** Qué hacer cuando falta información, cuándo escalar a un humano, qué nunca debe hacer.
5. **Referencias en archivos aparte.** Tablas largas o criterios van en `references/` y se mencionan desde el `SKILL.md`.

## Conceptos de la clase teórica que aparecen

| Concepto | Dónde se aplica en el skill |
|---|---|
| Ingeniería de prompts | Instrucciones y pasos |
| Few-shot | Carpeta `examples/` |
| Salida estructurada | Sección formato de salida |
| Grounding / RAG simple | Carpeta `references/` |
| Alucinaciones | Regla "si no está en la fuente, no lo inventes" |
| Guardrails | Sección límites |
| Evaluación | Casos de prueba del grupo |
