# Abrir un repositorio de GitHub

En la versión Web, los documentos se abren indicando un repositorio de GitHub. Si el repositorio es público, no hace falta iniciar sesión.

## Abrir desde la pantalla

1. Abra <https://docs.lunascape.org/>.
2. Pulse [Abrir documentos] (el icono de carpeta) en la barra de herramientas.
3. Escriba el repositorio en [Especificar un repositorio] y pulse [Abrir].
   Si ha iniciado sesión en GitHub, también puede elegirlo de la lista en [Elegir entre los repositorios que puede leer].

> **Sugerencia**
>
> - El icono de GitHub que está al lado abre en github.com el documento que está leyendo. No sirve para abrir documentos.

## Abrir mediante una URL

La dirección coloca el repositorio y la ubicación del documento tal cual, uno tras otro. La ruta es la ubicación dentro del repositorio, así que el orden es el mismo que en la URL de GitHub.

```text
https://docs.lunascape.org/github/owner/repo/docs/01-product/vision.md
```

| Qué se indica | Cómo se escribe |
|---|---|
| Solo el repositorio (rama predeterminada) | `/github/owner/repo` |
| Un documento dentro del repositorio | `/github/owner/repo/docs/01-product/vision.md` |
| Una rama o una etiqueta | añada `?ref=v1.2.0` al final |

La dirección cambia a medida que se desplaza por las páginas. Pulse [Compartir este documento] en la barra de herramientas para entregar a alguien un enlace a la página que está leyendo. Los botones [Atrás] y [Adelante] del navegador también funcionan.

La forma anterior con `?source=` se sigue abriendo igual que antes. Una vez abierta, se reescribe en la forma nueva.

```text
https://docs.lunascape.org/?source=github:owner/repo@main/docs#/01-product/vision.md
```

> **Nota**
>
> - Sin haber iniciado sesión, se aplica el límite de uso de la API de GitHub (60 solicitudes por hora). En repositorios con muchos documentos o si consulta repetidamente, use [Iniciar sesión con GitHub].
> - Los nombres de rama que contienen `/` (como `feature/xxx`) se pueden indicar con `?ref=` en el formato de dirección anterior. La forma con `?source=` no permite escribirlos.
> - Los documentos se cargan con los permisos de GitHub de quien los lee. Quien no tenga permiso de lectura no los verá.

## Abrir documentos de una carpeta local

Pulse [Abrir documentos] en la barra de herramientas y, debajo de la lista, elija [Abrir documentos de una carpeta local] para seleccionar una carpeta de su equipo. Los archivos se procesan dentro del navegador y no se envían a ningún sitio. Funciona en navegadores compatibles con la selección de carpetas (Chrome, Edge y otros).

## Temas relacionados

- [Consultar un repositorio privado](private-repository.md)
- [No se puede abrir o iniciar sesión en la versión Web](../07-troubleshooting/web.md)
