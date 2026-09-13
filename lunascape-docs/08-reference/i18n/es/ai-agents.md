# Uso desde agentes de IA

La extensión registra en VS Code la herramienta de modelo de lenguaje (Language Model Tool) de solo lectura `lunascape_getDocsSpecification`. Cuando se le pregunta a un agente de VS Code compatible sobre las funciones, la configuración o las convenciones de documentos de Lunascape Docs, este puede obtener el contenido de esta ayuda (la especificación general) mediante dicha herramienta.

## Cómo usarla

Pregunta en el chat de VS Code añadiendo `#lunascapeDocs`, o simplemente pregunta sobre la configuración o la estructura de documentos de Lunascape Docs.

```text
#lunascapeDocs #lunascapeDocs ¿Cómo habilito las traducciones al inglés en lunascape-docs.json?
```

## Argumentos de la herramienta

| Argumento | Significado |
|---|---|
| `topic` | La sección que se va a obtener: `all`, `usage` (Operaciones básicas), `structure` (Raíces de documentación y convenciones de archivos), `editing` (Editar un documento), `configuration` (Configuración del proyecto), `security` (Seguridad y límites de escritura) o `ai` (Uso desde agentes de IA) |
| `locale` | El idioma de la ayuda (una etiqueta de idioma de la ayuda incluida, como `ja` o `en`). Si se omite, se usa el idioma de visualización de VS Code y, en su defecto, la ayuda en japonés |

> **Nota**
>
> - La herramienta nunca envía el contenido de los documentos a ningún sitio.
> - La herramienta nunca devuelve nombres de áreas de trabajo ni rutas locales.
> - La herramienta nunca modifica archivos.
> - Funciona desde agentes de VS Code compatibles sin necesidad de un `AGENTS.md`. No se comparte automáticamente con otros clientes de IA que no usen la API de herramientas de la extensión.

## Temas relacionados

- [Mostrar esta ayuda](../02-reading/help.md)
- [Seguridad y límites de escritura](security.md)
