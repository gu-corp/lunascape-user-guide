# Configurar la información de navegación

El nombre y el orden que se muestran en el INDEX se escriben en el YAML front matter de cada documento. Aunque no se escriba, el documento se muestra igualmente usando el encabezado (H1) y el orden por nombre de archivo.

## Nombre y orden del documento

Escribe lo siguiente al principio del documento.

```yaml
---
navigation:
  title: Introducción
  order: 200
---
```

| Campo | Significado |
|---|---|
| `navigation.title` | El nombre que se muestra en el INDEX. Si se omite, se usa el H1 y, en su defecto, el nombre de archivo |
| `navigation.order` | Un número entero que determina el orden. Se ordena de menor a mayor. Si se omite, se aplica un orden predeterminado estable (por nombre de archivo) |

> **Sugerencia**
>
> - Asigna los valores de `order` en pasos de 100, como 100, 200, 300, para poder intercalar después un 150 entre ellos.
> - Aunque haya valores de `order` sin especificar, no válidos o duplicados, el documento no se oculta.
> - Al reordenar en el INDEX, `navigation.order` se escribe automáticamente. No hace falta escribirlo a mano.

## Nombre y orden de la carpeta

El nombre y el orden de una carpeta los guarda el front matter de su `README.md` (o `index.md` si no hay README). No es necesario que la portada tenga contenido en el cuerpo.

```yaml
---
navigation:
  title: Planificación de productos
  order: 100
---
```

Una carpeta sin portada se muestra con el nombre de la carpeta y el orden predeterminado. Cuando un cambio de título o una reordenación en el INDEX lo requiere, se crea un `README.md` que solo contiene el front matter. La simple lectura nunca crea un archivo.

## Tratamiento en las versiones traducidas

- El orden y el rol de una carpeta (portada o solo de configuración) los decide únicamente el documento en el idioma predeterminado.
- Una traducción solo puede sobrescribir `navigation.title`. Cuando el documento canónico tiene contenido en el cuerpo, el H1 de la traducción también se usa como nombre.
- Que solo exista una traducción no añade ninguna página.

## Orden y plegado de los elementos secundarios

En la portada de una carpeta están definidos `navigation.children.sort` y `navigation.children.defaultCollapsed`, que especifican cómo se ordenan los elementos secundarios directos y su estado de plegado inicial. La lectura y la edición en VS Code se admitirán próximamente.

## Temas relacionados

- [Cambiar el orden de los documentos](../03-editing/reorder.md)
- [Raíces de documentación y convenciones de archivos](structure.md)
