# Qué es Lunascape Docs

Lunascape Docs es una herramienta para usar los documentos Markdown guardados en un repositorio Git, tal como están, como un «sitio de especificaciones». No necesita compilación previa, servidor de documentación ni base de datos propia.

## Qué puede hacer

| Objetivo | Funciones principales |
|---|---|
| Leer | INDEX (índice), enlaces en el texto, ruta de navegación, Atrás/Adelante, índice de la página, búsqueda con filtro |
| Ver | Tablas, bloques de código, ajuste automático de imágenes, fórmulas KaTeX, diagramas de Mermaid, Vega-Lite, Markmap, WaveDrom y Svgbob, tablas de control del documento plegadas |
| Escribir | Cambio entre edición visual y edición del código fuente Markdown; creación, duplicación, cambio de nombre y reordenación desde el INDEX |
| Comprobar | Comprobación de documentos con docs-lint, verificación de documentos, capítulos y términos obligatorios según el Standard Pack, creación a partir de plantillas |
| Traducir | Generación de propuestas de traducción página a página o en bloque. Se revisan antes de guardarlas <!-- ai-only --> |
| Usar desde la IA | Herramienta de especificaciones de solo lectura que pueden consultar los agentes de VS Code <!-- ai-only --> |

## Entornos disponibles

| Entorno | Uso |
|---|---|
| Extensión de VS Code | Ver, editar, comprobar y traducir el repositorio local. Es el tema principal de esta ayuda |
| Versión web | Ver documentos de GitHub (públicos y privados), guardar borradores en el dispositivo, ver carpetas locales |
| Extensión para Chromium | Abre la versión web en una pestaña del navegador |

## Conceptos básicos

- **Markdown es la versión canónica.** Los documentos siguen siendo los archivos Markdown gestionados con Git. Lunascape Docs no los convierte ni los guarda en otro formato.
- **El usuario decide cuándo guardar.** Los cambios se escriben en el archivo solo al pulsar [Guardar]. El staging y el commit de Git nunca se hacen automáticamente.
- **Los documentos se procesan en el dispositivo.** Para ver o editar un documento no se envía nada al exterior. Solo al traducir se envía el documento, y antes se muestran el destino y el contenido; el envío se hace tras su aprobación.
- **Las traducciones se guardan en `i18n/<idioma>/`.** Los documentos del idioma predeterminado se quedan donde están; las traducciones se colocan con la misma ruta relativa en `i18n/en/`, etc.
- **La IA solo propone.** Las propuestas de traducción se guardan después de revisar las diferencias. Los documentos nunca se reescriben sin avisar. <!-- ai-only -->

## Temas relacionados

- [Nombres y funciones de las partes de la pantalla](screen.md)
- [Instalar la extensión](install.md)
- [Operaciones básicas](../02-reading/README.md)
