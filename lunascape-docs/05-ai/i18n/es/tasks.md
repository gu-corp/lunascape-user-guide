# Trabajos disponibles

Se eligen en [Trabajo], dentro de la pestaña [AI]. Cada trabajo cambia la instrucción que se entrega y la comprobación posterior.

| Trabajo | Contenido | Requisitos | Tipo de API |
|---|---|---|---|
| Traducir esta página | Traduce el documento en pantalla al idioma elegido | Tener abierto el documento, un idioma de destino | Sí |
| Traducir lo que falta | Traduce, uno tras otro, los documentos sin traducir y desactualizados del idioma elegido | Un idioma de destino | Solo de sesión |
| Corregir esta página | Revisa y corrige la terminología, el estilo y los apartados que exige la norma de documentos | Tener abierto el documento | Sí |
| Crear un documento nuevo | Crea un documento siguiendo la norma de documentos y sus plantillas | Un tema (opcional) | Solo de sesión |

## Qué incluye la instrucción

| N.º | Contenido |
|---|---|
| 1 | La ubicación de la raíz de documentación, con la indicación de no modificar nada fuera de ella |
| 2 | El idioma predeterminado (documento original) y el lugar de las traducciones: la carpeta `i18n/<idioma>/` junto al documento |
| 3 | Que `navigation.order` solo pertenece al documento original y que una traducción únicamente puede sustituir `navigation.title` |
| 4 | Que no se modifiquen los ID de requisito, los enlaces, el código, Mermaid, TeX ni la estructura del front matter |
| 5 | La norma de documentos y el glosario (`terminology` en `docs-lint.config.json`) |
| 6 | Ejecutar al terminar la comprobación de documentos, informar de los archivos modificados y no realizar operaciones de Git |

> **Sugerencia**
>
> Los documentos de «Traducir lo que falta» se toman del registro, hasta 200 por ejecución. Si hay más, vuelva a ejecutarlo.

## Temas relacionados

- [Entregar trabajo a una IA](README.md)
- [El registro y sus anotaciones](ledger.md)
