# Ejemplo 1 (caso sintético)

## Entrada

> MAMOGRAFÍA BILATERAL DIGITAL, 14/03/2026. Mamas heterogéneamente densas (ACR C). En mama izquierda, cuadrante superoexterno, nódulo de 9 mm de márgenes circunscritos, sin cambios respecto a estudio previo de 2024. Mama derecha sin hallazgos. No se observan microcalcificaciones sospechosas. Axilas sin adenopatías.
> CONCLUSIÓN: BI-RADS 2. Control anual.

## Salida esperada

```json
{
  "fecha_examen": "2026-03-14",
  "tipo_examen": "mamografia_bilateral",
  "densidad_mamaria": "c",
  "hallazgos": [
    {
      "tipo": "nodulo",
      "mama": "izquierda",
      "ubicacion": "cuadrante superoexterno",
      "tamano_mm": 9,
      "descripcion": "Márgenes circunscritos, estable respecto a 2024"
    }
  ],
  "birads_derecha": null,
  "birads_izquierda": null,
  "birads_global": "2",
  "recomendacion": "Control anual",
  "requiere_revision_humana": false,
  "motivo_revision": null
}
```
