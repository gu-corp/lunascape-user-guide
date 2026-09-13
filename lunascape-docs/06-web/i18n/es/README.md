# Qué permite hacer la versión Web

La versión Web de Lunascape Docs está publicada en <https://docs.lunascape.org/>. Sin instalar nada, permite leer los documentos alojados en GitHub como si fueran un sitio web.

## Funciones

| Función | Descripción |
|---|---|
| Consulta de repositorios públicos | Abre los documentos de un repositorio público de GitHub sin iniciar sesión |
| Consulta de repositorios privados | Al iniciar sesión con GitHub, abre los repositorios sobre los que tiene permiso de lectura |
| Consulta de carpetas locales | Con [Abrir documentos] y luego [Abrir documentos de una carpeta local], abre una carpeta de su dispositivo (solo en navegadores compatibles) |
| Funciones de lectura | INDEX, enlaces, historial, filtrado, índice de la página, cambio de idioma y cambio de tema. Igual que en la versión de VS Code |
| Diagramas y fórmulas | Mermaid, Vega-Lite, Markmap, WaveDrom, Svgbob, Penrose y fórmulas KaTeX |
| Borradores | Edita los documentos y conserva los cambios como borradores en su dispositivo. No escribe nada en el repositorio |
| Enlaces directos a una página | La URL puede indicar el repositorio y la página, de modo que se abre directamente una página concreta |

## Diferencias con la versión de VS Code

- La comprobación de documentos, la creación a partir de plantillas, la generación de propuestas de traducción y la organización desde el INDEX no están disponibles en la versión Web.
- Los diagramas TikZ no se representan.
- Las ediciones no se escriben en el repositorio, sino que quedan como borradores en su dispositivo. La «solicitud de publicación», que envía los borradores como Pull Request, está implementada, pero no está habilitada en el visor público. Para reflejar los cambios en el repositorio, edite con la versión de VS Code o en un clon local.

## Temas relacionados

- [Abrir un repositorio de GitHub](open-repository.md)
- [Consultar un repositorio privado](private-repository.md)
- [Guardar borradores](drafts.md)
