# Guía del práctico

## Antes de empezar (5 min)

- Un integrante por grupo debe tener cuenta de **GitHub** y de **Claude** con skills habilitados.
- Ese integrante hace una copia de este repo en su cuenta (botón **Fork** o **Use this template**).
- Copien la carpeta `plantilla-grupo/` y renómbrenla con el nombre de su proyecto, por ejemplo `grupo-3-triage-mensajes/`.

## Trabajo en grupo (30 min)

| Minuto | Tarea |
|---|---|
| 0 a 5 | Elegir un proyecto de [PROYECTOS.md](PROYECTOS.md) o proponer uno propio. Completar el README del grupo: problema, usuario, entrada, salida |
| 5 a 15 | Escribir el `SKILL.md`: descripción, instrucciones, formato de salida y límites |
| 15 a 22 | Escribir 3 casos de prueba en `casos-prueba.md` (uno normal, uno difícil, uno que intente romper el skill) |
| 22 a 28 | Subir el skill a Claude y probarlo con los 3 casos. Anotar resultados |
| 28 a 30 | Preparar la presentación |

### Cómo probar el skill en Claude

1. Comprimir la carpeta del skill (la que contiene `SKILL.md`) en un `.zip`.
2. En Claude: **Settings > Capabilities > Skills > Upload skill**.
3. Abrir un chat nuevo y pegar un caso de prueba. Verificar que el skill se active.

Alternativa si no pueden subir skills: crear un **Project** en Claude, conectar el repo de GitHub como conocimiento del proyecto y pedirle a Claude que siga las instrucciones de su `SKILL.md`.

## Entregables

1. Carpeta del grupo en GitHub con:
   - `README.md` completo
   - `SKILL.md` funcional
   - `casos-prueba.md` con los 3 casos y lo que obtuvieron
2. Al menos 1 commit por integrante (pueden editar directamente desde la web de GitHub).

## Presentación (5 min por grupo)

1. **Problema y usuario** (1 min): qué tarea clínica, para quién y por qué vale la pena.
2. **Demo en vivo** (2 min): un caso que funciona.
3. **Un caso que falló** (1 min): qué pasó y por qué creen que ocurrió.
4. **Riesgos y gobernanza** (1 min): qué haría falta antes de usarlo con pacientes reales.

## Pauta de evaluación

| Criterio | Pregunta guía |
|---|---|
| Pertinencia clínica | ¿Resuelve un problema real y acotado? |
| Calidad del skill | ¿La descripción, las instrucciones y el formato de salida son claros? |
| Uso de conceptos LLM | ¿Aplican few-shot, salida estructurada, guardrails u otros conceptos de la clase? |
| Evaluación | ¿Probaron casos difíciles y reconocen las fallas? |
| Seguridad | ¿Definen qué NO hace el skill y cuándo escalar a un humano? |
