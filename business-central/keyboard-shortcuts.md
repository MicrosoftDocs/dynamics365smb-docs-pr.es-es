---
title: Métodos abreviados
description: La lista completa de combinaciones de método abreviado de teclado para trabajar de manera eficaz con los datos.
author: jswymer
ms.topic: conceptual
ms.search.keywords: 'accessibility, shortcuts, keyboarding, keys'
ms.date: 02/09/2023
ms.author: jswymer
ms.review: jswymer
ms.service: dynamics365-business-central
ms.custom: bap-template
---

# <a name="keyboard-shortcuts"></a>Métodos abreviados de teclado

Este producto proporciona un resumen de algunas de las combinaciones de métodos abreviados que se pueden utilizar cuando trabaje con [!INCLUDE[prod_short](includes/prod_short.md)].

Para obtener una descripción general de los métodos abreviados de teclado más populares, vea [Métodos abreviados de teclado (solo PC)](keyboard-shortcuts-cheatsheet.md).

> [!TIP]
> Para obtener una vista gráfica de los métodos abreviados más utilizados, elija la siguiente imagen y descargue el archivo PDF.  
> [ ![Icono para el archivo PDF.](media/keyboard_shortcut_inline.png) ](media/keyboard_shortcuts.pdf "Icono que abre un PDF")

## <a name="overview"></a>Panorama

Los métodos abreviados de teclado ayudan a la accesibilidad y pueden hacer que sea más fácil y más eficiente navegar por diferentes áreas y elementos en una página. Son compatibles con la mayoría de los exploradores web; sin embargo el comportamiento puede variar ligeramente.

> [!NOTE]
> Los métodos abreviados de teclado aquí descritos se refieren al diseño del teclado de EE. UU. Puede que la distribución de las teclas de otros teclados no se corresponda exactamente con las teclas de un teclado de Estados Unidos.

La mayoría de los accesos directos son los mismos independientemente de que el sistema operativo sea Windows o macOS. Sin embargo, algunos accesos directos son distintos para macOS. Estos métodos abreviados de teclado se indican entre paréntesis en las siguientes secciones.

> [!NOTE]
> Además de los métodos abreviados de teclado globales descritos en este artículo, hay disponibles varios métodos específicos de la empresa. Por ejemplo, en la versión genérica de [!INCLUDE[prod_short](includes/prod_short.md)], <kbd>F9</kbd> publica un documento y <kbd>Ctrl</kbd>+<kbd>F7</kbd> muestra las entradas contables de un registro al abrirlo en una tarjeta. Este artículo incluye algunos de los atajos específicos de negocios más comunes, que se muestran en cursiva. Tenga en cuenta que los atajos reales pueden ser diferentes en su solución. En la interfaz de usuario, el método abreviado de teclado se muestra en la información sobre herramientas de la acción en cuestión.

## <a name="general-keyboard-shortcuts"></a><a name="Keyboard"></a> Métodos abreviados de teclado generales

En la siguiente tabla se describen métodos abreviados de teclado para navegar y acceder a diferentes elementos de una página. Los elementos incluyen cosas como acciones, listas desplegables, búsquedas y más. Para obtener más información sobre los métodos abreviados de teclado para navegar por los registros una vez que entra en una lista, consulte la siguiente sección.

|Seleccione estas teclas<br />(en macOS)|Para hacer esto|
|--------------------------------|----------|
|<kbd>Alt</kbd>|Muestra las teclas de acceso para seleccionar acciones en la barra de acciones y el menú de navegación de la página. Para obtener más información, vaya a [Claves de acceso](#access-keys-for-action-bar-and-navigation-menu).|
|<kbd>Alt</kbd>+<kbd>flecha arriba</kbd>|Abra una lista desplegable o busque un valor de un campo.|
|<kbd>Alt</kbd>+<kbd>flecha arriba</kbd>|Mostrar información sobre herramienta de un campo o encabezado de columna de una tabla. Si el campo contiene errores de validación, seleccione <kbd>Alt</kbd>+<kbd>flecha arriba</kbd> para mostrar el error de validación. Pulse <kbd>Esc</kbd> o <kbd>Alt</kbd>+<kbd>flecha arriba</kbd> para cerrar la información sobre herramientas.|
|<kbd>F2</kbd>|Alterne entre seleccionar todo el valor del campo o colocar el cursor al final del valor del campo.|
|<kbd>Alt</kbd>+<kbd>F2</kbd>|Mostrar u ocultar el panel de cuadro informativo.|
|<kbd>Alt</kbd>+<kbd>Mayús</kbd>+<kbd>F2</kbd>|<kbd>Cambiar</kbd> entre **Detalles** y **Archivos adjuntos** en el panel del cuadro informativo.|
|<kbd>Alt</kbd>+<kbd>O</kbd>|Agregar una nueva nota para el registro seleccionado, incluso si el panel del cuadro informativo no está abierto.|
|<kbd>Alt</kbd>+<kbd>Q</kbd><br /><br />(<kbd>Ctrl</kbd>+<kbd>Opción</kbd>+<kbd>Q</kbd>)|Abrir la ventana **Dígame**. Para obtener más información, consulte [Búsqueda de páginas e información con Dígame](ui-search.md).|
|<kbd>Ctrl</kbd>+<kbd>Alt</kbd>+<kbd>Q</kbd><br /><br />(<kbd>Ctrl</kbd>+<kbd>Opción</kbd>+<kbd>Cmd</kbd>+<kbd>Q</kbd>)|Abra la página **Buscar movimientos** para buscar documentos y movimientos relacionados entre sí en función de información común, como el número de documento o la fecha de publicación. Para más información, consulte [Búsqueda de entradas relacionados para documentos publicados ](ui-find-entries.md)|
|<kbd>Alt</kbd>+<kbd>N</kbd> |Abrir una página para crear un nuevo registro. (Similar a elegir las acciones **Nuevo** y **+**).|
|<kbd>Alt</kbd>+<kbd>Mayús</kbd>+<kbd>N</kbd> |Cerrar una página recién creada y abrir una nueva para crear un nuevo registro. Del mismo modo, <kbd>Alt</kbd>+<kbd>F9</kbd> registra un documento y crea uno nuevo.|
|<kbd>Alt</kbd>+<kbd>T</kbd>|Abrir la página **Mi configuración**.|
|<kbd>Alt</kbd>+<kbd>Flecha hacia la derecha</kbd>|Buscar información adicional o valores subyacentes para un campo que contiene el botón ![AssistEdit.](media/assist-edit-icon.png "Botón AssistEdit") . Se usa cuando el botón desplegable habitual (<kbd>Alt</kbd>+<kbd>flecha arriba</kbd>) en el mismo campo se usa para otro propósito.|
|<kbd>Ctrl</kbd>+<kbd>Alt</kbd>+<kbd>Mayús</kbd>+<kbd>C</kbd>|Mostrar información en el distintivo de la empresa. A partir del segundo lanzamiento de versiones de 2022 de Business Central (versión 21), este método abreviado ya no es compatible, siendo sustituido por <kbd>Ctrl</kbd>+<kbd>O</kbd>. |
|<kbd>Ctrl</kbd>+<kbd>Alt</kbd>+<kbd>F1</kbd>|Abrir y cerrar el panel de inspección de la página. El panel de inspección de la página muestra información sobre la página, como su tabla de orígenes, campos, filtros, extensiones y más.<br /><br />Para obtener más información, vea [Inspección de páginas](across-inspect-page.md).|
|<kbd>Ctrl</kbd>+<kbd>C</kbd> |Copiar el valor del campo. Si el campo tiene el enfoque y no ha seleccionado ningún texto en el campo, se copiará todo el valor. Si ha seleccionado texto en el campo, solo copiará el texto seleccionado.|
|<kbd>Ctrl</kbd>+<kbd>F1</kbd>|Abra el [panel de ayuda](product-help-and-support.md#help-pane) o un artículo de ayuda de Business Central en [Microsoft Learn](/dynamics365/business-central/), dependiendo de su versión de Business Central.|
|<kbd>Ctrl</kbd>+<kbd>F12</kbd>|Cambiar entre vista de diseño amplia y estrecha.|
|<kbd>Ctrl</kbd>+Clic|Navegar durante la personalización cuando la acción está resaltada con una punta de flecha. Para obtener más información, consulte [Personalizar el área de trabajo](ui-personalization-user.md).|  
|<kbd>Ctrl</kbd>+<kbd>F5</kbd>|Volver a cargar la aplicación [!INCLUDE[prod_short](includes/prod_short.md)]. (Similar a seleccionar actualizar/recargar en el explorador).|
|<kbd>F5</kbd>|Actualizar los datos en la página actual.<br /><br />Utilice esta tecla para asegurarse de que los datos de la página estén actualizados con cualquier cambio que otros hayan hecho mientras usted trabaja.|
|<kbd>Ctrl</kbd>+<kbd>O</kbd>|Abra el panel **Empresas disponibles** para cambiar a otra empresa o entorno. Para más información, vea [Cambiar a otra empresa o entorno](ui-organization-switch.md).|
|<kbd>Entrar</kbd>|Habilite o acceda al elemento o control que tiene el enfoque.|
|<kbd>Esc</kbd>|Cerrar la página o lista desplegable actual.|
|<kbd>Tabulador</kbd>|Mueva el enfoque al control o elemento siguiente de una página, como acciones, botones, campos o encabezados de una lista.|
|<kbd>Mayús</kbd>+<kbd>Tabulador</kbd>|Mueva el enfoque al control o elemento anterior de una página, como acciones, botones, campos o encabezados de una lista.|
|<kbd>Y</kbd> y <kbd>N</kbd>|Activar los botones **Sí** y **No** en cuadros de diálogo. Las claves reales variarán según el idioma actual especificado en **Mi configuración**. Por ejemplo, seleccione <kbd>J</kbd> para activar el botón **Ja** cuando se utiliza el idioma alemán.|

## <a name="keyboard-shortcuts-in-lists"></a>Métodos abreviados de teclado en las listas

En la tabla siguiente se describen los métodos abreviados de teclado que puede usar en una página de lista. La acción de acceso directo es ligeramente diferente en función de si la página se muestra en la vista de lista o de mosaico.
<!--
> [!Note]
> In the table that follows, the term *actionable field* refers to a field on which you can do something, like change a value or link to another page. In general, the shortcuts will skip over fields that display information that you cannot change from the list (in other words, fields that are read-only).
-->
### <a name="general"></a>General

|Seleccione estas teclas<br />(en macOS)|Para hacerlo en una vista de lista|Para hacerlo en una vista de mosaico |
|--------------------------------|-------------------------|--------------------------|
|<kbd>Alt</kbd>+<kbd>F7</kbd> |Ordenar la columna seleccionada en orden ascendente o descendente.|No aplicable.|
|<kbd>Alt</kbd>+<kbd>N</kbd>|Insertar una nueva línea en una lista editable, como la página **Presupuestos contables**.|Igual.|
|<kbd>Mayús</kbd>+<kbd>F9</kbd>|Publica e imprime un documento.|Igual.|
|<kbd>Mayús</kbd>+<kbd>F10</kbd> |Abrir un menú de opciones que están disponibles para la fila seleccionada.|Igual.|
|<kbd>Alt</kbd>+<kbd>D</kbd>|Abre las entradas de grupo de dimensiones.|Igual.|
|<kbd>Ctrl</kbd>+<kbd>F7</kbd>|Abra entradas del libro mayor, entradas de registros, entradas de costos, etc.|
|<kbd>Ctrl</kbd>+<kbd>F9</kbd>|Lanzar documento.|Igual.|
|*<kbd>F7</kbd>*|Abrir estadísticas.|Igual.|
|*<kbd>F9</kbd>*|Publicar, emitir, registrar o anular el documento.|Igual.|
|*<kbd>Mayús</kbd>+<kbd>Ctrl</kbd>+<kbd>F</kbd>*|Envíe las líneas sugeridas en la página de hojas de cálculo de flujo de efectivo.|No aplicable.|
|*<kbd>Mayús</kbd>+<kbd>Ctrl</kbd>+<kbd>I</kbd>*|Ver números de serie y de lote asignados al producto de línea en el documento o diario.|No aplicable.|

### <a name="navigating-between-rows-and-columns"></a><a name="navigateshortcuts"></a>Navegación entre filas y columnas

Las cuadrículas con filas y columnas existen en muchos tipos de página en [!INCLUDE[prod_short](includes/prod_short.md)], como páginas de lista y partes de **Líneas** en documentos. Moverse de una celda a otra a través de una cuadrícula está totalmente preparado para el teclado.

| Seleccione estas teclas<br />(en macOS) | Para hacerlo en una vista de lista | Para hacerlo en una vista de mosaico |
|--|--|--|
| <kbd>Ctrl</kbd>+<kbd>Inicio</kbd><br /><br />(<kbd>Fn</kbd>+<kbd>Ctrl</kbd>+<kbd>Flecha izquierda</kbd>) | Seleccione la primera fila de la lista; el enfoque permanece en la misma columna. | Desplazarse al primer mosaico en la primera fila. |
| <kbd>Ctrl</kbd>+<kbd>Fin</kbd><br /><br />(<kbd>Fn</kbd>+<kbd>Ctrl</kbd>+<kbd>Flecha derecha</kbd>) | Seleccione la última fila de la lista; el enfoque permanece en la misma columna. | Desplazarse al último mosaico de la última fila. |
| <kbd>Inicio</kbd><br /><br />(<kbd>Fn</kbd>+<kbd>Flecha izquierda</kbd>) | Desplazarse al primer campo en una fila. | Desplazarse al primer mosaico en una fila. |
| <kbd>Fin</kbd><br /><br />(<kbd>Fn</kbd>+<kbd>Flecha derecha</kbd>) | Desplazarse al último campo en una fila. | Desplazarse al último mosaico en una fila. |
| <kbd>Introduzca</kbd> | Abre el registro asociado a este campo.<br /><br />Solo es relevante si una página de ficha está asociada con el registro. | Abre el registro.<br /><br />Solo es relevante si una página de ficha está asociada con el registro. |
| <kbd>Ctrl</kbd>+<kbd>Entrar</kbd> | Mueva el enfoque al siguiente elemento fuera de la lista. | Mueva el enfoque al siguiente elemento fuera de la lista. |
| <kbd>Re. pág.</kbd><br /><br />(<kbd>Fn</kbd>+<kbd>flecha arriba</kbd>) | Desplazarse para mostrar las filas establecidas por encima de las filas actuales a la vista. | Se desplaza para mostrar los mosaicos establecidos por encima de los mosaicos actuales a la vista. |
| <kbd>Av. Pág.</kbd><br /><br />(<kbd>Fn</kbd>+<kbd>flecha arriba</kbd>) | Desplazarse para mostrar las filas establecidas por debajo de las filas actuales a la vista. | Desplazarse para mostrar los mosaicos establecidos por debajo de los mosaicos actuales a la vista. |
| <kbd>Flecha hacia arriba</kbd> | En la misma columna, desplazarse al campo de la fila inferior. | En la misma columna, desplazarse al mosaico de la fila inferior. |
| <kbd>Flecha hacia arriba</kbd> | En la misma columna, desplazarse al campo de la fila superior. | En la misma columna, desplazarse al mosaico de la fila superior. |
| <kbd>Flecha hacia la derecha</kbd> | En una lista de solo lectura, desplácese en la misma fila al siguiente campo de la derecha.<br /><br />En una lista editable, desplácese a la derecha del campo actual. | En la misma fila, desplazarse al siguiente mosaico de la derecha. |
| <kbd>Flecha izquierda</kbd> | En una lista de solo lectura, desplácese en la misma fila al campo anterior de la izquierda. <br /><br />En una lista editable, desplácese a la izquierda del campo actual. | En la misma fila, desplazarse al mosaico anterior de la izquierda. |
| <kbd>Tab</kbd> | En una lista editable, desplácese en la misma fila al siguiente campo de la derecha. | No aplicable. | 
| <kbd>Mayús</kbd>+<kbd>Tabulador</kbd> | En una lista editable, desplácese en la misma fila al anterior campo de la izquierda. | No aplicable. |

### <a name="selecting-copying-and-pasting"></a><a name="CopyRows"></a>Selección, copia y pegado

|Seleccione estas teclas<br />(en macOS)|Para hacerlo en una vista de lista |Para hacerlo en una vista de mosaico |
|--------------------------------|--------------------------|--------------------------|
|<kbd>Ctrl</kbd>+Clic<br /><br />(<kbd>Cmd</kbd>+Clic)|Extienda la selección de filas para incluir la fila en la que hace clic.|No aplicable.|
|<kbd>Mayús</kbd>+Clic|Extienda la selección de filas para incluir la fila en la que hace clic y en todas las filas que hay en medio.<br /><br />Puede usar esto después de usar <kbd>Ctrl</kbd>+<kbd>Flecha arriba</kbd> o <kbd>Ctrl</kbd>+ Arriba/abajo para expandir la selección.|No aplicable.|
|<kbd>Ctrl</kbd>+<kbd>Flecha arriba</kbd><br /><br />(<kbd>Ctrl</kbd>+<kbd>Cmd</kbd>+<kbd>Flecha arriba</kbd>)|Mueva el enfoque de la fila superior y mantenga la fila actual seleccionada.|No aplicable.|
|<kbd>Ctrl</kbd>+<kbd>Flecha arriba</kbd><br /><br />(<kbd>Ctrl</kbd>+<kbd>Cmd</kbd>+<kbd>Flecha arriba</kbd>)|Mueva el enfoque de la fila inferior y mantenga la fila actual seleccionada.|No aplicable.|
|<kbd>Ctrl</kbd>+<kbd>Barra espaciadora</kbd><br /><br />(<kbd>Ctrl</kbd>+<kbd>Cmd</kbd>+Espacio)|Extienda la selección de filas para incluir la fila enfocada.<br /><br />Puede usar esto después de usar <kbd>Ctrl</kbd>+<kbd>Flecha arriba</kbd> o <kbd>Ctrl</kbd>+<kbd>Flecha abajo</kbd> para expandir su selección.|No aplicable.|
|<kbd>Ctrl</kbd>+<kbd>A</kbd>|Seleccionar todas las filas.|No aplicable.|
|<kbd>Ctrl</kbd>+<kbd>C</kbd><br /><br />(<kbd>Cmd</kbd>+<kbd>C</kbd>)|Copiar las filas seleccionadas al portapapeles.|Sí, pero solo para un único mosaico seleccionado.|
|<kbd>Ctrl</kbd>+<kbd>V</kbd><br /><br />(<kbd>Cmd</kbd>+<kbd>V</kbd>)|Pegar las filas seleccionadas del portapapeles en la página actual o en un documento externo, como Microsoft Excel o el correo electrónico de Outlook. Solo lo puede hacer en listas editables.|No aplicable.|
|<kbd>Mayús</kbd>+<kbd>Flecha arriba</kbd>|Extienda la selección de filas para incluir la fila superior.|No aplicable.|
|<kbd>Mayús</kbd>+<kbd>Flecha arriba</kbd>|Extienda la selección de filas para incluir la fila inferior.|No aplicable.|
|<kbd>Mayús</kbd>+<kbd>Re Pág</kbd><br /><br />(<kbd>Mayús</kbd>+<kbd>Fn</kbd>+<kbd>Flecha arriba</kbd>)|Extienda la selección de filas para incluir todas las filas visibles sobre la selección actual de filas.|No aplicable.|
|<kbd>Mayús</kbd>+<kbd>Av Pág</kbd><br /><br />(<kbd>Mayús</kbd>+<kbd>Fn</kbd>+<kbd>Flecha arriba</kbd>)|Extienda la selección de filas para incluir las filas visibles por debajo de la selección actual de filas.|No aplicable.|
|<kbd>F8</kbd>|Copie el campo en la misma columna de la fila anterior y péguelo en la fila actual. Solo lo puede hacer en listas editables. Mediante este método abreviado seguido de una <kbd>tabulación</kbd> podrá completar rápidamente los campos de los productos de la línea que desea que tengan el mismo valor que la fila anterior.|No aplicable.|

### <a name="searching-and-filtering-lists"></a><a name="KeyboardFilter"></a>Búsqueda y filtrado de listas

|Seleccione estas teclas<br />(en macOS)|Para hacer esto|
|--------------------------------|----------|
|<kbd>F3</kbd>|Alterna el cuadro de búsqueda.<ul><li>Se activa el cuadro de búsqueda, por lo que puede empezar a escribir el texto de búsqueda.</li><li>Si el cuadro de búsqueda ya está activado, <kbd>F3</kbd> vuelve a la lista sin borrar el texto de búsqueda.</li><ul>|
|<kbd>Mayús</kbd>+<kbd>F3</kbd>|Abrir y cerrar el panel de filtros.<ul><li> Si el panel de filtro no está abierto, <kbd>Mayús</kbd>+<kbd>F3</kbd> lo abre y se centra en la acción **+ Filtrar** bajo **Filtrar lista por**. Luego puede presionar <kbd>Entrar</kbd> para comenzar a agregar un filtro de campo.</li><li>Si el panel de filtro ya está abierto, <kbd>Mayús</kbd>+<kbd>F3</kbd> lo cierra, pero no borra ningún filtro que haya agregado.</li></ul>|
|<kbd>Ctrl</kbd>+<kbd>Mayús</kbd>+<kbd>F3</kbd>|Abrir y cerrar el panel de filtros.<ul><li> Si el panel de filtro no está abierto, <kbd>Ctrl</kbd>+<kbd>Mayús</kbd>+<kbd>F3</kbd> lo abre y se centra en la acción **+ Filtrar** bajo **Filtrar total por**. Luego puede presionar <kbd>Entrar</kbd> para comenzar a agregar un filtro de totales.</li><li>Si el panel de filtro ya está abierto, <kbd>Ctrol</kbd>+<kbd>Mayús</kbd>+<kbd>F3</kbd> lo cierra, pero no borra ningún filtro que haya agregado.</li></ul>  |
|<kbd>Alt</kbd>+<kbd>F3</kbd>|Alternar el filtrado al valor seleccionado.<ul><li>Aplica un filtro de columna en el valor del campo seleccionado en la lista. Esto es lo mismo que elegir **Filtrar a este valor** desde un encabezado de columna. Abre el panel de filtros, establece el filtro en el valor seleccionado, mientras que el foco permanece en la celda de la lista.</li><li>Si la columna ya está filtrada, <kbd>Alt</kbd>+<kbd>F3</kbd> borra el filtro en esa columna.</li></ul> |
|<kbd>Mayús</kbd>+<kbd>Alt</kbd>+<kbd>F3</kbd>|Abrir el panel de filtros y agregar un filtro en la columna seleccionada de la lista. El foco está en el nuevo campo de filtro, que le permite comenzar a escribir los criterios de filtro de inmediato.<br /><br /> Esto es lo mismo que seleccionar **Filtro** desde la cabecera de columna.<br /><br />Si ya existe un filtro en el campo, se agregará uno nuevo. |
|<kbd>Ctrl</kbd>+<kbd>Mayús</kbd>+<kbd>Alt</kbd>+<kbd>F3</kbd>|Restablecer filtros. Esto es lo mismo que elegir **Restablecer filtros** en el panel de filtro y se aplica a los filtros de campos y totales.<br /><br /> Los filtros vuelven a los filtros predeterminados para la vista actual. Si la vista actual es **Todos**, entonces es lo mismo que volver a una vista sin filtros con todos los registros. |
|<kbd>Ctrl</kbd>+<kbd>Entrar</kbd>|Cambiar el enfoque del panel de filtros a la lista.|

## <a name="keyboard-shortcuts-in-cards-and-documents"></a>Métodos abreviados de teclado en fichas y documentos

Los siguientes métodos abreviados están disponibles en las páginas de ficha, como **Ficha cliente**, y en las páginas de documento, como **Pedido de venta**, para visualizar y modificar registros.

|Seleccione estas teclas<br />(en macOS)|Para hacer esto|
|--------------------------------|----------|
|<kbd>Alt</kbd>+<kbd>D</kbd>|Abre las entradas de grupo de dimensiones.|
|<kbd>Alt</kbd>+<kbd>F6</kbd>|Alterna contraer/expandir para la <kbd>ficha</kbd> desplegable o parte de ella (subpágina).|
|<kbd>Alt</kbd>+<kbd>F9</kbd>|Crea un nuevo documento y lo publica.|
|<kbd>Alt</kbd>+<kbd>G</kbd>|Abra la página **Buscar entradas** para buscar entradas relacionadas con el documento registrado. Funciona también en listas.|
|<kbd>Alt</kbd>+<kbd>N</kbd> |Abrir una página para crear un nuevo registro; de la misma manera que se elige la acción **Nueva**. |
|<kbd>Alt</kbd>+<kbd>Mayús</kbd>+<kbd>N</kbd> |Cerrar una página y abrir una nueva para crear un nuevo registro; de la misma manera que se selecciona la acción **Aceptar y nuevo**. |
|<kbd>Alt</kbd>+<kbd>Mayús</kbd>+<kbd>W</kbd> |Abra la ficha o documento actual en una nueva ventana. Para obtener más información, consulte [Multitarea en varias páginas](ui-enter-data.md#multitasking-across-multiple-pages).|
|<kbd>Ctrl</kbd>+<kbd>Entrar</kbd>|Guarde y cierre la página.|
|<kbd>Ctrl</kbd>+<kbd>Flecha arriba</kbd>|Abrir el siguiente registro de una entidad.|
|<kbd>Ctrl</kbd>+<kbd>Flecha arriba</kbd> |Abrir el registro anterior de una entidad.|
|<kbd>Ctrl</kbd>+<kbd>Insertar</kbd> |Insertar una nueva línea en los documentos.|
|<kbd>Ctrl</kbd>+<kbd>Supr</kbd> |Eliminar la línea en documentos, diarios y hojas de trabajo.|
|<kbd>Ctrl</kbd>+<kbd>F7</kbd>|Abra entradas del libro mayor, entradas de registros, entradas de costos, etc.|
|<kbd>Ctrl</kbd>+<kbd>F9</kbd>|Lanzar documento.|
|<kbd>Ctrl</kbd>+<kbd>Mayús</kbd>+<kbd>F12</kbd> |Maximizar la parte de productos de línea en una página de documento Vuelva a seleccionar las teclas para volver a la pantalla normal. Para obtener más información, consulte [Enfoque en los productos de línea](ui-enter-data.md#Focus).|
|<kbd>F6</kbd>|Mueve hasta la <kbd>Ficha</kbd> desplegable o parte (subpágina) siguiente.|
|*<kbd>F7</kbd>*|Abrir estadísticas.|
|*<kbd>F9</kbd>*|Publicar, emitir, registrar o anular el documento.|
|*<kbd>Mayús</kbd>+<kbd>Ctrl</kbd>+<kbd>F9</kbd>*|Publique, imprima y guarde el recibo de almacén.|
|<kbd>Mayús</kbd>+<kbd>F6</kbd>|Mueve hasta la <kbd>ficha</kbd> desplegable o parte (subpágina) anterior.|
|*<kbd>Mayús</kbd>+<kbd>F9</kbd>*|Publica e imprime un documento.|

## <a name="quick-entry-shortcuts-for-fields"></a><a name="QuickEntry"></a>Métodos abreviados de entrada rápida para campos

Los siguientes accesos directos pertenecen a la función de entrada rápida en fichas, documentos y páginas de listas. En las listas, los métodos abreviados no se pueden utilizar cuando la lista está en la vista de mosaico. Para obtener más información sobre la entrada rápida, consulte [Aceleración de la entrada de datos mediante la entrada rápida](ui-enter-data.md#QuickEntry).

|Seleccione estas teclas<br />(en macOS)|Para hacer esto|Comentarios|
|--------------------------------|----------|-------|
|<kbd>Introduzca</kbd>|Confirmar el valor en el campo actual y pasar al siguiente campo de entrada rápida.||
|<kbd>Mayús</kbd>+<kbd>Entrar</kbd>|Confirmar el valor en el campo actual y pasar al campo de entrada rápida anterior.||
|<kbd>Ctrl</kbd>+<kbd>Mayús</kbd>+<kbd>Entrar</kbd>|Confirmar el valor en la columna actual y pasar al siguiente campo de entrada rápida fuera de la lista.<br /><br />Este método abreviado se aplica a las listas insertadas en una página, como los productos de lista de un pedido de venta. Le permite salir rápidamente de la lista y continuar introduciendo datos en otros campos de la página.|

## <a name="keyboard-shortcuts-in-the-calendar-date-picker"></a><a name="calendarshortcuts"></a> Métodos abreviados de teclado en el Calendario (selector de fecha)

Al configurar un campo de fecha, puede introducir la fecha manualmente o abrir un calendario (selector de fecha) que le permite seleccionar la fecha que desea. En la tabla siguiente se describen los métodos abreviados de teclado del calendario.

|Seleccione estas teclas<br />(en macOS)|Para hacer esto|
|--------------------------------|----------|
|<kbd>Ctrl</kbd>+<kbd>Inicio</kbd>|Abrir el calendario si está cerrado. **Nota**: Esto no funciona si el campo de fecha está en una cuadrícula, donde <kbd>Ctrl</kbd>+<kbd>Inicio</kbd> salta a la primera fila.|
|<kbd>Ctrl</kbd>+<kbd>Inicio</kbd><br /><br />(<kbd>Cmd</kbd>+<kbd>Inicio</kbd>)|Desplazarse al mes actual, día actual.|
|<kbd>Ctrl</kbd>+<kbd>Flecha izquierda</kbd><br /><br />(<kbd>Cmd</kbd>+<kbd>Flecha izquierda</kbd>)|Desplazarse al día anterior.|
|<kbd>Ctrl</kbd>+<kbd>Flecha derecha</kbd><br /><br />(<kbd>Cmd</kbd>+<kbd>Flecha derecha</kbd>)|Desplazarse al día siguiente.|
|<kbd>Ctrl</kbd>+<kbd>Flecha arriba</kbd><br /><br />(<kbd>Cmd</kbd>+<kbd>Flecha arriba</kbd>)|Desplazarse a la semana anterior, el mismo día de la semana.|
|<kbd>Ctrl</kbd>+<kbd>Flecha arriba</kbd><br /><br />(<kbd>Cmd</kbd>+<kbd>Flecha arriba</kbd>)|Desplazarse a la semana siguiente, el mismo día de la semana.|
|<kbd>Introduzca</kbd>|Seleccionar la fecha enfocada.|
|<kbd>Ctrl</kbd>+<kbd>Fin</kbd><br /><br />(<kbd>Cmd</kbd>+<kbd>Fin</kbd>)|Cierre el calendario y elimine la fecha actual.|
|<kbd>Esc</kbd>|Cierre el calendario sin una selección, mantenga la fecha actual.|
|<kbd>Av. Pág.</kbd>|Desplazarse al mes siguiente.|
|<kbd>Re. pág.</kbd>|Desplazarse al mes anterior.|  

## <a name="keyboard-shortcuts-in-date-fields"></a>Métodos abreviados de teclado en campos de fecha

|Seleccione estas teclas<br />(en macOS)|Para hacer esto|
|--------------------------------|----------|
|<kbd>h</kbd>|Introduzca la fecha actual. "H" significa "hoy".|
|<kbd>t</kbd>|Introduzca la fecha de trabajo. Para obtener más información, consulte [Fecha de trabajo](ui-change-basic-settings.md#work-date).|

## <a name="keyboard-shortcuts-in-the-report-preview"></a><a name="reportpreviewshortcuts"></a>Métodos abreviados de teclado en la vista preliminar de informe

|Seleccione estas teclas<br />(en macOS)|Para hacer esto|
|--------------------------------|----------|
|<kbd>Flecha hacia arriba</kbd>|Desplazarse hacia abajo por la página.|  
|<kbd>Flecha hacia arriba</kbd>|Desplazarse hacia arriba por la página.|
|<kbd>Ctrl</kbd>+<kbd>0</kbd> (cero)<br /><br />(<kbd>Cmd</kbd>+<kbd>0</kbd>)|Ajusta toda la página a la página. |
|<kbd>Ctrl</kbd>+<kbd>Inicio</kbd><br /><br />(<kbd>Cmd</kbd>+<kbd>Inicio</kbd>)|Ir a la primera página del informe.|
|<kbd>Ctrl</kbd>+<kbd>Fin</kbd><br /><br />(<kbd>Cmd</kbd>+<kbd>Inicio</kbd>)|Ir a la última página del informe.|
|<kbd><kbd>Flecha izquierda</kbd></kbd>|Desplazarse a la izquierda cuando la página se acerca de modo que no está totalmente en la vista. |
|<kbd>Flecha hacia la derecha</kbd>|Desplazarse a la derecha cuando la página se acerca de modo que no está totalmente en la vista. |
|<kbd>Av. Pág.</kbd><br /><br />(<kbd>Fn</kbd>+<kbd>flecha arriba</kbd>)|Ir a la página siguiente del informe.|
|<kbd>Re. pág.</kbd><br /><br />(<kbd>Fn</kbd>+<kbd>flecha arriba</kbd>)|Ir a la página anterior del informe.|

## <a name="keyboard-shortcuts-for-zooming-in-and-out"></a><a name="zoomshortcuts"></a>Atajos de teclado para acercar y alejar

|Seleccione estas teclas|Para hacer esto|
|--------------------------------|----------|
|<kbd>Ctrl</kbd>+<kbd>+</kbd>|Ampliar la página actual.|  
|<kbd>Ctrl</kbd>+<kbd>-</kbd>|Alejar la página actual.|  
|<kbd>Ctrl</kbd>+<kbd>0</kbd>|Acercar o alejar al 100 % la página actual.|  

## <a name="keyboard-shortcuts-for-role-explorer"></a><a name="roleexplorer"></a>Atajos de teclado para el Explorador de roles

El Explorador de roles le brinda una descripción general y acceso rápido a todas las características comerciales que están disponibles para su rol. Para obtener más información, vea [Búsqueda de páginas con el explorador de roles](ui-role-explorer.md).

|Seleccione estas teclas<br />(en macOS)|Para hacer esto|
|--------------------------------|----------|
|<kbd>Mayús</kbd>+<kbd>F12</kbd>|Abra el explorador de roles.|
|<kbd>F3</kbd>|Abra el cuadro **Buscar** en el explorador de roles para encontrar características basadas en una palabra o término de búsqueda determinado.|
|<kbd>F3</kbd> o <kbd>Ctrl</kbd>+<kbd>Flecha arriba</kbd>|Mueve el foco a la siguiente característica encontrada en el explorador de roles. <kbd>F3</kbd> moverá el foco al cuadro **Buscar** después de la última característica encontrada.|
|<kbd>Mayús</kbd> <kbd>F3</kbd> o <kbd>Ctrl</kbd>+<kbd>Flecha arriba</kbd>|Mueve el foco a la anterior característica encontrada en el explorador de roles.|
|<kbd>Ctrl</kbd>+<kbd>Mayús</kbd>|Expanda o contraiga todos los subnodos, además de los nodos de nivel superior, cuando elija la acción **Expandir** o **Contraer**.|

## <a name="numeric-keypad-shortcuts"></a><a name="keypad"></a> Accesos directos del teclado numérico

En la tabla siguiente se describen los métodos abreviados en un teclado numérico.

|Seleccione estas teclas<br />(en macOS)|Para hacer esto|
|--------------------------------|----------|
|<kbd>Alt</kbd>+<kbd>Separador decimal</kbd>|Cambie la salida de la tecla de separador decimal a un punto (.) o al carácter determinado por la opción **Región** de la página **Mi configuración**. Para más información, consulte [Configurar el separador decimal utilizado por los teclados numéricos](ui-enter-data.md#decimal).|


## <a name="access-keys-for-action-bar-and-navigation-menu"></a>Teclas de acceso para la barra de acciónes y el menú de navegación

Las teclas de acceso son métodos abreviados de teclado que seleccionan acciones específicas en la barra de acciones y el menú de navegación, lo que le permite navegar a través de las acciones para llegar a la página que se desea. Las claves de acceso están disponibles en el cliente web de Business Central y son similares a las claves de acceso en Excel y Word Online.  

Para usar las teclas de acceso en una página, primero seleccione la tecla <kbd>Alt</kbd> para mostrar *sugerencias de teclas*, que son letras en pequeños recuadros junto a las acciones de la barra de acciones y el menú de navegación. 

![Imagen que muestra claves de acceso en la página de lista de clientes.](media/access-keys.png) 

Para seleccionar una acción, seleccione la combinación de teclas que se muestra en la sugerencia de teclas, por ejemplo <kbd>H</kbd> o <kbd>J</kbd>+<kbd>F</kbd>.
- Si la acción abre un submenú de otras acciones, se muestran las sugerencias de teclas para el submenú, lo que le permite continuar usando las teclas de acceso si lo desea.
- Si la acción abre una página diferente, las sugerencias clave se desactivan. Para volver a mostrarlos, seleccione la tecla <kbd>Alt</kbd>. 
 
## <a name="see-also"></a>Consulte también .

[Referencia rápida de teclado: solo PC](keyboard-shortcuts-cheatsheet.md)  
[Características de asistencia](ui-accessibility.md)  
[Preparación para hacer negocios](ui-get-ready-business.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Preguntas más frecuentes](across-faq.yml)  
[Buscar movimientos](ui-find-entries.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
