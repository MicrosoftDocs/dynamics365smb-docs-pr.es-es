---
title: Analizar datos en páginas de lista usando el modo de análisis de datos
description: Aprenda a usar el modo de análisis de datos en Business Central para analizar datos.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.date: 03/30/2023
ms.custom: bap-template
ms.service: dynamics365-business-central
ms.search.form: '456, 457, 458, 459, 460, 461, 16, 22, 25, 26, 27, 31, 143, 144, 9300, 9301, 9303, 9304, 9305, 9306, 9307, 9309, 9310, 9311'
---
# <a name="analyze-list-data-using-data-analysis-mode"></a><a name="analyze-list-data-using-data-analysis-mode"></a>Analizar datos en lista usando el modo de análisis de datos

En este artículo, aprenderá a analizar datos de páginas en listas mediante el *modo de análisis de datos*. El modo de análisis de datos le permite analizar datos directamente desde la página, sin tener que ejecutar un informe o cambiar a otra aplicación, como Excel. Proporciona una forma interactiva y versátil de calcular, resumir y examinar datos. En lugar de ejecutar informes con diferentes opciones y filtros, puede agregar varias pestañas que representen diferentes tareas o vistas de los datos. Los ejemplos podrían ser "Mis clientes", "Elementos de seguimiento", "Proveedores agregados recientemente", "Estadísticas de ventas" o cualquier otra vista que pueda imaginar.

> [!TIP]
> Lo bueno del modo de análisis de datos es que no cambia ninguno de los datos subyacentes de la página de lista ni el diseño de la página cuando no está en modo de análisis de datos. Entonces, la mejor manera de aprender qué puede hacer en el modo de análisis de datos es probar cosas.

## <a name="prerequisite"></a><a name="prerequisite"></a>Requisito previo

El modo de análisis de datos se encuentra actualmente en versión preliminar, lo que significa que un administrador debe activarlo antes de que pueda usarlo. Si es administrador y desea activar el modo de análisis de datos, vaya a la página **Administración de características** y habilite **Actualización de funciones: modo de análisis, analice rápidamente los datos directamente en Business Central**. Para más información sobre la activación y desactivación de características, vaya a [Administración de características](/dynamics365/business-central/dev-itpro/administration/feature-management).

## <a name="get-started"></a><a name="get-started"></a>Comenzar

1. Abra la página de lista.

   Por ejemplo, para trabajar con **Asientos de libro mayor de clientes**, seleccione el icono de la característica ![Lupa que abre la función Dígame.](media/ui-search/search_small.png) (<kbd>Alt</kbd>+<kbd>Q</kbd>), escriba *Movimientos de contabilidad de clientes* y luego elija el vínculo relacionado.  
2. En la barra de acciones de la parte superior de la página, active el interruptor **Analizar**.

    El modo de análisis de datos abre los datos en una experiencia optimizada para el análisis de datos.  En el modo de análisis de datos, la barra de acción normal se reemplaza con una barra de modo de análisis de datos especial. La siguiente figura ilustra las diferentes áreas de una página en el modo de análisis de datos.

   [![Muestra una descripción general de una página en el modo de análisis de datos](media/analysis-mode-overview-2.png)](media/analysis-mode-overview-2.png#lightbox)

   Cada área se explica en las secciones siguientes.

3. Utilice las diferentes áreas para manipular, resumir y analizar datos. Vea las secciones siguientes para obtener detalles.

4. Cuando desee salir del modo de análisis, desactive el conmutador **Analizar**.

   Las pestañas de análisis que ha agregado permanecerán hasta que las elimine. Entonces, si regresa al modo de análisis de datos nuevamente, las verá exactamente como las dejó.

> [!NOTE]
> Los datos que se muestran en el modo de análisis están controlados por los filtros o vistas establecidos en la página de lista. Esto le permite filtrar previamente los datos antes de entrar al modo de análisis.

## <a name="work-with-data-analysis-mode"></a><a name="work-with-data-analysis-mode"></a>Trabajar con el modo de análisis de datos

En el modo de análisis de datos, la página se divide en dos áreas:

- El área principal, que consta del área de datos (1), la barra de resumen (2) y la barra de pestañas (5)
- El área de manipulación de datos, que consta de dos paneles: columnas (3) y filtros de análisis (4).

### <a name="data-area-1"></a><a name="data-area-1"></a>Área de datos (1)

El área de datos es donde se muestran las filas y columnas de la página de lista y se resumen los datos. El área de datos proporciona una forma versátil de controlar el diseño de las columnas y una forma rápida de obtener un resumen de los datos. Para las columnas que contienen valores numéricos, la suma de todos los valores de la columna se muestra en la última fila, a menos que haya definido grupos de filas. En este caso, las sumas aparecen como subtotal para los grupos.  

![Muestra una descripción general del área de datos en una página en el modo de análisis de datos](media/analysis-mode-data-area.png)

- Para mover una columna, selecciónela y arrástrela hasta donde tenga más sentido en su análisis.
- Haga clic con el botón derecho en la columna o coloque el cursor sobre ella y seleccione el icono de menú ![Muestra el icono en una columna en el modo de análisis de datos que abre un menú de acciones](media/analysis-mode-column-menu-icon.png) para acceder a varias acciones que puede realizar en las columnas. Por ejemplo:

  - Para anclar una columna a la izquierda o a la derecha del área de datos para que no se mueva de la pantalla cuando se desplace, seleccione ![Muestra el icono en una columna en el modo de análisis de datos que abre un menú de acciones](media/analysis-mode-column-menu-icon.png) > **Anclar columna** > **Anclar a la izquierda** la parte de la columna.
  - Defina filtros de datos directamente en la definición de columna en lugar de ir a los paneles de **Filtros de análisis**. Todavía puede echar un vistazo a los detalles sobre los datos relacionados y de cada línea, así como abrir la tarjeta para obtener más información sobre una entidad determinada.
- Utilice el área de datos para interactuar con los datos. Para las columnas que contienen valores sumables numéricos, puede obtener estadísticas descriptivas en un conjunto de campos, marcándolos. Las estadísticas aparecen en la barra de estado (2), en la parte inferior de la página.
- Exportar datos en formato Excel o csv. Simplemente, haga clic con el botón derecho en el área de datos o en una selección de celdas para exportar.

### <a name="summary-bar-2"></a><a name="summary-bar-2"></a>Barra de resumen (2)

La barra de resumen se encuentra en la parte inferior de la página y muestra estadísticas sobre los datos de la lista. A medida que interactúa con columnas cuyos valores se pueden sumar, como al seleccionar varias filas en una columna que muestra cantidades, los datos se actualizarán.

![Muestra una descripción general de una barra de resumen en el modo de análisis de datos](media/analysis-mode-totals-row.png)

La siguiente tabla describe los diferentes números que se muestran en el área de totales:

|Número|Descripción|
|-|-|
|Filas|El número de filas seleccionadas como parte del número total de filas disponibles. |
|Total de filas|El número de filas en la lista sin filtrar.|
|Filtrado|El número de filas mostradas como resultado de los filtros aplicados a la lista.|
|Promedio|El valor promedio en todos los campos sumables seleccionados.|
|Total|El número de filas seleccionadas.|
|Mín|El valor mínimo en todos los campos sumables seleccionados.|
|Máx|El valor máximo en todos los campos sumables seleccionados.|
|Suma|La suma total de todos los valores en los campos sumables seleccionados.|

### <a name="columns-3"></a><a name="columns-3"></a>Columnas (3)

El panel **Columnas** es uno de los dos paneles que trabajan juntos para definir su análisis. La otra zona es el panel **Filtros de análisis**. El panel **Columnas** se utiliza para resumir los datos. Utilice el panel **Columnas** para definir qué columnas deben incluirse en el análisis.

![Muestra una descripción general del panel de columnas en el modo de análisis de datos](media/analysis-mode-columns-2.png)

|Áreas|Descripción|
|-|-|
|Buscar/marcar o borrar todas las casillas|Buscar columnas. Seleccione la casilla para seleccionar/limpiar todas las columnas.|
|Casillas|Esta área incluye una casilla para cada campo en la tabla de origen de la lista. Utilice esta área para cambiar las columnas que se muestran en la lista. Seleccione una casilla para mostrar la columna del campo en la página; limpie la casilla para ocultar la columna. |
|Grupos de filas|Utilice esta área para agrupar y sumar datos por uno o más campos. Solo puede incluir campos no numéricos, como campos de texto, fecha y hora. Los grupos de filas se usan a menudo en modo dinámico.|
|Valores|Utilice esta área para especificar los campos para los que desea una suma total. Solo puede incluir campos que contengan números que se puedan sumar; por ejemplo, no campos de texto, fecha u hora.|

Para mover un campo de un área a otra, seleccione el icono de agarrar ![Muestra una descripción general de una página en el modo de análisis de datos](media/column-grab-icon.png) junto a la columna en la lista anterior y arrástrelo al área de destino. No puede mover un campo a un área donde no está permitido.

### <a name="analysis-filters-4"></a><a name="analysis-filters-4"></a>Filtros de análisis (4)

El panel **Filtros de análisis** le permite establecer más filtros de datos en las columnas para limitar las entradas de la lista. Establezca filtros en las columnas para limitar las entradas en la lista y las sumas posteriores solo a aquellas entradas que le interesen según los criterios que defina. Por ejemplo, suponga que solo le interesan los datos de un cliente específico o los pedidos de ventas que superan un importe específico. Para establecer un filtro, seleccione la columna, elija la operación de comparación de la lista (como **Iguales** o **Comienza por**) y luego introduzca el valor.

![Muestra una descripción general del panel de filtros en el modo de análisis de datos](media/analysis-mode-filters.png)

> [!NOTE]
> Los filtros adicionales solo se aplican a la pestaña de análisis actual. Esto le permite definir exactamente los filtros de datos adicionales que se necesitan para un análisis específico.

### <a name="tabs-5"></a><a name="tabs-5"></a>Pestañas (5)

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

## <a name="pivot-mode"></a><a name="pivot-mode"></a>Modo dinámico

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

## <a name="limitations"></a><a name="limitations"></a>Limitaciones

La vista de análisis actualmente tiene un límite de 100 000 filas. Si supera este límite, recibirá un mensaje indicándoselo. Para solucionar esta limitación, configure los filtros en la página antes de cambiar al modo de análisis de datos, si es posible.  Tal vez desee analizar un determinado grupo de clientes o tal vez solo desee datos del año en curso. También puede elegir una vista predefinida si funciona para su análisis.

## <a name="see-also"></a><a name="see-also"></a>Consulte también .

[Análisis de datos ad hoc](reports-adhoc-analysis.md)  
[Ver y editar en Excel](across-work-with-excel.md)  
