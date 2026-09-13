# Mostrar la información del documento

La «tabla de control del documento» que se coloca al comienzo de un documento (una tabla con el ID de documento, la versión, la fecha de actualización, el estado, etc.) se agrupa, al leer, en una fila compacta de «información del documento». El Markdown en sí sigue siendo una tabla normal, por lo que también se puede leer tal cual en GitHub.

## Condiciones

Coloque una tabla de dos columnas como la siguiente inmediatamente después del encabezado (H1).

```markdown
# Requisitos funcionales

| 項目 | 内容 |
|---|---|
| 文書ID | REQ-001 |
| 版 | 1.0 |
| 更新日 | 2026-08-31 |
| 状態 | 承認済み |
| 文書責任者 | G.U.Corp |
```

- La condición es que exista una fila de ID de documento y varios campos de gestión.
- También se reconoce una tabla colocada bajo un encabezado `## 文書管理` o `## Document information`.
- Las tablas que están en medio del texto y las tablas genéricas de «elemento/valor» no se convierten.

## Cómo se muestra

- Al leer, solo se muestran el estado y la fecha de actualización, en tamaño pequeño.
- Al pulsar la fila, se muestran todos los campos.
- Al imprimir, se muestran todos los campos.
- En el editor, la tabla se muestra como una tabla normal y se puede editar como tal.

> **Consejo**
>
> Si quiere mostrarla siempre como tabla en lugar de contraerla, desactive [Contraer los datos del documento] en [Configuración de visualización].

## Temas relacionados

- [Editar un documento](README.md)
- [Cambiar los ajustes de visualización](../02-reading/display-settings.md)
