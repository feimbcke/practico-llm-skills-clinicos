---
name: informe-para-paciente
description: Traduce informes médicos técnicos (imagenología, laboratorio, anatomía patológica) a lenguaje simple para pacientes, en español. Usar cuando el usuario pida "explícale este informe al paciente", "traduce a lenguaje simple", "versión para el paciente" o similar.
---

# Informe para el paciente

## Objetivo
Ayudar a que un paciente entienda su informe, sin agregar información que no esté en el documento y sin reemplazar la conversación con su médico tratante.

## Entrada esperada
Texto de un informe médico. Opcionalmente, la edad del paciente o su nivel educacional.

## Pasos
1. Leer el informe completo e identificar: tipo de examen, hallazgos, conclusión o impresión diagnóstica.
2. Traducir cada término técnico a lenguaje cotidiano. Usar el glosario de `references/glosario.md` cuando aplique.
3. Redactar a un nivel de lectura de enseñanza básica (frases cortas, sin siglas sin explicar).
4. Verificar que **cada afirmación** de la explicación tenga respaldo en el informe original.
5. Proponer 2 o 3 preguntas que el paciente podría hacerle a su médico.

## Formato de salida

```
**¿Qué examen se hizo?**
(1 o 2 frases)

**¿Qué encontraron?**
(viñetas cortas, una por hallazgo)

**¿Qué significa?**
(1 párrafo, solo lo que dice la conclusión del informe)

**Preguntas para su médico**
1. ...
2. ...

_Esta explicación es una ayuda para entender su informe. Converse los resultados con su médico tratante._
```

## Límites
- **No** agregar diagnósticos, pronósticos ni tratamientos que no estén en el informe.
- **No** minimizar ni dramatizar los hallazgos. Si el informe menciona sospecha de malignidad, decirlo con claridad y con calma, e indicar que debe conversarlo pronto con su médico.
- Si el informe es ilegible, incompleto o no es un informe médico, decirlo y no inventar.
- Si aparecen hallazgos críticos (por ejemplo, "hallazgo crítico comunicado"), indicar que debe contactar a su médico a la brevedad.

## Ejemplo
Ver `examples/ejemplo-1.md`.
