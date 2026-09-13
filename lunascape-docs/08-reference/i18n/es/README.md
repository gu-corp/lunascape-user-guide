# Especificaciones principales

## Requisitos del sistema

| Entorno | Requisitos |
|---|---|
| Extensión de VS Code | VS Code 1.90 o posterior. Las funciones que escriben archivos requieren un área de trabajo de confianza |
| Visor web | Versiones recientes de Chrome, Edge, Safari o Firefox. Para consultar una carpeta local se necesita un navegador compatible con la selección de carpetas (File System Access API) |
| Extensión de Chromium | Manifest V3. No solicita permisos de host |

## Documentos admitidos

| Elemento | Detalles |
|---|---|
| Archivos | `.md`, `.markdown`, `.mdx` |
| Markdown | GitHub Flavored Markdown (tablas, listas de tareas, bloques de código, texto tachado), imágenes locales, front matter en YAML |
| MDX | Solo se muestran los componentes permitidos. No se ejecuta ningún script arbitrario |
| HTML | Se depura con DOMPurify 3.4.14 antes de mostrarlo |

## Diagramas y fórmulas

| Tipo | Nombre del lenguaje | Notas |
|---|---|---|
| Fórmulas | `$...$`, `$$...$$`, `\(...\)`, `\[...\]` | KaTeX. `trust: false`, `maxSize: 50`, `maxExpand: 1000` |
| Mermaid | `mermaid` | |
| Vega-Lite | `vega-lite` | Solo datos incrustados. No se admiten URL externas ni marcas de imagen |
| Markmap | `markmap` | |
| WaveDrom | `wavedrom` | Solo JSON estricto |
| Svgbob | `svgbob` | |
| TikZ | `tikz` | En la versión distribuida, el código fuente se muestra plegado. Límites: 64 KiB de entrada, 15 segundos y 2 MiB de SVG |
| Penrose (experimental) | `penrose` | Solo el ajuste preestablecido `set-theory` |

## Límites

| Elemento | Valor |
|---|---|
| Resultado de la expansión de una plantilla | 4 MiB |
| Contexto de referencia de la traducción | 49.152 caracteres de forma predeterminada, 1.048.576 como máximo |
| Documentos por ejecución de traducción por lotes | 1.000 |
| Ancho personalizado de las imágenes | 16–4096 px |

## Archivos

| Archivo | Función | En Git |
|---|---|---|
| `lunascape-docs.json` | Configuración de la raíz de documentación | Sí |
| `docs-lint.config.json` | Configuración de las reglas de comprobación | Sí |
| `.lunascape-docs/translation-freshness.json` | Registro de la vigencia de las traducciones (solo rutas, idiomas, hashes y fechas) | Sí |
| Configuración de VS Code y estado del área de trabajo | Configuración de visualización personal, proveedor seleccionado y estado de apertura de INDEX | No |

## Standard Pack incluido

`builtin:gu-corp-software` — perfiles: `base`, `web-application`, `api-service`, `regulated-financial-product`, `smart-contract`

## Temas relacionados

- [Lista de ajustes de VS Code](settings.md)
- [Seguridad y límites de escritura](security.md)
