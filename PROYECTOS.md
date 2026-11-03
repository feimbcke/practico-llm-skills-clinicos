# Ideas de proyecto

Elijan uno o propongan el suyo. Cada idea indica qué concepto de LLM practican.

## 1. Informe para el paciente
Traducir un informe de imagen o laboratorio a lenguaje simple.
- **Entrada:** informe técnico.
- **Salida:** explicación en lenguaje claro, preguntas sugeridas para el médico tratante.
- **Conceptos:** control de tono y nivel de lectura, no inventar hallazgos, no dar diagnósticos nuevos.
- **Ejemplo resuelto:** `skills-ejemplo/informe-para-paciente/`

## 2. Extracción estructurada de informes
Convertir un informe en texto libre a JSON.
- **Entrada:** informe de mamografía, colonoscopía o ecocardiograma.
- **Salida:** JSON con campos definidos (por ejemplo BI-RADS, calidad de preparación, FEVI).
- **Conceptos:** salida estructurada, few-shot, manejo de datos ausentes (`null` en vez de inventar).
- **Ejemplo resuelto:** `skills-ejemplo/extraccion-mamografia/`

## 3. Entrega de turno I-PASS o SBAR
Generar una entrega de turno desde notas de evolución.
- **Entrada:** notas de evolución de enfermería y médicas.
- **Salida:** entrega en formato I-PASS.
- **Conceptos:** resumen, plantillas, riesgo de omisiones críticas.

## 4. Sugerencia de códigos CIE-10
Proponer códigos a partir de un diagnóstico en texto libre.
- **Entrada:** diagnóstico de egreso.
- **Salida:** códigos candidatos, justificación y nivel de certeza.
- **Conceptos:** alucinación (códigos inexistentes), calibración, uso de una tabla de referencia en `references/`.

## 5. Borrador de epicrisis
Redactar una epicrisis a partir del resumen de una hospitalización.
- **Entrada:** datos de ingreso, evolución, exámenes, indicaciones.
- **Salida:** epicrisis con estructura institucional.
- **Conceptos:** plantillas, trazabilidad a la fuente, marcar lo que falta en vez de completarlo.

## 6. Triage de mensajes de pacientes
Clasificar mensajes del portal de pacientes por urgencia.
- **Entrada:** mensaje del paciente.
- **Salida:** categoría (urgente, prioritario, rutina, administrativo), motivo y acción sugerida.
- **Conceptos:** guardrails, criterios explícitos de escalamiento, sesgo hacia la seguridad.

## 7. Auditoría de calidad del registro clínico
Revisar si una nota cumple criterios mínimos.
- **Entrada:** nota clínica.
- **Salida:** checklist (alergias, diagnóstico, plan, indicaciones, firma) con cumple o no cumple.
- **Conceptos:** criterios en `references/`, salida tabular, consistencia entre ejecuciones.

## 8. Conciliación de medicamentos
Comparar la lista de medicamentos al ingreso y al alta.
- **Entrada:** dos listas de medicamentos.
- **Salida:** medicamentos suspendidos, nuevos, con cambio de dosis y posibles duplicidades.
- **Conceptos:** límites explícitos (no recomendar cambios), razonamiento paso a paso, revisión humana obligatoria.
