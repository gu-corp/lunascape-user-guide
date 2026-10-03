# Abrir un repositorio de GitHub

En la versión web y en Lunascape, puede abrir y leer un repositorio de GitHub directamente, sin duplicarlo. Los repositorios públicos no requieren iniciar sesión.

## Abrir desde la pantalla

1. Pulse [Abrir documentos] (el icono de carpeta) en la barra de herramientas. Se abre la pantalla «Abrir documentos».
2. En la columna de la izquierda, elija dónde buscar.

   | Ubicación | Qué muestra |
   |---|---|
   | Todo | Todo lo de abajo. Lo abierto recientemente aparece primero |
   | Abiertos recientemente | Los repositorios y las carpetas que ha abierto hasta ahora |
   | Destacados | Los manuales que presenta el sitio |
   | Repositorios de GitHub | Si ha iniciado sesión con GitHub, los repositorios que usted puede leer |
   | Este equipo | Las carpetas de este dispositivo. En Lunascape, aquí también aparecen los repositorios duplicados |

3. Pulse [Abrir] en la fila que desee. Para filtrar las filas, escriba en [Filtrar por nombre de documento o de repositorio], en la parte superior.

Si un repositorio no aparece en la lista, indíquelo con [Introducir owner/repo y abrir], en la columna de la izquierda.

> **Sugerencia**
>
> - En la lista aparecen los repositorios de GitHub que tienen instalada la GitHub App «Lunascape Docs» y en los que usted tiene permiso de lectura. Si no encuentra un repositorio, pida a su propietario que añada la App.

## Comprobar la ubicación del documento

El pequeño icono de la parte izquierda de la barra de herramientas (el chip de ubicación) indica dónde está el documento que está leyendo.

| Icono | Ubicación |
|---|---|
| El logotipo de GitHub | Lo está leyendo desde GitHub. No está guardado en este dispositivo |
| Un equipo portátil | Una carpeta de este dispositivo administrada por Lunascape. También se muestran el nombre de la rama de Git y el número de archivos modificados |
| Una carpeta | Una carpeta de este dispositivo |

Al pulsar el icono, se muestran la ubicación, su estado y las operaciones disponibles desde ahí ([Ver en GitHub], [Copiar enlace], etc.).

## Duplicar un repositorio en Lunascape

En Lunascape, puede duplicar un repositorio de GitHub en este dispositivo para editarlo y confirmar cambios con Git.

- En la pantalla «Abrir documentos», pulse [Duplicar] en la fila del repositorio.
- Si está leyendo un repositorio abierto desde GitHub, pulse el chip de ubicación y, a continuación, pulse [Duplicar en este equipo]. Cuando termina la duplicación, el mismo documento se abre desde la copia de este dispositivo.

En la lista, los repositorios duplicados se indican con «En este equipo», y [Abrir en este equipo] aparece en primer lugar.

## Abrir mediante una URL

La dirección indica el repositorio y la ubicación del documento, uno tras otro. La ruta es la ubicación dentro del repositorio, así que sigue el mismo orden que la URL de GitHub.

```text
https://docs.lunascape.org/github/owner/repo/docs/01-product/vision.md
```

| Qué se indica | Cómo se escribe |
|---|---|
| Solo el repositorio (rama predeterminada) | `/github/owner/repo` |
| Un documento dentro del repositorio | `/github/owner/repo/docs/01-product/vision.md` |
| Una rama o una etiqueta concreta | Añada `?ref=v1.2.0` al final |

Al cambiar de página, la dirección también cambia. Para pasar a otra persona un enlace a la página que está leyendo, pulse [Compartir este documento] en la barra de herramientas. También puede usar los botones [Atrás] y [Adelante] del navegador.

Las direcciones con la forma anterior `?source=` se siguen abriendo como antes. Una vez abiertas, se reescriben con la forma nueva.

```text
https://docs.lunascape.org/?source=github:owner/repo@main/docs#/01-product/vision.md
```

> **Nota**
>
> - Si no ha iniciado sesión, se aplica el límite de uso de la API de GitHub (60 solicitudes por hora). Para repositorios con muchos documentos o para consultas repetidas, pulse [Iniciar sesión con GitHub].
> - Los nombres de rama que contienen `/` (como `feature/xxx`) se pueden indicar con `?ref=` en el formato de dirección descrito arriba. No se pueden escribir con la forma `?source=`.
> - Los documentos se cargan con los permisos de GitHub de quien los lee. Las personas sin permiso de lectura no los ven.

## Abrir documentos de una carpeta local

Pulse [Abrir documentos] en la barra de herramientas y, en la columna de la izquierda, pulse [Abrir documentos de una carpeta local] y elija una carpeta de este dispositivo. Los archivos se procesan dentro del navegador y nunca se envían al exterior. Esta función está disponible en los navegadores que permiten seleccionar carpetas (Chrome, Edge, etc.).

## Temas relacionados

- [Consultar un repositorio privado](private-repository.md)
- [La versión web no se abre o no permite iniciar sesión](../07-troubleshooting/web.md)
