# Práctico: Skills clínicos en Claude con GitHub

Diplomado Online en Sistemas de Información en Salud
Módulo: Inteligencia Artificial Generativa y LLM
Docente: Dr. Fernando Eimbcke Bosch

## Objetivo

Aplicar los conceptos de la clase teórica (prompting, salida estructurada, few-shot, alucinaciones, guardrails y evaluación) construyendo en equipo un **skill de Claude** que resuelva una tarea clínica concreta, versionado en GitHub.

## Agenda (aprox. 2 horas)

| Bloque | Tiempo | Contenido |
|---|---|---|
| 1 | 20 min | Demo de Alemana IA y Alemana Agéntica |
| 2 | 15 min | [GitHub en 15 minutos](docs/GITHUB_101.md) |
| 3 | 10 min | [Anatomía de un skill](docs/ANATOMIA_SKILL.md) |
| 4 | 30 min | Trabajo en grupos, ver la [guía del práctico](GUIA_PRACTICO.md) |
| 5 | 30 min | Presentaciones (5 min + 1 min de preguntas por grupo) |
| Cierre | 5 min | Riesgos, gobernanza y camino a producción |

## Contenido del repo

```
GUIA_PRACTICO.md            Instrucciones, entregables y pauta de evaluación
PROYECTOS.md                8 ideas de proyecto para elegir
docs/
  GITHUB_101.md             Conceptos mínimos de GitHub
  ANATOMIA_SKILL.md         Cómo se construye un skill
skills-ejemplo/
  informe-para-paciente/    Skill de ejemplo: lenguaje simple para pacientes
  extraccion-mamografia/    Skill de ejemplo: texto libre a JSON estructurado
casos-sinteticos/           Casos clínicos ficticios para probar
plantilla-grupo/            Punto de partida para cada equipo
skills-zip/                 Skills de ejemplo listos para subir a Claude
```

## Reglas del práctico

1. **Solo datos sintéticos.** Nunca uses datos reales de pacientes, ni siquiera anonimizados "a mano".
2. Los skills son **apoyo a la decisión**, no reemplazan el juicio clínico.
3. Todo lo que construyan debe poder explicarse: qué hace, qué NO hace y cuándo falla.
