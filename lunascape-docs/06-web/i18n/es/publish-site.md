# Publicar tus documentos en la Web

Puedes publicar los documentos de tu propio repositorio como un sitio web en GitHub Pages o en cualquier hosting estático. Hay dos maneras de hacerlo. Estos pasos están dirigidos a desarrolladores que puedan clonar el repositorio de Lunascape Docs y usar `npm`.

## Opción 1: colocar los dos archivos del visor

Consiste en desplegar únicamente el visor (`index.html` y `lsdoc.js`) y dejar que cargue los documentos desde GitHub. Los documentos en sí no forman parte del sitio, por lo que este método es seguro incluso con repositorios privados (los lectores inician sesión con GitHub).

1. Ejecuta el siguiente comando en el repositorio de Lunascape Docs.

   ```sh
   npm run build:viewer
   ```

   Se generan `index.html` y `lsdoc.js` en `dist/viewer/`.
2. Coloca los dos archivos en la carpeta `docs/` del repositorio que quieras publicar.
3. Activa GitHub Pages.

La raíz de documentación que se muestra se determina en este orden.

1. La configuración `source` dentro de `index.html`
2. El valor `repository` indicado en el archivo `lunascape-docs.json` de la misma carpeta
3. La deducción a partir de la URL `*.github.io` y la estructura de ramas

## Opción 2: exportar un sitio estático que incluya los documentos

Consiste en exportar el visor junto con los archivos de los documentos y alojar el resultado tal cual.

```sh
npm run export:web -- --root ./docs --out ./dist-site
```

Se generan el conjunto del visor, los documentos que están bajo `docs/`, el archivo de índice `lunascape-docs-manifest.json` y `.nojekyll`. Puedes publicar el resultado colocándolo en S3 o en GitHub Pages. Para ver un ejemplo de publicación automática con GitHub Actions, consulta `examples/workflows/publish-docs-pages.yml` en el repositorio.

> **Nota**
>
> - **No exportes los documentos de un repositorio privado ni los coloques en GitHub Pages.** Fuera de Enterprise Cloud, cualquier persona puede consultar GitHub Pages. Si necesitas una publicación restringida, usa la opción 1 y haz que los lectores inicien sesión con GitHub.
> - Abrir `index.html` directamente mediante `file://` no funciona, porque el navegador impide cargar archivos contiguos y ejecutar módulos ES. Para comprobarlo en tu equipo, usa la versión de VS Code o un servidor HTTP.
> - Las bibliotecas de representación de TikZ, Vega-Lite, Markmap, WaveDrom, Svgbob y Penrose se cargan en el momento de mostrarlas. En un sitio exportado, coloca también la carpeta `vendor/`.

## Temas relacionados

- [Qué puedes hacer con la versión Web](README.md)
- [Consultar un repositorio privado](private-repository.md)
