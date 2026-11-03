# GitHub en 15 minutos

## ¿Qué es?

GitHub es un lugar en la nube para guardar carpetas de archivos con **historial completo de cambios**. Piensen en el control de cambios de un protocolo clínico: quién cambió qué, cuándo y por qué, pero aplicado a código, prompts y documentación.

## Conceptos mínimos

| Concepto | Qué es | Analogía clínica |
|---|---|---|
| **Repositorio (repo)** | Una carpeta de proyecto con su historial | La carpeta de un protocolo |
| **Commit** | Un cambio guardado con un mensaje que lo explica | Una versión firmada del protocolo |
| **README.md** | La portada del repo, se muestra automáticamente | La primera página: objetivo y alcance |
| **Fork** | Tu propia copia de un repo ajeno | Adaptar un protocolo de otra institución |
| **Branch (rama)** | Una línea de trabajo paralela | Un borrador en revisión antes de aprobarse |
| **Pull request** | Solicitud para incorporar cambios de una rama | Enviar el borrador al comité para aprobación |

## ¿Por qué importa en IA clínica?

- **Trazabilidad:** cada cambio a un prompt o skill queda registrado. Es la base de la gobernanza.
- **Colaboración:** varias personas trabajan sobre lo mismo sin pisarse.
- **Reversibilidad:** si una versión empeora el desempeño, se vuelve a la anterior.
- **Contexto para Claude:** un repo se puede conectar a un Project de Claude para que lo use como conocimiento.

## Lo que haremos hoy (todo desde la web, sin terminal)

1. Hacer **Fork** o **Use this template** de este repo.
2. Editar archivos con el ícono del lápiz y guardar con **Commit changes**.
3. Crear archivos nuevos con **Add file > Create new file** (escribir `carpeta/archivo.md` crea la carpeta).
4. Conectar el repo a Claude: en un Project, **Add content > GitHub** y seleccionar el repo.

## Formato Markdown básico

```markdown
# Título
## Subtítulo
- viñeta
**negrita**
| tabla | simple |
|---|---|
| a | b |
```
