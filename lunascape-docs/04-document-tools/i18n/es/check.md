# Comprobar los documentos

Con docs-lint puede revisar la estructura de los encabezados, los enlaces rotos, la falta de documentos o capítulos obligatorios, las inconsistencias terminológicas y la coherencia de los ID de requisito, entre otros aspectos. La comprobación se realiza siempre sobre toda la raíz de documentación.

## Ejecutar una comprobación

1. Pulse [Herramientas de documentos] en la barra de herramientas y abra la pestaña [Comprobación].
2. Pulse [Comprobar la raíz de documentación].
   También puede ejecutarla desde la paleta de comandos con «Lunascape Docs: Comprobar la raíz de documentación».
3. Revise la lista de resultados.

## Leer los resultados

- Con [Este documento] / [Todo], encima de la lista, cambia el alcance de lo que se muestra. El alcance de la comprobación en sí es siempre toda la raíz de documentación.
- Los avisos tienen cuatro niveles: «error», «advertencia», «información» y «sugerencia». En [Herramientas de documentos], en la barra de herramientas, se muestra el número de errores y advertencias.
- Al pulsar un aviso se abre en el editor de VS Code la posición correspondiente del código fuente Markdown.
- Los avisos que afectan a toda la raíz de documentación (por ejemplo, la falta de un documento de pruebas) aparecen como elementos de «toda la raíz de documentación» y no tienen posición.
- Los mismos avisos aparecen también en el panel «Problemas» de VS Code.

## Elementos que se comprueban

Si pulsa [Revisar y cambiar las reglas], se muestra la lista de comprobaciones activas y la finalidad de cada una. Los elementos principales son los siguientes.

| Elemento | Contenido |
|---|---|
| Estructura de los encabezados | Que haya un único H1 y que los niveles de encabezado no se salten |
| Enlaces internos | Que el documento de destino exista y no quede fuera de la raíz de documentación |
| Lenguaje de los bloques de código | Que los bloques de código indiquen el nombre del lenguaje |
| Carpetas y documentos necesarios | Que estén todas las carpetas y documentos que exige el perfil del Standard Pack |
| Capítulos necesarios en el documento | Que cada tipo de documento tenga los capítulos necesarios |
| Unificación terminológica | Detecta las expresiones que deben evitarse y propone unificar con el término recomendado |
| Nomenclatura y duplicados de los ID de requisito | Que los ID de requisito sigan la regla de nomenclatura y no estén definidos dos veces |
| Coherencia de las referencias a los ID de requisito | Que existan los ID de requisito a los que remiten el diseño, las pruebas o las tablas de estado |
| Correspondencia entre requisitos y pruebas | Que los ID de requisito estén referenciados desde los documentos de pruebas |

Los elementos que se activan dependen del Standard Pack y del perfil elegidos en `lunascape-docs.json`, así como de `docs-lint.config.json`.

> **Nota**
>
> - Al modificar un documento o una configuración, el resultado anterior pasa a «requiere nueva comprobación». No se da por aprobado automáticamente. Vuelva a pulsar [Comprobar la raíz de documentación].
> - Los cambios sin guardar no se reflejan en la comprobación. Guarde primero.
> - La comprobación se ejecuta de forma determinista en el equipo. Los resultados de las evaluaciones o traducciones de la IA nunca se mezclan con los resultados de la comprobación.

## Temas relacionados

- [Cambiar las reglas de comprobación](rules.md)
- [Configuración del proyecto](project-configuration.md)
- [La comprobación, la creación o la traducción no funcionan](../07-troubleshooting/tools.md)
