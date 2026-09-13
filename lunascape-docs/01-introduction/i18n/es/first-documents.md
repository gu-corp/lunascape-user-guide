# Crear los primeros documentos

En un proyecto que todavía no tiene una carpeta de documentación, puede crear un primer conjunto de documentos desde la paleta de comandos.

1. Abra la carpeta del proyecto en VS Code y marque el área de trabajo como de confianza.
2. En la paleta de comandos (`⇧⌘P` / `Ctrl+Shift+P`), ejecute «Lunascape Docs: Crear documentación a partir de una plantilla».
   Si el área de trabajo tiene varias carpetas, elija aquella en la que se crearán los documentos.
3. Elija la estructura que desea crear.
   - [Documento de una página]: solo un `README.md`. Es la estructura mínima, adecuada para una especificación breve, notas o un documento explicativo independiente.
   - [Conjunto de documentación]: crea una página principal y las páginas de entrada de `specification/` (especificaciones), `manual/` (manual) y `help/` (ayuda).
4. Escriba el título de la documentación. Se usa en el README y en los encabezados de cada documento.
5. Escriba la carpeta de documentación que se creará, con una ruta relativa al área de trabajo. El valor predeterminado es `docs`.
6. Revise la lista de archivos que se van a crear y pulse [Crear].
   Cuando termine la creación, el nuevo `README.md` se abre en el visor.

> **Nota**
>
> - Los archivos existentes no se sobrescriben. Si alguno de los archivos que se van a crear ya existe, no se crea nada y la operación se detiene.
> - No es posible crear documentos en un área de trabajo que no sea de confianza.

> **Sugerencia**
>
> - Si ya tiene una carpeta de documentación, omita este procedimiento y continúe en [Operaciones básicas](../02-reading/README.md).
> - A medida que crezca la documentación, puede añadir los documentos de uno en uno eligiendo una plantilla en la pestaña [Crear] de Herramientas de documentos.

## Temas relacionados

- [Crear un documento a partir de una plantilla](../04-document-tools/templates.md)
- [Raíces de documentación y convenciones de archivos](../04-document-tools/structure.md)
