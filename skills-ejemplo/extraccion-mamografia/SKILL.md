---
name: extraccion-mamografia
description: Extrae datos estructurados en JSON desde informes de mamografía en texto libre (categoría BI-RADS, densidad mamaria, hallazgos, lateralidad, recomendación). Usar cuando el usuario pida "extrae los datos de esta mamografía", "estructura este informe", "pasa a JSON" o similar.
---

# Extracción estructurada de mamografía

## Objetivo
Convertir un informe de mamografía en texto libre a un JSON consistente, útil para registros, indicadores de calidad o seguimiento.

## Entrada esperada
Uno o más informes de mamografía. Si son varios, devolver una lista de objetos JSON.

## Pasos
1. Identificar fecha, lateralidad del examen y técnica (si está).
2. Extraer la densidad mamaria (a, b, c, d) según `references/bi-rads.md`.
3. Listar cada hallazgo con tipo, mama, ubicación y tamaño si se informa.
4. Extraer la categoría BI-RADS final. Si hay una por mama, registrar ambas.
5. Extraer la recomendación.
6. Revisar: todo valor debe estar textualmente respaldado por el informe.

## Formato de salida
Responder **solo** con JSON válido, sin texto adicional:

```json
{
  "fecha_examen": "AAAA-MM-DD o null",
  "tipo_examen": "mamografia_bilateral | mamografia_unilateral | null",
  "densidad_mamaria": "a | b | c | d | null",
  "hallazgos": [
    {
      "tipo": "nodulo | microcalcificaciones | distorsion | asimetria | otro",
      "mama": "derecha | izquierda",
      "ubicacion": "texto o null",
      "tamano_mm": "número o null",
      "descripcion": "texto breve"
    }
  ],
  "birads_derecha": "0 | 1 | 2 | 3 | 4A | 4B | 4C | 5 | 6 | null",
  "birads_izquierda": "0 | 1 | 2 | 3 | 4A | 4B | 4C | 5 | 6 | null",
  "birads_global": "valor más alto o null",
  "recomendacion": "texto o null",
  "requiere_revision_humana": true,
  "motivo_revision": "texto o null"
}
```

## Límites
- Si un dato no está en el informe, usar `null`. **Nunca inferir** una categoría BI-RADS que no esté escrita.
- `requiere_revision_humana` es `true` si: BI-RADS 0, 4, 5 o 6; el informe es ambiguo; o hay contradicciones (por ejemplo, hallazgo sospechoso con BI-RADS 2).
- No emitir opinión diagnóstica.

## Ejemplo
Ver `examples/ejemplo-1.md`.
