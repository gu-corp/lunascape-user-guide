# Abrir un repositorio de GitHub

En la versión web puede abrir y leer un repositorio de GitHub directamente, sin clonarlo. Los repositorios públicos no requieren iniciar sesión.

## Abrir desde la pantalla

1. Pulse [Abrir documentos] (el icono de carpeta) en la barra de herramientas. Se abre la pantalla «Abrir documentos».
2. En la columna de la izquierda, elija la ubicación que quiere abrir.

   | Ubicación | Qué muestra |
   |---|---|
   | Todo | Todo lo de abajo. Lo que abrió recientemente aparece primero |
   | Abiertos recientemente | Los repositorios y las carpetas que ha abierto |
   | Destacados | Los manuales que presenta el sitio |
   | Repositorios de GitHub | Si ha iniciado sesión en GitHub, los repositorios que puede leer |
   | Este equipo | Las carpetas de este dispositivo |

3. Pulse [Abrir] en la fila que desee. Para reducir las filas, escriba en [Filtrar por nombre de documento o de repositorio], en la parte superior.

Si el repositorio no aparece en la lista, indíquelo con [Introducir owner/repo y abrir] en la columna de la izquierda.

> **Consejo**
>
> - Los repositorios de GitHub de la lista son aquellos que tienen instalada la GitHub App «Lunascape Docs» y sobre los que usted tiene permiso de lectura. Si no encuentra uno, pida al propietario del repositorio que agregue la App.

## Comprobar dónde está un documento

El pequeño icono situado a la izquierda de la barra de herramientas (el chip de ubicación) indica dónde está el documento que está leyendo.

| Icono | Ubicación |
|---|---|
| El logotipo de GitHub | Se lee desde GitHub. No está guardado en este dispositivo |
| Carpeta | Una carpeta de este dispositivo |

Al pulsar el icono se muestran la ubicación, su estado y las acciones disponibles desde ahí ([Ver en GitHub], [Copiar enlace], etc.).

## Abrir mediante una URL

La dirección indica el repositorio y la posición del documento, uno tras otro. La ruta es la posición dentro del repositorio, por lo que sigue el mismo orden que la URL de GitHub.

```text
https://docs.lunascape.org/github/owner/repo/docs/01-product/vision.md
```

| Qué se indica | Cómo se escribe |
|---|---|
| Solo el repositorio (rama predeterminada) | `/github/owner/repo` |
| Un documento dentro del repositorio | `/github/owner/repo/docs/01-product/vision.md` |
| Una rama o una etiqueta | Añada `?ref=v1.2.0` al final |

Al cambiar de página, la dirección también cambia. Pulse [Compartir este documento] en la barra de herramientas para enviar un enlace a la página que está leyendo. También puede usar los botones [Atrás] y [Adelante] del navegador.

La forma anterior con `?source=` se sigue abriendo como hasta ahora. Una vez abierta, la dirección se reescribe con la forma nueva.

```text
https://docs.lunascape.org/?source=github:owner/repo@main/docs#/01-product/vision.md
```

> **Atención**
>
> - Si no ha iniciado sesión, se aplica el límite de uso de la API de GitHub (60 solicitudes por hora). Para repositorios con muchos documentos o para lecturas repetidas, use [Iniciar sesión con GitHub].
> - Los nombres de rama que contienen `/` (como `feature/xxx`) se pueden indicar con `?ref=` en el formato de dirección descrito arriba. No se pueden escribir con la forma `?source=`.
> - Los documentos se cargan con los permisos de GitHub de quien los lee. Las personas sin permiso de lectura no pueden verlos.

## Abrir documentos de una carpeta local

Pulse [Abrir documentos] en la barra de herramientas y, en la columna de la izquierda, use [Abrir documentos de una carpeta local] para elegir una carpeta del dispositivo. Los archivos se procesan dentro del navegador y nunca se envían al exterior. Funciona en navegadores compatibles con la selección de carpetas (Chrome, Edge, etc.).

## Temas relacionados

- [Ver un repositorio privado](private-repository.md)
- [No se puede abrir la versión web o no se puede iniciar sesión](../07-troubleshooting/web.md)
