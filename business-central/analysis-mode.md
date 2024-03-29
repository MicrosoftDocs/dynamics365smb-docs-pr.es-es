---
title: Analizar datos en páginas de lista y consultas usando el modo de análisis de datos
description: Aprenda a usar el modo de análisis de datos en Business Central para analizar datos.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.date: 12/08/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
ms.search.form: '456, 457, 458, 459, 460, 461, 16, 22, 25, 26, 27, 31, 143, 144, 9300, 9301, 9303, 9304, 9305, 9306, 9307, 9309, 9310, 9311'
---
# <a name="analyze-list-page-and-query-data-using-data-analysis-mode"></a>Analizar página de lista y datos de consulta usando el modo de análisis de datos

> **SE APLICA A:** Vista previa pública en el primer lanzamiento de versiones de Business Central 2023 y posteriores para analizar páginas de lista; Generalmente disponible en el segundo lanzamiento de versiones de Business Central 2023 para analizar datos de páginas de listas y consultas.

En este artículo, aprenderá a analizar datos de páginas en listas y consultas mediante el *modo de análisis de datos*. El modo de análisis de datos le permite analizar datos directamente desde la página, sin tener que ejecutar un informe o cambiar a otra aplicación, como Excel. Proporciona una forma interactiva y versátil de calcular, resumir y examinar datos. En lugar de ejecutar informes con diferentes opciones y filtros, puede agregar varias pestañas que representen diferentes tareas o vistas de los datos. Los ejemplos podrían ser "Mis clientes", "Elementos de seguimiento", "Proveedores agregados recientemente", "Estadísticas de ventas" o cualquier otra vista que pueda imaginar.

> [!TIP]
> Lo bueno del modo de análisis de datos es que no cambia ninguno de los datos subyacentes de la página de lista o consulta ni el diseño de la página o consulta cuando no está en modo de análisis de datos. Entonces, la mejor manera de aprender qué puede hacer en el modo de análisis de datos es probar cosas.

## <a name="prerequisites"></a>Requisitos previos

- Si está utilizando Business Central versión 22, el modo de análisis de datos está en versión preliminar. Por lo tanto, un administrador debe habilitarlo antes de poder utilizarlo. Para habilitarlo, vaya a la página **Administración de características** y active la **Actualización de funciones: modo de análisis, analice rápidamente los datos directamente en Business Central**. [Más información acerca de la Administración de características](/dynamics365/business-central/dev-itpro/administration/feature-management).
- En la versión 23 y posteriores, a su cuenta se le debe asignar el conjunto de permisos **ANÁLISIS DE DATOS - EXEC** o incluir permiso de ejecución en el objeto del sistema **9640 Permitir datos Modo de análisis**. Como administrador, puede excluir estos permisos a los usuarios que no desea que tengan acceso al modo de análisis.

> [!NOTE]
> Es posible que observe algunas páginas de lista que no incluyen el interruptor **Analizar** para cambiar al modo de análisis. La razón es que los desarrolladores pueden desactivar el modo de análisis en páginas específicas utilizando la propiedad  [AnalysisModeEnabled](/dynamics365/business-central/dev-itpro/developer/properties/devenv-analysismodeenabled-property) en AL.

## <a name="get-started"></a>Comenzar

1. Abra la página de lista o consulta.

   Por ejemplo, para trabajar con la página **Asientos de libro mayor de clientes**, seleccione el icono de la característica ![Lupa que abre la función Dígame.](media/ui-search/search_small.png) (<kbd>Alt</kbd>+<kbd>Q</kbd>), escriba *Movimientos de contabilidad de clientes* y luego elija el vínculo relacionado. 

2. En la barra de acciones de la parte superior de la página, active el interruptor **Analizar**.

    El modo de análisis de datos abre los datos en una experiencia optimizada para el análisis de datos.  En el modo de análisis de datos, la barra de acción normal se reemplaza con una barra de modo de análisis de datos especial. La siguiente figura ilustra las diferentes áreas de una página en el modo de análisis de datos.

   [![Muestra una descripción general de una página en el modo de análisis de datos](media/analysis-mode-overview-2.png)](media/analysis-mode-overview-2.png#lightbox)

   Cada área se explica en las secciones siguientes.

3. Utilice las diferentes áreas para manipular, resumir y analizar datos. Vea las secciones siguientes para obtener detalles.

4. Cuando desee salir del modo de análisis, desactive el conmutador **Analizar**.

   Las pestañas de análisis que ha agregado permanecerán hasta que las elimine. Entonces, si regresa al modo de análisis de datos nuevamente, las verá exactamente como las dejó.

> [!NOTE]
> Los datos que se muestran en el modo de análisis están controlados por los filtros o vistas establecidos en la página de lista. Esto le permite filtrar previamente los datos antes de entrar al modo de análisis.

## <a name="work-with-data-analysis-mode"></a>Trabajar con el modo de análisis de datos

En el modo de análisis de datos, la página se divide en dos áreas:

- El área principal, que consta del área de datos (1), la barra de resumen (2) y la barra de pestañas (5)
- El área de manipulación de datos, que consta de dos paneles: columnas (3) y filtros de análisis (4).

### <a name="data-area-1"></a>Área de datos (1)

El área de datos es donde se muestran las filas y columnas de la página de consulta de lista y se resumen los datos. El área de datos proporciona una forma versátil de controlar el diseño de las columnas y una forma rápida de obtener un resumen de los datos. Para las columnas que contienen valores numéricos, la suma de todos los valores de la columna se muestra en la última fila, a menos que haya definido grupos de filas. En este caso, las sumas aparecen como subtotal para los grupos.  

![Muestra una descripción general del área de datos en una página en el modo de análisis de datos](media/analysis-mode-data-area.png)

- Para mover una columna, selecciónela y arrástrela hasta donde tenga más sentido en su análisis.
- Para ordenar por una columna, seleccione el encabezado de la columna. Para ordenar en varias columnas, seleccione y mantenga presionada la tecla <kbd>Shift</kbd> mientras selecciona los encabezados de columna que desea ordenar.
- Haga clic con el botón derecho en la columna o coloque el cursor sobre ella y seleccione el icono de menú ![Muestra el icono en una columna en el modo de análisis de datos que abre un menú de acciones](media/analysis-mode-column-menu-icon.png) para acceder a varias acciones que puede realizar en las columnas. Por ejemplo:

  - Para anclar una columna a la izquierda o a la derecha del área de datos para que no se mueva de la pantalla cuando se desplace, seleccione ![Muestra el icono en una columna en el modo de análisis de datos que abre un menú de acciones](media/analysis-mode-column-menu-icon.png) > **Anclar columna** > **Anclar a la izquierda** la parte de la columna.
  - Defina filtros de datos directamente en la definición de columna en lugar de ir a los paneles de **Filtros de análisis**. Todavía puede echar un vistazo a los detalles sobre los datos relacionados y de cada línea, así como abrir la tarjeta para obtener más información sobre una entidad determinada.
- Utilice el área de datos para interactuar con los datos. Para las columnas que contienen valores sumables numéricos, puede obtener estadísticas descriptivas en un conjunto de campos, marcándolos. Las estadísticas aparecen en la barra de estado (2), en la parte inferior de la página.
- Exportar datos en formato Excel o csv. Haga clic con el botón derecho en el área de datos o en una selección de celdas para exportar.

### <a name="summary-bar-2"></a>Barra de resumen (2)

La barra de resumen se encuentra en la parte inferior de la página y muestra estadísticas sobre los datos de la página de lista o consulta. A medida que interactúa con columnas cuyos valores se pueden sumar, como al seleccionar varias filas en una columna que muestra cantidades, los datos se actualizan.

![Muestra una descripción general de una barra de resumen en el modo de análisis de datos](media/analysis-mode-totals-row.png)

La siguiente tabla describe los diferentes números que se muestran en el área de totales:

|Número|Descripción|
|-|-|
|Filas|El número de filas seleccionadas como parte del número total de filas disponibles. |
|Total de filas|El número de filas en la lista sin filtrar o consulta.|
|Filtrado|El número de filas mostradas como resultado de los filtros aplicados a la lista o consulta.|
|Promedio|El valor promedio en todos los campos sumables seleccionados.|
|Total|El número de filas seleccionadas.|
|Mín|El valor mínimo en todos los campos sumables seleccionados.|
|Máx|El valor máximo en todos los campos sumables seleccionados.|
|Suma|La suma total de todos los valores en los campos sumables seleccionados.|

### <a name="columns-3"></a>Columnas (3)

El panel **Columnas** es uno de los dos paneles que trabajan juntos para definir su análisis. La otra zona es el panel **Filtros de análisis**. El panel **Columnas** se utiliza para resumir los datos. Utilice el panel **Columnas** para definir qué columnas deben incluirse en el análisis.

![Muestra una descripción general del panel de columnas en el modo de análisis de datos](media/analysis-mode-columns-2.png)

|Áreas|Descripción|
|-|-|
|Buscar/marcar o borrar todas las casillas|Buscar columnas. Seleccione la casilla para seleccionar/limpiar todas las columnas.|
|Casillas|Esta área incluye una casilla para cada campo en la tabla de origen de la lista o consulta. Utilice esta área para cambiar las columnas que se muestran. Seleccione una casilla para mostrar la columna del campo en la página; limpie la casilla para ocultar la columna. |
|Grupos de filas|Utilice esta área para agrupar y sumar datos por uno o más campos. Solo puede incluir campos no numéricos, como campos de texto, fecha y hora. Los grupos de filas se usan a menudo en modo dinámico.|
|Valores|Utilice esta área para especificar los campos para los que desea una suma total. Solo puede incluir campos que contengan números que se puedan sumar; por ejemplo, no campos de texto, fecha u hora.|

Para mover un campo de un área a otra, seleccione el icono de agarrar ![Muestra una descripción general de una página en el modo de análisis de datos](media/column-grab-icon.png) junto a la columna en la lista y arrástrelo al área de destino. No puede mover un campo a un área donde no está permitido.

### <a name="analysis-filters-4"></a>Filtros de análisis (4)

El panel **Filtros de análisis** le permite establecer más filtros de datos en las columnas para limitar las entradas de la lista. Establezca filtros en las columnas para limitar las entradas en la lista y las sumas posteriores solo a aquellas entradas que le interesen según los criterios que defina. Por ejemplo, suponga que solo le interesan los datos de un cliente específico o los pedidos de ventas que superan un importe específico. Para establecer un filtro, seleccione la columna, elija la operación de comparación de la lista (como **Iguales** o **Comienza por**) y luego introduzca el valor.

![Muestra una descripción general del panel de filtros en el modo de análisis de datos](media/analysis-mode-filters.png)

> [!NOTE]
> Los filtros adicionales solo se aplican a la pestaña de análisis actual. Esto le permite definir exactamente los filtros de datos adicionales que se necesitan para un análisis específico.

### <a name="tabs-5"></a>Pestañas (5)

El área de pestañas de la parte superior le permite crear diferentes configuraciones (columnas y filtros de análisis) en pestañas separadas, donde puede manipular los datos de las pestañas de forma independiente. Siempre hay al menos una pestaña, llamada **Análisis 1**, de forma predeterminada. Agregar más pestañas es beneficioso para guardar configuraciones de análisis de uso frecuente en un conjunto de datos. Por ejemplo, puede tener pestañas para analizar datos en modo dinámico y otras pestañas que filtran a un subconjunto de filas. Algunas pestañas pueden mostrar una vista detallada con muchas columnas y otras solo mostrar algunas columnas clave.

Aquí hay algunos consejos sobre cómo trabajar con varias pestañas de análisis:

- Para agregar una nueva pestaña, seleccione el signo grande **+** junto a la última pestaña de análisis.
- Seleccione la punta de flecha hacia abajo en una pestaña para acceder a una lista de acciones que puede realizar en una pestaña, como cambiar el nombre, duplicar, eliminar y mover.

   - **Eliminar** elimina la pestaña que tiene abierta actualmente. **Eliminar todo** elimina todas las pestañas que ha agregado, excepto la pestaña predeterminada **Análisis 1** .
- No puede eliminar por completo **Análisis 1**, pero puede cambiarle el nombre mediante la acción **Renombrar** y borrar los cambios que ha realizado utilizando **Eliminar** o **Eliminar todo**.  

- Las pestañas de análisis que ha agregado y configurado permanecerán hasta que las elimine. Entonces, si regresa al modo de análisis de datos nuevamente, las verá exactamente como las dejó.

   > [!TIP]
   > Las pestañas que configuras solo son visibles para usted. Otros usuarios solo verán las pestañas que hayan configurado.
- Puede copiar pestañas de análisis. La copia puede ser útil si desea experimentar cambiando una pestaña sin cambiar la original, o si desea crear diferentes variaciones del mismo análisis.


## <a name="date-hierarchies"></a>Jerarquías de fecha

En el modo de análisis, los campos de fecha del conjunto de datos se generan en una jerarquía Año-Trimestre-Mes de tres campos separados. Esta jerarquía se basa en el calendario normal, no en ningún calendario fiscal definido en Business Central.

Los campos adicionales reciben el nombre _\<field name\> Año_, _\<field name\> Trimestre_ y _\<field name\> Mes_. Por ejemplo, si el conjunto de datos incluye un campo llamado _Fecha de publicación_, entonces la jerarquía de fechas correspondiente consta de campos llamados _Año de fecha de publicación_, _Trimestre de fecha de contabilización_, y _Mes de fecha de contabilización_.

> [!NOTE]
> Actualmente, la jerarquía de fechas solo se aplica a los campos de tipo date, no a los campos de tipo de fecha y hora.

## <a name="pivot-mode"></a>Modo dinámico

Puede usar el modo dinámico para analizar una gran cantidad de datos numéricos, subtotalizando datos por categorías y subcategorías. El modo dinámico es como [tablas dinámicas en Microsoft Excel](https://support.microsoft.com/office/create-a-pivottable-to-analyze-worksheet-data-a9a84538-bfe9-40a9-a8e9-f99134456576).

Para activar y desactivar el modo dinámico, deslice el conmutador **Modo pivote** del panel **Columnas** (3). Cuando activa el modo pivote, el área **Etiquetas de columna** aparece en el panel. Utilice el área **Etiquetas de columna** para agrupar sumas totales de filas en categorías. Los campos que agregue al área **Etiquetas de columna** se mostrarán como columnas en el área de datos (1).

Desarrollar el análisis de datos en modo dinámico implica mover campos a las tres áreas: **Grupos de filas**, **Etiquetas de columnas** y **Valores**. La siguiente figura ilustra dónde se asignan los campos al área de datos (1), donde `sum` son los datos calculados y, opcionalmente, **Valores**.

<table>
<tr><th></th><th>Etiqueta de la columna</th><th></th><th>Etiqueta de la columna</th><th></th></tr>
<tr><th>Grupo de filas</th><th>Valor</th><th>Valor</th><th>Valor</th><th>Valor</th></tr>
<tr><td>fila</td><td>suma</td><td>suma</td><td>suma</td><td>suma</td></tr>
<tr><td>fila</td><td>suma</td><td>suma</td><td>suma</td><td>suma</td></tr>
<tr><td>fila</td><td>suma</td><td>suma</td><td>suma</td><td>suma</td></tr>
<tr><td>fila</td><td>suma</td><td>suma</td><td>suma</td><td>suma</td></tr>
</table>

> [!TIP]
> Las columnas que solo tienen unos pocos valores posibles son las mejores candidatas para usarlas en **Valores** de columnas.


## <a name="analyze-large-amounts-of-data"></a>Analizar grandes cantidades de datos

Si el conjunto de datos que desea analizar supera las 100 000 filas, se le sugiere ingresar a un modo de análisis optimizado para conjuntos de datos grandes. Actualmente existen dos limitaciones si cambia a este modo: 

- El formato de los campos de los siguientes cuatro tipos de datos puede cambiar: 

   - divisa 
   - decimales (siempre se muestran con dos decimales) 
   - fechas (siempre se muestran en el formato AAAA-MM-DD)
   - zonas horarias
- Los campos que se utilizan en modo dinámico y se agregan a las etiquetas de las columnas deben tener una cantidad baja de valores distintos.

   Si habilita el modo dinámico y arrastra un campo al área **Etiquetas de columna**, donde los datos subyacentes para ese campo tienen demasiados valores distintos, entonces la pestaña del navegador podría dejar de responder y eventualmente se cierra, lo que requiere que usted comience de nuevo en una nueva sesión. En este caso, no gire sobre ese campo o establezca un filtro en el campo antes de agregarlo al área **Etiquetas de columna**.

## <a name="share-data-analysis"></a>Compartir análisis de datos

Después de haber preparado un análisis en una pestaña, puede compartirlo como un vínculo con compañeros de trabajo y otras personas de su organización directamente desde el cliente. Sólo los destinatarios que tengan permiso sobre la empresa y los datos pueden utilizar el enlace.

1. En la pestaña de análisis, seleccione la punta de flecha hacia abajo y luego seleccione **Copiar enlace**.

   ![Muestra la acción para copiar un análisis](media/copy-analysis.svg)

   Se abre el cuadro de diálogo **Enlace a \<tab name\>**.

1. De forma predeterminada, el análisis que comparta se vinculará a la página o consulta de la empresa en la que trabaja actualmente, que se indica con `company=<company_name>` en el campo URL junto al botón **Copiar**. Si desea enviar un enlace a un análisis que no está asociado con una empresa específica, establezca el campo **Empresa:** en **No vincular a una empresa específica**.

   ![Muestra el cuadro de diálogo Copiar enlace para una pestaña de análisis](media/analysis-link-copied.svg)

1. Seleccione **Copiar**.

1. Pegue el enlace en el medio de comunicación de su elección, como Word, Outlook, Teams, OneNote, etc. 

2. Una vez recibido, los destinatarios pueden seleccionar el enlace y abrir el análisis de la página o consulta en Business Central. Se les solicita que especifiquen un nombre para la nueva pestaña de análisis que se creará.  

## <a name="limitations-in-2023-release-wave-1-preview"></a>Limitaciones en el primer lanzamiento de versiones de 2023 (vista previa)

La vista previa pública de esta característica tiene las siguientes limitaciones:

- La vista del modo análisis tiene un límite de 100 000 filas. Si supera este límite, recibirá un mensaje indicándoselo. Para solucionar esta limitación, configure los filtros en la página antes de cambiar al modo de análisis, si es posible. Tal vez desee analizar un determinado grupo de clientes o solo desee datos del año en curso. También puede elegir una vista predefinida si funciona para su análisis.
- La función de análisis de datos compartidos no está disponible.
- La capacidad de guardar opciones de análisis de datos preferidas en páginas de lista y guardar menús de análisis por pestaña de análisis no está disponible actualmente.

## <a name="see-also"></a>Consulte también .

[Análisis de datos ad hoc](reports-adhoc-analysis.md)  
[Ver y editar en Excel](across-work-with-excel.md)  
