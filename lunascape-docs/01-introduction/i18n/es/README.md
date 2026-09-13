# Qué es Lunascape Docs

Lunascape Docs es una herramienta para tratar los documentos Markdown que están en un repositorio Git como un «sitio de especificaciones», tal como están. No hace falta compilación previa, ni servidor de documentación, ni una base de datos específica.

## Qué se puede hacer

| Objetivo | Funciones principales |
|---|---|
| Leer | INDEX (índice), enlaces del texto, ruta de navegación, atrás y adelante, índice de la página, búsqueda con filtro |
| Ver | Tablas, bloques de código, ajuste automático de las imágenes, fórmulas KaTeX, diagramas de Mermaid, Vega-Lite, Markmap, WaveDrom y Svgbob, tablas de control de documentos plegadas |
| Escribir | Cambio entre la edición visual y la edición del código Markdown; crear, duplicar, renombrar y reordenar desde el INDEX |
| Comprobar | Comprobación de documentos con docs-lint, verificación de los documentos, capítulos y términos obligatorios según el Standard Pack, creación a partir de plantillas |
| Traducir | Generación de propuestas de traducción por página o en lote. Se revisan antes de guardarlas <!-- ai-only --> |
| Usar desde la IA | Una herramienta de especificaciones de solo lectura que los agentes de VS Code pueden consultar <!-- ai-only --> |

## Entornos disponibles

| Entorno | Uso |
|---|---|
| Extensión de VS Code | Lectura, edición, comprobación y traducción del repositorio local. Es el centro de esta ayuda |
| Versión para navegador web | Lectura de documentos en GitHub (públicos y privados), borradores en el dispositivo, lectura de una carpeta local |
| Extensión de Chromium | Abre la versión para navegador web en una pestaña del navegador |
| Navegador Lunascape | Está previsto que incorpore el mismo modelo de documentos |

## Ideas básicas

- **El Markdown es el original.** Los documentos siguen siendo los archivos Markdown gestionados con Git. Lunascape Docs no los convierte a otro formato ni conserva una copia convertida.
- **Guardar es cosa del usuario.** El contenido editado se escribe en el archivo solo cuando se pulsa [Guardar]. La preparación (staging) y la confirmación (commit) de Git nunca se hacen de forma automática.
- **Los documentos se procesan en el dispositivo.** Para leer o editar un documento no se envía nada al exterior. Solo la traducción envía contenido, y antes se muestran el destino y el contenido; el envío se realiza tras la aprobación.
- **Las traducciones se colocan en `i18n/<idioma>/`.** Los documentos en el idioma predeterminado se quedan donde están; las traducciones se colocan con la misma ruta relativa en `i18n/en/`, etc.
- **La IA solo propone.** Las propuestas de traducción se guardan después de revisar las diferencias. Nunca se reescribe un documento en silencio. <!-- ai-only -->

## Temas relacionados

- [Nombre y función de cada parte de la pantalla](screen.md)
- [Instalar la extensión](install.md)
- [Operaciones básicas](../02-reading/README.md)
