---
title: Introducir datos en Business Central
description: 'Hay muchas características generales que le ayudan a introducir datos de forma más fácil, rápida y precisa. Los principios básicos y las funciones avanzadas se describen aquí.'
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'decimal separator, data entry, focus'
ms.search.form: '9020, 9022, 9026, 9027, 9030, 9000, 9009, 9004, 9005, 9024, 9006, 9007, 9010, 9016, 9017'
ms.date: 03/23/2022
ms.author: jswymer
---
# Introducción de datos

Hay muchas características generales que le ayudan a introducir datos de forma más fácil, rápida y precisa. Los principios básicos y las características avanzadas para la introducción de datos se describen en este artículo.  

[!INCLUDE [about-ui-learn](includes/about-ui-learn.md)]

Los ejemplos de este producto utilizan los datos de demostración.

## Trabajar con campos editables

Los campos en [!INCLUDE[prod_short](includes/prod_short.md)] puede contener diferentes datos editables, como texto o importe de divisas. Los campos editables suelen mostrar un cuadro de entrada donde puede escribir o elegir un valor. Los campos no editables generalmente se muestran con un fondo gris.   

Algunos campos editables proporcionan un selector para ayudarle a especificar un valor.  

<!-- TODO: Add illustrations or images of each picker -->
|**Encargado de picking**        |**Cómo le ayuda a especificar un valor**|
|------------------|------------------------------------|
|Selector de fechas       |Este selector muestra un calendario basado en su configuración regional actual. Le ayuda a elegir una única fecha.|
|Desplegable          |Los menús desplegables ofrecen una opción de valores fijos o registros de referencia de otra tabla|
|Conmutador o casilla|Algunos campos ofrecen una elección sencilla de valores *Sí* o *No*. El conmutador se usa para especificar este valor y siempre se muestra como una casilla en listas|
|Edición de asistencia       |Algunos campos proporcionan selectores personalizados adecuados para buscar y elegir el mejor valor para ese campo, como la ventana emergente.|

### Modificar un valor de campo

Para modificar el valor de un campo, primero debe establecer el foco en ese campo. El foco se establece mediante las siguientes acciones:

- Usando la tecla <kbd>Tab</kbd>. La acción selecciona todo el valor.
- Haciendo clic con el botón izquierdo del ratón o dispositivo de entrada similar. Esta acción solo seleccionará el valor del campo completo si el campo está en una lista.  

Cuando interactúa con campos en la interfaz de usuario, [!INCLUDE[prod_short](includes/prod_short.md)] normalmente favorece la selección de todo el valor del campo para que le sea más fácil reemplazar ese valor.

Cuando se selecciona todo el valor del campo:
- Reemplace el valor simplemente escribiendo para especificar un nuevo valor. Si el campo ofrece un selector, puede activarlo utilizando el atajo del teclado <kbd>Alt</kbd>+<kbd>Flecha abajo</kbd>.
- Utilice la tecla <kbd>Supr</kbd> o <kbd>Retroceso</kbd> para borrar el valor.

seleccione la tecla <kbd>F2</kbd> para alternar entre seleccionar todo el valor del campo o situar el cursor tras el valor del campo. Al colocar el cursor al final del valor se facilita la anexión al valor existente.

Cuando el cursor se muestra al final del valor del campo:
- Agregue al valor escribiendo.
- Use las teclas <kbd>Inicio</kbd>, <kbd>Fin</kbd>, <kbd>Flecha izquierda</kbd> y <kbd>Flecha derecha</kbd> para mover el cursor dentro del valor. Si está editando un campo en una lista, seleccione la tecla <kbd>Flecha izquierda</kbd> nuevamente cuando el cursor esté al comienzo del valor establecerá el foco en el campo anterior. Del mismo modo, al seleccionar la tecla <kbd>Flecha derecha</kbd> nuevamente cuando el cursor esté al final del valor establecerá el foco en el siguiente campo.

> [!NOTE]
> Después de especificar un valor, Business Central solo comprobará que sea válido después de hacer clic fuera del campo o establecer el foco en otro elemento, como el siguiente campo.  

[!INCLUDE [background_doc_journal_check](includes/background_doc_journal_check.md)]

## Métodos abreviados de teclado

Existen varios métodos abreviados de teclado que le permiten trabajar "sin ratón" y acelerar la entrada de datos. Estos métodos abreviados de teclado son especialmente útiles con entradas a gran escala y tareas de escritura repetitivas.

Para obtener más información sobre estos métodos abreviados, consulte [Métodos abreviados de teclado](keyboard-shortcuts.md). Algunos de los métodos del teclado abreviados se explican en este artículo.

## <a name="QuickEntry"></a>Acelerar la entrada de datos con la entrada rápida

La entrada rápida es una característica diseñada para la entrada de datos cuando se utiliza el teclado. La entrada rápida funciona en campos (como en las páginas de fichas) y en listas (filas y columnas). Es beneficioso cuando se realizan tareas de mecanografía repetitivas que requieren la creación de múltiples registros en secuencia. Los ejemplos incluyen un lote de pedidos de ventas o el registro de nuevos artículos.

Puede usar tecla Tab para navegar desde un campo de una página al siguiente campo editable. Una desventaja de usar Tab es que siempre va secuencialmente al siguiente campo. <!-- even if the field is non-editable or seldom filled it in.-->La entrada rápida le permite cambiar esta ruta. Con la entrada rápida, use la tecla <kbd>Entrar</kbd> para navegar solo por los campos en los que está interesado. La entrada rápida omite los campos no editables y los campos que normalmente no completa. Es posible que ya haya observado este comportamiento en algunas páginas. Este comportamiento se debe a que los campos que se deben incluir al presionar Entrar y los que se deben omitir han sido predeterminados. Puede personalizar la entrada rápida si personaliza su espacio de trabajo y optimiza la forma en que introduce los datos en cada página.

### Cómo funciona la entrada rápida

Cada campo puede marcarse como *incluido en la entrada rápida* o como *excluido de la entrada rápida*. Los campos que se incluyen en la Entrada rápida se incluirán en la ruta cuando seleccione <kbd>Entrar</kbd>. Los campos que están excluidos de la Entrada rápida no lo harán.

Cuando haya finalizado de rellenar un campo, seleccione <kbd>Entrar</kbd> para confirmar los cambios e ir al siguiente campo. Si desea invertir la dirección y pasar al campo anterior, seleccione <kbd>Shift</kbd>+<kbd>Entrar</kbd>. Para obtener más información sobre estos métodos abreviados, consulte [Métodos abreviados de entrada rápida para campos](keyboard-shortcuts.md#QuickEntry).

#### Sugerencias y trucos

La lista siguiente ofrece información útil sobre el uso de la entrada rápida.

- Está disponible para cualquier campo editable.
- También funciona en columnas y filas.
- No impide el acceso a otros elementos de una página, como las acciones. Se puede seguir accediendo a estos elementos mediante <kbd>Tabulación</kbd> y <kbd>Mayúscula</kbd>+<kbd>Tabulación</kbd>.  
- No es necesario que se expandan las fichas desplegables para que funcione la Entrada rápida. Si el siguiente campo de entrada rápida se encuentra en una ficha desplegable contraída, esa ficha desplegable se expandirá automáticamente y el foco estará en el campo elegido. [!INCLUDE[prod_short](includes/prod_short.md)] recordará que la ficha desplegable debe ampliarse la próxima vez que visite la página.  
- La entrada rápida funciona independientemente de si los campos son obligatorios. Por lo tanto, es buena idea asegurarse de que los campos obligatorios se incluyan en la entrada rápida.
- De forma predeterminada, la mayoría de los campos se incluyen automáticamente en la entrada rápida. Por lo tanto, al principio, lo más probable es que su tarea sea excluir campos de la entrada rápida.

### Para cambiar los campos de entrada rápida

Para configurar la Entrada rápida en campos, utilice la personalización.

1. Inicie la personalización seleccionando el icono ![Configuración.](media/ui-experience/settings_icon_small.png "Icono de configuración para el área de trabajo") , y luego la acción **Personalizar**.
2. Seleccione el campo que desea cambiar. En listas, seleccione el encabezado de columna correspondiente. Luego, elija **Incluir en Entrada rápida** o **Excluir de Entrada rápida**.

Para obtener más información sobre la personalización, consulte [Personalizar el área de trabajo](ui-personalization-user.md).

## Campos obligatorios

Cuando se introducen datos en páginas, determinados campos aparecen marcados con un asterisco de color rojo. El asterisco rojo significa que el campo debe completarse para completar un determinado proceso. Un ejemplo es cuando publica una transacción que usa el valor en el campo.  

Aunque el campo es obligatorio, no se le obliga a rellenar el campo para ir a otros campos o cerrar la página. El asterisco rojo solo sirve como recordatorio de que se le bloqueará y no podrá terminar un determinado proceso.  

## Buscar datos al escribir

 Cuando comience a escribir caracteres en un campo, aparecerá una lista desplegable que muestra los posibles valores de campo. Esta lista cambia a medida que escriba caracteres adicionales y puede seleccionar el valor correcto cuando aparezca.  

 Muchos campos tienen un botón de flecha hacia abajo que puede elegir. Seleccione la flecha para desplegar una lista de datos que están disponibles para su introducción en el campo. El botón tiene dos funciones, según el tipo de campo:  

- Búsqueda: muestra información de otra tabla, que puede introducir en el campo. Puede seleccionar un elemento de datos a la vez.  

- Desplegable: muestra el conjunto de opciones que existe para el campo. Sólo puede seleccionar una de las opciones.  

## Preguntas frecuentes sobre copiar y pegar campos y líneas

Puede copiar una o más filas de una lista o un solo campo de una página. Luego pegue lo que copió en la misma página, en otra página o en un documento externo. Podría, por ejemplo, pegarlo en Microsoft Excel o en correo electrónico de Outlook. En resumen, para copiar, seleccione <kbd>Ctrl</kbd>+<kbd>C</kbd> (cmd+C in macOS) en su teclado. Para pegar, seleccione <kbd>Ctrl</kbd>+<kbd>V</kbd> o <kbd>cmd+V</kbd> en macOS.

En una lista, para copiar el campo en la misma columna de la fila anterior y pegarlo en la fila actual, seleccione <kbd>F8</kbd>.

Para obtener más información, consulte [Preguntas frecuentes sobre copiar y pegar](faq-copy-paste.yml).

## Filtrado de los productos de línea

Para empezar a filtrar, seleccione ![Icono del panel de filtrado](media/open-filter-pane-icon.png "Icono Panel de filtro") en la parte superior de la lista o seleccione <kbd>Mayúscula</kbd>+<kbd>F3</kbd> para abrir el panel de filtrado. Con el panel de filtros se trabaja como en cualquier otra lista. Para obtener más información, consulte [Filtrado](ui-enter-criteria-filters.md#filtering).

El filtrado es especialmente útil cuando se ven y analizan documentos más largos. Imagine que abre un histórico de facturas de venta. Luego, filtre los artículos de líneas para mostrar todos los artículos de líneas que tienen un descuento individual superior al 5 %. O bien, filtre para mostrar solo accesorios de bicicleta con 'pro' en el nombre.

## <a name="Focus"></a>Enfoque en los productos de línea

Al trabajar en documentos que incluyen una parte de artículos de línea, puede cambiar la vista para centrarse solo en los artículos de línea. Los documentos de ejemplo son pedidos de ventas o páginas de facturas. La parte de artículos de línea se amplía para que ocupe casi todo el espacio de trabajo. Oculta otras partes de la página, excepto el área de acciones de la parte superior. Este diseño le proporciona una mejor visión general de los productos de línea y más espacio para trabajar en ellos.

Se beneficiará especialmente cuando trabaje con grandes listas de artículos de línea y desee escribir datos rápidamente. Esta característica también proporciona capacidad de filtrado avanzado. Al igual que en otras listas, navegar y buscar en las líneas de pedido se vuelve aún más fácil.

### Activar y desactivar el enfoque

Para centrarse en productos de línea, seleccione cualquier lugar de la parte de producto de línea y, a continuación, seleccione el ![icono Modo de enfoque.](media/focus-mode.png "Icono Modo de enfoque") en la esquina superior derecha, o seleccione <kbd>Ctrl</kbd>+<kbd>Mayúscula</kbd>+<kbd>F12</kbd>.

Para volver a la vista normal, elija el ![icono Modo de enfoque.](media/focus-mode.png "Icono Modo de enfoque") o seleccione <kbd>Ctrl</kbd>+<kbd>Mayúscula</kbd>+<kbd>F12</kbd> nuevamente.

## Multitarea en varias páginas

Puede abrir una página de ficha o documento en una nueva ventana. Abrir una nueva ventana le permite:

- Trabajar en varias tareas al mismo tiempo
- Administre interrupciones en la tarea actual, como atender una llamada entrante.
- Mantener una ventana abierta para una tarea en curso mientras inicia o completa otra tarea en ventanas.

Para abrir la tarjeta o documento actual en una nueva ventana, elija ![Abrir nueva ventana.](media/open-new-window-icon.png "Icono Abrir en una nueva ventana") en la esquina superior derecha, o seleccione <kbd>Alt</kbd>+<kbd>Mayúscula</kbd>+<kbd>W</kbd>.

<!--
When working on multiple tasks at a time or when managing interruptions to the current task, such as taking an incoming call, you can open a card or document page in a new window. This allows you to keep a window open for an ongoing task while you start or complete another task in one or more other windows.
-->

> [!NOTE]
> Cuando abre otras páginas desde una ficha o documento que está abierto en una nueva ventana, esas páginas se abrirán en una nueva ventana aunque no elija ![Abrir nueva ventana.](media/open-new-window-icon.png "Icono Abrir en una nueva ventana").

> [!NOTE]
> Si trabaja en el explorador Safari, un bloqueador de ventanas emergentes puede provocar que no se abra la nueva ventana. Si este es el caso, especifique la URL del producto como un sitio web permitido. Para obtener información, consulte [Cambiar las preferencias en Safari](https://go.microsoft.com/fwlink/?LinkId=2102965).<br /><br />
> Lo mismo puede suceder en otros navegadores, como Firefox. Para obtener más información, consulte [Configuración del bloqueador de elementos emergentes en Firefox](https://go.microsoft.com/fwlink/?LinkId=2116400).  

Otra forma de realizar múltiples tareas es abrir [!INCLUDE[prod_short](includes/prod_short.md)] en dos o más pestañas del navegador. Cuando lo haga de esta forma, debe crear una nueva pestaña y luego copiar/pegar la URL de la pestaña original en la nueva pestaña. De esta forma se crea una nueva sesión.   

> [!NOTE]
> No use la función **Duplicar** del navegador para crear la nueva pestaña, ya que esto puede hacer que las acciones de una pestaña bloqueen las acciones de otras pestañas porque son parte de la misma sesión.

## Introducir cantidades por cálculo

Al introducir números en campos de cantidad, como el campo **Cantidad** de una línea de diario de producto, puede introducir la fórmula en lugar de la cantidad de la suma.  

### Ejemplos  

- Si introduce 19+19, el campo se calcula para obtener el valor 38.  

- Si introduce 41-9, el campo se calcula para obtener el valor 32.  

- Si introduce 12*4, el campo se calcula para obtener el valor 48.  

- Si introduce 12/4, el campo se calcula para obtener el valor 3.  

## Especificación de números negativos

Puede especificar números negativos de dos formas. El número -20,5 se puede especificar como:  

- -20,5  

  O
- 20,5-  

En ambos casos, el importe se registrará como -20,5.  

Si el último carácter de la expresión es **+** o **-**, la expresión completa se registrará con ese signo. Ejemplo, **10-20+** dará como resultado 10 y no -10.  

## Introducir fechas y horas

Puede especificar fechas y horas en todos los campos diseñados para las fechas (campos de fecha). Las fechas pueden escribirse con o sin separadores.

> [!NOTE]  
> La forma de especificar las fechas y horas depende de los valores **Región**. Para obtener más información, consulte [Cambiar configuración básica](ui-change-basic-settings.md).  

### Introducción de fechas

Puede utilizar el selector de fechas para seleccionar una fecha de un calendario o puede introducir fechas manualmente. Esta sección proporciona un breve resumen de cómo introducir fechas. Para obtener más información, consulte [Trabajar con fechas y horas del calendario](ui-enter-date-ranges.md).

Para la entrada de fecha manual, puede introducir dos, cuatro, seis u ocho dígitos:  

- Dos dígitos se interpretan como el día. Agregará el mes y el año de la fecha de trabajo.  

- Cuatro dígitos se interpretan como el día y el mes. Agregará el año de la fecha de trabajo.  

- Si la fecha que desea está en el rango del 01/01/1950 al 31/12/2049, introduzca el año con dos dígitos. De lo contrario, introduzca el año con cuatro dígitos.

  > [!NOTE]
  > Si está usando [!INCLUDE[prod_short](includes/prod_short.md)] en las instalaciones, el intervalo de años de dos dígitos puede ser diferente. Los administradores pueden cambiar el rango modificando el ajuste **CalendarTwoDigitYearMax** del servidor [!INCLUDE[prod_short](includes/prod_short.md)]. Para obtener más información, consulte [Configuración de Business Central Server](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#General).

También puede introducir una fecha como día de la semana seguido de un número de semana. O bien, puede introducir un año. Por ejemplo, Lun25 o lun25 significa lunes de la semana 25.  

En lugar de introducir una fecha específica, puede introducir uno de estos códigos.  

|Code|Resultado|  
|--------------|----------------|  
|h|Especifica la fecha de hoy (la fecha de sistema del equipo).|  
|p|Especifica un "período contable, donde p significa el primer período contable, p2 significa el segundo período contable, y así sucesivamente. |
|t|Especifica la fecha de trabajo que está configurada en la aplicación. Para cambiar la fecha de trabajo, vea [Cambiar la configuración básica](ui-change-basic-settings.md). Una fecha de trabajo se puede usar si hay muchas operaciones con una fecha distinta a la activa.|
|c|Especifica que la fecha después de c es una fecha de cierre, por ejemplo, C123101.|  

## Introducción de horas

Cuando introduzca horas, puede insertar cualquier signo separador entre las unidades, aunque no es necesario. No necesita escribir minutos, segundos ni AM/PM.  

En la tabla siguiente se muestran varias formas de introducir horas y cómo se interpretan.  

|Movimiento|Interpretación|  
|---------------|------------------------|  
|5|05:00:00|  
|5:30|05:30:00|  
|0530|05:30:00|  
|5:30:5|05:30:05|  
|053005|05:30:05|  
|5:30:5.50|05:30:05,5|  
|053005050|05:30:05.05|  

 Introduzca dos dígitos para cada unidad de tiempo si no escribe ningún separador.  

## Introducir fechas/horas combinadas

[!INCLUDE [datetimes](includes/datetimes.md)]

## Introducción de duración

Introduzca un periodo de tiempo como un número seguido de su unidad de medida.  

A continuación se muestran algunos ejemplos.  

|Duración|Unidad de medida**|  
|------------------|-------------------------|  
|2h|2 h|  
|6 h 30 m|6 h 30 m|  
|6,5h|6 h 30 m|  
|90m|1 h 30 m|  
|2d 6h 30m|2 días 6 hrs 30 mins|  
|2d 6h 30m 56s 600ms|2 días 6 h 30 m 56 s 600 ms|  

 También puede introducir un número y se convertirá automáticamente en un periodo de tiempo. El número que introduzca se convierte según la unidad de medida predeterminada que se ha especificado en el campo Duración.  

 Para ver la unidad de medida usada en el campo Duración, introduzca un número y observe a qué unidad de medida se convierte.  

 El número 5 se convierte a 5 hrs, si la unidad de medida es horas.  

## <a name="decimal"></a>Configurar el separador decimal utilizado por los teclados numéricos

Cuando utilice la tecla <kbd>Separador decimal</kbd> en un teclado numérico para introducir datos, el separador decimal real que se introduce en el campo viene determinado por su configuración regional en Business Central. La mayoría de las regiones usan el punto (.) o la coma (,) como separador para los valores decimales, como se suele ver en las cantidades de moneda. La tecla decimal de su teclado se adapta a su región. Suele ser diferente a las teclas de punto o coma del resto del teclado. Establezca la región en Business Central en la página **Mi configuración**.

Por ejemplo, suponga que está utilizando un teclado numérico que utiliza un punto (.) como tecla de <kbd>separación decimal</kbd>. Pero está introduciendo datos para un idioma regional que usa una coma (**,**) para el separador decimal, como francés (Francia). Por lo tanto, desea que los decimales como "1.23" se introduzcan como "1,23". En este caso, puede ir a la página **Mi configuración** y configurar la **Región** al idioma regional de destino, como **Francés (Francia)**. Para obtener más información, consulte [Cambiar configuración básica](ui-change-basic-settings.md#region).

> [!TIP]
> Puede haber ocasiones en las que quiera usar el separador decimal para introducir un punto (.). Por ejemplo, suponga que estaba introduciendo un rango de fechas en un filtro, como `01/01/2022..04/01/2022`, o cualquier cosa que requiera un punto. Para adaptarse a este caso, seleccione las teclas <kbd>Alt</kbd>+<kbd>Separador decimal</kbd> en el teclado numérico. Esta combinación de teclas cambia el separador decimal entre la salida de un punto y el separador decimal determinado por el ajuste **Región**.

## Consulte también .

[Ordenar, buscar y filtrar listas](ui-enter-criteria-filters.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
