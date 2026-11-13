# Template_Manual_Practicas

Plantilla LaTeX para manuales de prácticas del laboratorio (estilo Libro de Marca UCUENCA).
Basada en `Manual_Prácticas_Lego_EV3`, pero sin su contenido.

## Cómo usarla

1. Copiar la carpeta completa y renombrarla (p. ej. `Manual_Prácticas_MiEquipo`).
2. En `main.tex`, editar el bloque **DATOS DEL DOCUMENTO** (título, tema, autor, encabezado, metadatos del PDF).
3. Reemplazar `1-introduccion.tex` y copiar `2-practica1.tex` para cada práctica nueva; agregar el `\input{...}` en `main.tex`.
4. Poner las imágenes en `images/` (ya está en `\graphicspath`, se llaman solo por el nombre) y las referencias en `references.bib`.

## Compilar

```
latexmk -pdf -outdir=build main.tex
```

Necesita `pdflatex` + `biber` (MiKTeX/TeX Live) y los paquetes FiraSans, tcolorbox, fontawesome5, etc.

## Archivos

| Archivo | Para qué |
|---|---|
| `main.tex` | Datos del documento y orden de los capítulos |
| `Template/Template.tex` | Preámbulo: fuentes, colores, cajas, títulos, encabezado (no se edita por documento) |
| `Template/Portada.tex` | Portada azul con franjas rojas; usa los datos de `main.tex` |
| `1-introduccion.tex` | Capítulo de ejemplo con figuras, citas y enlaces |
| `2-practica1.tex` | Práctica de ejemplo con todos los elementos |
| `references.bib` | Bibliografía (estilo IEEE) |

## Elementos disponibles (ver `2-practica1.tex`)

- Cajas: `objetivebox`, `materialbox`, `infobox[Título]`, `warningbox[Título]`, `entregabox`
- Código: `ArduinoSketchBox{Título}` y `lstlisting`
- Macros: `\ExternalLink`, `\doclink{URL}{texto}`, `\keys{...}`, `\pinref{...}`, `\comp{...}`
- Tablas con `booktabs`, figuras con `[H]`, ecuaciones, TikZ
