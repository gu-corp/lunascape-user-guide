# Seguridad y límites de escritura

Los límites que Lunascape Docs mantiene para proteger sus documentos y su equipo.

## Visualización

- El HTML generado a partir de Markdown y el SVG generado a partir de los diagramas se depuran con DOMPurify 3.4.14 antes de mostrarse.
- Los scripts arbitrarios incluidos en MDX nunca se ejecutan.
- KaTeX se ejecuta con `trust: false`, `maxSize: 50` y `maxExpand: 1000`, y no confía ni en el HTML externo ni en los comandos arbitrarios.
- Las bibliotecas de dibujo Markmap, WaveDrom, Svgbob, Vega-Lite y Penrose se cargan en el equipo, en versiones fijadas, solo cuando existe el bloque correspondiente. No se permiten las referencias a recursos externos, el HTML sin procesar ni las notaciones ejecutables, y se eliminan del SVG generado los scripts, las imágenes externas, `link`, `style` y `foreignObject`.
- El dibujo de TikZ no inicia el LaTeX del sistema anfitrión: se ejecuta de forma secuencial en un proceso de trabajo TeX en WebAssembly con un sistema de archivos en memoria. Tiene límites de entrada, cola de espera, memoria, tiempo de ejecución (15 segundos) y salida SVG, y rechaza las instrucciones de E/S de archivos.

## Acceso a los documentos y a los archivos

- Los enlaces de los documentos y las operaciones con archivos no pueden salir de la raíz de documentación.
- La creación, el cambio de nombre, el movimiento y la eliminación desde el INDEX se vuelven a verificar en la extensión —raíz de documentación, versión del INDEX, ruta del documento original, tipo del elemento de destino, límites de los enlaces simbólicos y documentos sin guardar— antes de aplicarse. Las solicitudes procedentes de un menú obsoleto o de otra raíz de documentación no se aplican.
- Las operaciones de modificación del INDEX se desactivan mientras se edita un documento o mientras se aplica otra operación del INDEX.
- La creación a partir de una plantilla vuelve a verificar, después de la vista previa, la confianza del área de trabajo, la identidad de la raíz de documentación, la versión del INDEX, el Standard Pack y el contenido generado, el destino y los límites de los enlaces simbólicos. Nunca sobrescribe un archivo existente ni crea contenido distinto del de la vista previa o cuyo resultado expandido supere los 4 MiB.
- Al guardar un archivo de configuración se comprueba su versión justo antes de guardar y la operación se cancela si se detecta un cambio externo.

## Envío al exterior

- Los documentos nunca se envían al exterior para su lectura, edición o comprobación. Las comprobaciones de documentos se ejecutan en el equipo de forma determinista.
- Solo la traducción (la traducción de esta página y la traducción por lotes) envía documentos a un modelo de lenguaje, tras indicar de antemano el destino y el alcance del envío y únicamente con una aprobación explícita. <!-- ai-only -->
- Las propuestas de traducción se presentan como diferencias, se vuelven a verificar las versiones del documento original y del documento de destino, y solo se aplican cuando una persona las guarda de forma explícita. <!-- ai-only -->
- La herramienta de especificación destinada a los agentes de IA no devuelve el contenido de los documentos, ni los nombres de las áreas de trabajo, ni las rutas locales. <!-- ai-only -->

## Git

- Al guardar solo se escribe en el archivo. Ninguna función prepara ni confirma cambios en Git de forma automática.
- Los archivos existentes, como `_meta.json`, nunca se eliminan ni se modifican de forma silenciosa. Las traducciones huérfanas tampoco se eliminan ni se mueven automáticamente.

## Temas relacionados

- [Especificaciones principales](README.md)
- [Uso desde la IA](ai-agents.md)
