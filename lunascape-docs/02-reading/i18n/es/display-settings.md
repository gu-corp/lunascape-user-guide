# Cambiar la configuración de visualización

Desde [Configuración de visualización] (engranaje) en la barra de herramientas, cada usuario puede cambiar el aspecto del INDEX y la visibilidad del botón de edición.

1. Pulse [Configuración de visualización] en la barra de herramientas.
2. Active o desactive los elementos que desee cambiar. Los cambios se aplican de inmediato.
3. Pulse [Configuración de visualización] de nuevo, o haga clic fuera del panel, para cerrarlo.

## Elementos configurables

| Sección | Elemento | Función |
|---|---|---|
| Idioma del documento | (estado actual) | Muestra el idioma predeterminado del proyecto y el idioma que se está viendo. [Configurar los idiomas del proyecto…] abre la configuración de idiomas del proyecto |
| Contenido | [Nombres de archivo] | Muestra el nombre del archivo en lugar del título del documento |
| | [Iconos de documento] | Muestra un icono en los elementos de documento |
| | [Iconos de carpeta] | Muestra un icono en los elementos de carpeta |
| | [Número de elementos por carpeta] | Muestra la cantidad de documentos que contiene cada carpeta |
| | [Guías de jerarquía] | Muestra líneas guía que indican la jerarquía |
| | [Ocultar si solo hay un documento] | En una raíz de documentación con un solo documento, cierra el INDEX automáticamente la primera vez |
| | [Contraer los datos del documento] | Contrae la tabla de control del inicio del documento en una fila «Datos del documento». Si se desactiva, la tabla se muestra tal cual |
| | [Densidad de visualización] | Elige el interlineado del INDEX entre [Normal] y [Compacta] |
| | [Botón de edición] | Muestra [Editar] en la parte inferior derecha del cuerpo del documento |
| Acciones | [Restablecer los valores predeterminados del proyecto] | Elimina todos los cambios del usuario y vuelve a la configuración del proyecto |
| | [Abrir la configuración de la extensión] | Abre la configuración de Lunascape Docs en la pantalla de configuración de VS Code |

> **Sugerencia**
>
> - La configuración de visualización se guarda por usuario y por raíz de documentación, y no se escribe en archivos gestionados por Git.
> - La configuración se aplica en este orden de prioridad: «configuración de visualización del usuario → configuración de VS Code → `lunascape-docs.json` → valores predeterminados del producto». Los valores predeterminados comunes del equipo se definen en `tree` y `editor` de `lunascape-docs.json`.

## Cambiar la combinación de colores

Al pulsar el selector de tema (sol/luna) de la barra de herramientas, se alterna entre el fondo blanco y la combinación de colores de VS Code. La combinación de colores al abrir se determina con la configuración `lunascapeDocEditor.appearance` (`light` o `auto`).

## Temas relacionados

- [Usar el INDEX](index-panel.md)
- [Configuración del proyecto](../04-document-tools/project-configuration.md)
- [Lista de configuraciones de VS Code](../08-reference/settings.md)
