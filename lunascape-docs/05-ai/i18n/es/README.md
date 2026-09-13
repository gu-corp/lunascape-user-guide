# Entregar el trabajo a una IA

Lunascape Docs no llama a ningún modelo de lenguaje. Prepara **el contexto, las herramientas y las comprobaciones**, y deja la traducción, la corrección y la redacción a la IA que usted ya utiliza.

## La idea

| Lo que aporta el producto | Contenido |
|---|---|
| Contexto | Las convenciones de la documentación (dónde se guardan las traducciones, el front matter, el estándar de documentos, el glosario) y la ubicación del documento de destino |
| Herramientas de trabajo | El registro de traducciones sin traducir y desactualizadas, la lectura y escritura de documentos, la creación a partir de plantillas |
| Comprobaciones posteriores | La verificación con docs-lint y la diferencia de cobertura y actualidad |

La instrucción no incluye el texto del documento. La IA lee los archivos, los escribe y los verifica por sí misma.

## Entregar un trabajo

1. Pulse [Herramientas de documentos] en la barra de herramientas y abra la pestaña [IA].
2. Elija el trabajo que desea entregar en [Tarea].
3. Complete los datos necesarios (idioma de destino, tema).
4. Pulse [Entregar esta tarea].
   Se abre un terminal de VS Code y la IA elegida recibe la instrucción y comienza a trabajar.

> **Sugerencia**
>
> La sesión de Claude Code va acompañada de las herramientas de trabajo (el servidor MCP `lunascape-docs`). La sesión puede obtener por sí misma la lista de documentos sin traducir y desactualizados, ejecutar docs-lint y registrar la actualidad después de traducir.

## Revisar el resultado

| Tipo de proveedor | Dónde llega el resultado |
|---|---|
| De sesión (Claude Code, Codex) | Escribe directamente en el árbol de trabajo. **Revíselo en las diferencias de Git** |
| De API (modelos de lenguaje de VS Code, Anthropic, compatibles con OpenAI) | Devuelve una propuesta por documento. Revísela con [Abrir diferencias] y escríbala con [Guardar] |

### Revisar una propuesta de tipo API

Al ejecutar con un proveedor de tipo API, la propuesta llega a la pestaña [IA].

1. Pulse [Abrir diferencias] y compare la propuesta con el contenido actual.
2. Si le parece bien, pulse [Guardar]. En el caso de una traducción, también se registra la actualidad. Para descartarla, pulse [Descartar].
   Para detener la generación a mitad de camino, pulse [Detener].

> **Nota**
>
> - Lunascape Docs nunca prepara ni confirma cambios en Git. Revise siempre los cambios en las diferencias.
> - No se puede entregar trabajo en un área de trabajo que no sea de confianza ni mientras se ve temporalmente una carpeta fuera de la raíz de documentación.

## Temas relacionados

- [Trabajos que puede entregar](tasks.md)
- [Configuración de IA](settings.md)
- [El registro y sus datos](ledger.md)
