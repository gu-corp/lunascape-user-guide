# Crear un documento a partir de una plantilla

En la pestaña [Crear] de Herramientas de documentos puede elegir una plantilla, ver una vista previa del contenido y crear un documento nuevo.

1. Pulse [Herramientas de documentos] en la barra de herramientas y abra la pestaña [Crear].
2. Pulse [Crear a partir de una plantilla] y elija una plantilla.
3. Complete los campos (título, resumen, etc.). Los campos obligatorios se indican con «Obligatorio».
4. Escriba la ubicación de destino como una ruta relativa a la raíz de documentación (por ejemplo, `03-design/api.md`).
5. Pulse [Vista previa] y revise el Markdown generado.
6. Pulse [Crear con este contenido].
   El documento se crea y se muestra en el visor. A continuación se ejecuta la comprobación de toda la raíz de documentación.

## Plantillas disponibles

| Plantilla | Contenido |
|---|---|
| Documento de una página | Una especificación breve, notas o un documento explicativo independiente en un solo archivo |
| Especificación, manual y ayuda | Un solo archivo con una estructura de capítulos general, apta para especificaciones, manuales y ayuda |
| Plantillas de Standard Pack | Si en `lunascape-docs.json` está seleccionado Standard Pack, se añaden los tipos de documento disponibles en ese perfil (documento de requisitos, documento de diseño, etc.) |

> **Nota**
>
> - Para crear documentos se necesita un área de trabajo de confianza.
> - Los archivos existentes no se sobrescriben. Si en el destino ya hay un documento con el mismo nombre, no se puede crear.
> - El destino necesita la extensión `.md` o `.mdx`. No se puede crear nada dentro de `i18n` (donde están las traducciones).
> - Después de modificar los datos introducidos, pulse [Vista previa] de nuevo antes de crear el documento.

> **Sugerencia**
>
> En un proyecto que todavía no tiene una carpeta de documentos, puede crear el primer conjunto con «Lunascape Docs: Crear documentación a partir de una plantilla» en la paleta de comandos. Consulte [Crear sus primeros documentos](../01-introduction/first-documents.md).

## Temas relacionados

- [Usar las Herramientas de documentos](README.md)
- [Cambiar las reglas de comprobación](rules.md)
