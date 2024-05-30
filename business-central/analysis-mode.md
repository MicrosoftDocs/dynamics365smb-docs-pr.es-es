---
title: Analizar página de lista y datos de consulta usando el análisis de datos
description: Aprenda a usar el modo de análisis en Business Central para analizar datos.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.date: 04/29/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
ms.search.form: '456, 457, 458, 459, 460, 461, 16, 22, 25, 26, 27, 31, 143, 144, 9300, 9301, 9303, 9304, 9305, 9306, 9307, 9309, 9310, 9311'
---
# Analizar página de lista y datos de consulta usando la característica de análisis de datos

> **SE APLICA A:** Vista previa pública en el primer lanzamiento de versiones de Business Central 2023 y posteriores para analizar páginas de lista; Generalmente disponible en el segundo lanzamiento de versiones de Business Central 2023 para analizar datos de páginas de listas y consultas.

Este artículo explica cómo utilizar la función de análisis de datos de páginas de listas y consultas. El análisis de datos le permite analizar los datos directamente desde la página, sin tener que ejecutar un informe o abrir otra aplicación, como Excel. La característica proporciona una forma interactiva y versátil de calcular, resumir y examinar datos. En lugar de ejecutar informes con diferentes opciones y filtros, puede agregar varias pestañas que representen diferentes tareas o vistas de los datos. Algunos ejemplos son "Mis clientes", "Elementos de seguimiento", "Proveedores agregados recientemente", "Estadísticas de ventas" o cualquier otra vista que pueda imaginar.

> [!TIP]
> Lo bueno de la función de análisis de datos es que no cambia los datos subyacentes de una página de lista o consulta. Tampoco cambia el diseño de la página o consulta cuando no está en modo de análisis. Entonces, la mejor manera de aprender qué puede hacer en el modo de análisis es probar cosas.

## Requisitos previos

- Si está utilizando [!INCLUDE [prod_short](includes/prod_short.md)] versión 22, la característica de análisis de datos está en versión preliminar. Por lo tanto, un administrador debe habilitarlo antes de poder utilizarlo. Para habilitarlo, vaya a la página **Administración de características** y active la **Actualización de funciones: modo de análisis, analice rápidamente los datos directamente en Business Central**. [Más información acerca de la Administración de características](/dynamics365/business-central/dev-itpro/administration/feature-management).
- En la versión 23 y posteriores, a su cuenta se le debe asignar el conjunto de permisos **ANÁLISIS DE DATOS - EXEC** o incluir permiso de ejecución en el objeto del sistema **9640 Permitir datos Modo de análisis**. Como administrador, puede excluir estos permisos a los usuarios que no desea que tengan acceso al modo de análisis.

> [!NOTE]
> Algunas páginas de lista que no ofrecen la opción **Entrar en el modo de análisis** para activar el modo de análisis. La razón es que los desarrolladores pueden desactivar el modo de análisis en páginas específicas utilizando la propiedad  [AnalysisModeEnabled](/dynamics365/business-central/dev-itpro/developer/properties/devenv-analysismodeenabled-property) en AL.

## Introducción

Siga estos pasos para empezar a utilizar el modo de análisis.

>[!TIP]
> El modo de análisis también incluye una característica de Copilot llamada *asistencia de análisis* que puede ayudarle a comenzar. [Obtenga más información sobre la asistencia de análisis con Copilot](analysis-assist.md).

1. Abra la página de lista o consulta.

   Por ejemplo, para trabajar con la página **Asientos de libro mayor de clientes**, seleccione el icono de la característica ![Lupa que abre la función Dígame.](media/ui-search/search_small.png) (<kbd>Alt</kbd>+<kbd>Q</kbd>), escriba *Movimientos de contabilidad de clientes* y luego elija el vínculo relacionado. 

2. En la barra de acciones en la parte superior de la página, seleccione el botón **Entrar en el modo de análisis** ![Muestra el botón para activar el modo de análisis](media/analysis-mode-icon.png).

    El modo de análisis abre los datos en una experiencia optimizada para el análisis de datos. En el modo de análisis, la barra de acción normal se reemplaza con una barra de modo de análisis especial. La siguiente figura ilustra las diferentes áreas de una página en el modo de análisis.

   [![Muestra una descripción general de una página en el modo de análisis de datos](media/analysis-mode-overview-3.png)](media/analysis-mode-overview-3.png#lightbox)

   Cada área se explica en las secciones siguientes.

3. Utilice las diferentes áreas para manipular, resumir y analizar datos. Vea las secciones siguientes para obtener detalles.

4. Cuando desee detener el modo de análisis, seleccione el botón **Salir del modo de análisis** ![Muestra el botón para desactivar el modo de análisis](media/analysis-mode-exit-icon.png)

   Las pestañas de análisis que ha agregado permanecerán hasta que las elimine. Entonces, si regresa al modo de análisis nuevamente, las verá exactamente como las dejó.

> [!NOTE]
> Los datos que se muestran en el modo de análisis están controlados por los filtros o vistas establecidos en la página de lista. Esto le permite filtrar previamente los datos antes de entrar al modo de análisis.

## Trabajar con el modo de análisis

En el modo de análisis, la página se divide en dos áreas:

- El área principal, que consta del área de datos (1), la barra de resumen (2) y la barra de pestañas (5).
- El área de manipulación de datos, que consta de dos paneles: columnas (3) y filtros de análisis (4).

### Área de datos (1)

El área de datos es donde se muestran las filas y columnas de la página de consulta de lista y se resumen los datos. El área de datos proporciona una forma versátil de controlar el diseño de las columnas y una forma rápida de obtener un resumen de los datos. Para las columnas que contienen valores numéricos, la suma de todos los valores de la columna se muestra en la última fila, a menos defina grupos de filas. En este caso, las sumas aparecen como subtotal para los grupos.  

![Muestra una descripción general del área de datos en una página en el modo de análisis](media/analysis-mode-data-area.png)

- Para mover una columna, selecciónela y arrástrela hasta donde tenga más sentido en su análisis.
- Para ordenar por una columna, seleccione el encabezado de la columna. Para ordenar en varias columnas, seleccione y mantenga presionada la tecla <kbd>Shift</kbd> mientras selecciona los encabezados de columna que desea ordenar.
- Para tener acceso a varias acciones que puede realizar sobre las columnas, haga clic con el botón derecho del ratón sobre la columna o pase el ratón por encima y seleccione el icono de menú ![Muestra el icono en una columna en el modo de análisis que abre un menú de acciones](media/analysis-mode-column-menu-icon.png). Por ejemplo:

  - Para anclar una columna al área de datos para que no se mueva de la pantalla cuando se desplace, seleccione ![Muestra el icono en una columna en el modo de análisis que abre un menú de acciones](media/analysis-mode-column-menu-icon.png) > **Anclar columna** > **Anclar a la izquierda** la parte de la columna.
  - Defina filtros de datos directamente en la definición de columna en lugar de ir a los paneles de **Filtros de análisis**. Todavía puede echar un vistazo a los detalles sobre los datos relacionados y de cada línea, así como abrir la tarjeta para obtener más información sobre una entidad determinada.
- Utilice el área de datos para interactuar con los datos. Para las columnas que contienen valores sumables numéricos, puede obtener estadísticas descriptivas en un conjunto de campos, marcándolos. Las estadísticas aparecen en la barra de estado (2), en la parte inferior de la página.
- Exportar datos en formato Excel o csv. Haga clic con el botón derecho en el área de datos o en una selección de celdas para exportar.

### Barra de resumen (2)

La barra de resumen se encuentra en la parte inferior de la página y muestra estadísticas sobre los datos de la página de lista o consulta. A medida que interactúa con columnas cuyos valores se pueden sumar, como al seleccionar varias filas en una columna que muestra cantidades, los datos se actualizan.

![Muestra una descripción general de una barra de resumen en el modo de análisis](media/analysis-mode-totals-row.png)

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

### Columnas (3)

El panel **Columnas** es uno de los dos paneles que trabajan juntos para definir su análisis. La otra zona es el panel **Filtros de análisis**. El panel **Columnas** se utiliza para resumir los datos. Utilice el panel **Columnas** para definir qué columnas deben incluirse en el análisis.

![Muestra una descripción general del panel de columnas en el modo de análisis](media/analysis-mode-columns-3.png)

|Áreas|Descripción|
|-|-|
|Buscar/marcar o borrar todas las casillas|Buscar columnas. Para seleccionar/borrar todas las columnas, active la casilla de verificación.|
|Casillas|Esta área incluye una casilla para cada campo en la tabla de origen de la lista o consulta. Utilice esta área para cambiar las columnas que se muestran. Seleccione una casilla para mostrar la columna del campo en la página; limpie la casilla para ocultar la columna. |
|Grupos de filas|Utilice esta área para agrupar y sumar datos por uno o más campos. Solo puede incluir campos no numéricos, como campos de texto, fecha y hora. Los grupos de filas se usan a menudo en modo dinámico.|
|Valores|Utilice esta área para especificar los campos para los que desea una suma total. Solo puede incluir campos que contengan números que se puedan sumar; por ejemplo, no campos de texto, fecha u hora.|

Para mover un campo de un área a otra, seleccione el icono de agarrar ![Muestra el botón para capturar un campo en el modo de análisis](media/column-grab-icon.png) junto a la columna en la lista y arrástrelo al área de destino. No puede mover un campo a un área donde no está permitido.

### Filtros de análisis (4)

El panel **Filtros de análisis** le permite establecer más filtros de datos en las columnas para limitar las entradas de la lista. Establezca filtros en las columnas para limitar las entradas en la lista y las sumas posteriores solo a aquellas entradas que le interesen según los criterios que defina. Por ejemplo, suponga que solo le interesan los datos de un cliente específico o los pedidos de ventas que superan un importe específico. Para establecer un filtro, seleccione la columna, elija la operación de comparación de la lista (como **Iguales** o **Comienza por**) y luego introduzca el valor.

![Muestra una descripción general del panel de filtros en el modo de análisis de datos](media/analysis-mode-filters-2.png)

> [!NOTE]
> Los filtros adicionales solo se aplican a la pestaña de análisis actual. Esto le permite definir exactamente los filtros de datos adicionales que se necesitan para un análisis específico.

### Pestañas (5)

El área de pestañas de la parte superior le permite crear diferentes configuraciones (columnas y filtros de análisis) en pestañas separadas, donde puede manipular los datos de las pestañas de forma independiente. Siempre hay al menos una pestaña, llamada **Análisis 1**, de forma predeterminada. Agregar más pestañas es beneficioso para guardar configuraciones de análisis de uso frecuente en un conjunto de datos. Por ejemplo, puede tener pestañas para analizar datos en modo dinámico y otras pestañas que filtran a un subconjunto de filas. Algunas pestañas pueden mostrar una vista detallada con muchas columnas y otras solo mostrar algunas columnas clave.

Aquí hay algunos consejos sobre cómo trabajar con varias pestañas de análisis:

- Para agregar una nueva pestaña, seleccione el signo grande **+** junto a la última pestaña de análisis.
- Seleccione la punta de flecha hacia abajo en una pestaña para acceder a una lista de acciones que puede realizar en una pestaña, como cambiar el nombre, duplicar, eliminar y mover.

   - **Eliminar** elimina la pestaña que tiene abierta actualmente. **Eliminar todo** elimina todas las pestañas que ha agregado, excepto la pestaña predeterminada **Análisis 1** .
- No puede eliminar por completo **Análisis 1**, pero puede cambiarle el nombre mediante la acción **Renombrar** y borrar los cambios que ha realizado utilizando **Eliminar** o **Eliminar todo**.  

- Las pestañas de análisis que ha agregado y configurado permanecerán hasta que las elimine. Entonces, si regresa al modo de análisis nuevamente, las verá exactamente como las dejó.

   > [!TIP]
   > Las pestañas que configuras solo son visibles para usted. Otros usuarios solo verán las pestañas que hayan configurado.
- Puede copiar pestañas de análisis. Copiar puede resultar útil, por ejemplo, para experimentar cambiando una pestaña sin cambiar el original. Copiar también es útil si desea crear diferentes variaciones del mismo análisis.

## Jerarquías de fecha

En el modo de análisis, los campos de fecha del conjunto de datos se generan en una jerarquía Año-Trimestre-Mes de tres campos separados. Esta jerarquía se basa en el calendario normal, no en ningún calendario fiscal definido en Business Central.

Los campos adicionales reciben el nombre *\<field name\> Año*, *\<field name\> Trimestre* y *\<field name\> Mes*. Por ejemplo, si el conjunto de datos incluye un campo llamado *Fecha de publicación*, entonces la jerarquía de fechas correspondiente consta de campos llamados *Año de fecha de publicación*, *Trimestre de fecha de contabilización*, y *Mes de fecha de contabilización*.

> [!NOTE]
> Actualmente, la jerarquía de fechas solo se aplica a los campos de tipo date, no a los campos de tipo de fecha y hora.

## Modo dinámico

Puede usar el modo dinámico para analizar una gran cantidad de datos numéricos, subtotalizando datos por categorías y subcategorías. El modo dinámico es como [tablas dinámicas en Microsoft Excel](https://support.microsoft.com/office/create-a-pivottable-to-analyze-worksheet-data-a9a84538-bfe9-40a9-a8e9-f99134456576).

Para activar y desactivar el modo dinámico, active el conmutador **Modo dinámico** del panel **Columnas** (3). Cuando activa el modo dinámico, el área **Etiquetas de columna** aparece en el panel. Utilice el área **Etiquetas de columna** para agrupar sumas totales de filas en categorías. Los campos que agregue al área **Etiquetas de columna** se mostrarán como columnas en el área de datos (1).

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

## Analizar grandes cantidades de datos

Si el conjunto de datos que desea analizar supera las 100 000 filas, se le sugiere ingresar a un modo de análisis optimizado para conjuntos de datos grandes. Actualmente existen dos limitaciones si cambia a este modo: 

- El formato de los campos de los siguientes cuatro tipos de datos puede cambiar: 

   - divisa 
   - decimales (siempre se muestran con dos decimales) 
   - fechas (siempre se muestran en el formato AAAA-MM-DD)
   - zonas horarias
- Los campos que se utilizan en modo dinámico y se agregan a las etiquetas de las columnas deben tener una cantidad baja de valores distintos.

   Si habilita el modo dinámico y arrastra un campo al área **Etiquetas de columna**, donde los datos subyacentes para ese campo tienen demasiados valores distintos, entonces la pestaña del navegador podría dejar de responder. El navegador acaba cerrándose, lo que le obliga a empezar de nuevo en una nueva sesión. En este caso, no gire sobre ese campo o establezca un filtro en el campo antes de agregarlo al área **Etiquetas de columna**.

## Compartir análisis de datos

Después de preparar un análisis en una pestaña, puede compartirlo como un vínculo con compañeros de trabajo y otras personas de su organización directamente desde el cliente. Sólo los destinatarios que tengan permiso sobre la empresa y los datos pueden utilizar el enlace.

1. En la pestaña de análisis, seleccione la punta de flecha hacia abajo y luego seleccione **Copiar enlace**.

   ![Muestra la acción para copiar un análisis](media/analysis-mode-copy.png)

   Se abre el cuadro de diálogo **Enlace a \<tab name\>**.

1. De forma predeterminada, el análisis que comparta se vinculará a la página o consulta de la empresa en la que trabaja actualmente, que se indica con `company=<company_name>` en el campo URL junto al botón **Copiar**. Si desea enviar un enlace a un análisis que no está asociado con una empresa específica, establezca el campo **Empresa:** en **No vincular a una empresa específica**.

   ![Muestra el cuadro de diálogo Copiar enlace para una pestaña de análisis](media/analysis-link-copied.svg)

1. Seleccione **Copiar**.
1. Pegue el enlace en el medio de comunicación de su elección, como Word, Outlook, Teams, OneNote, etc.
1. Una vez recibido, los destinatarios pueden seleccionar el enlace y abrir el análisis de la página o consulta en [!INCLUDE [prod_short](includes/prod_short.md)]. Se les solicita que especifiquen un nombre para la nueva pestaña de análisis que se crea.  

## Ejemplos de cómo analizar datos

Utilice la característica **Análisis de datos** para una verificación rápida de hechos y un análisis ad hoc:

- Si no desea ejecutar un informe.
- Si no existe un informe para su necesidad específica.
- Si desea iterar rápidamente para obtener una buena descripción general de una parte de su negocio.

Las siguientes secciones proporcionan ejemplos de escenarios para muchas de las áreas funcionales en [!INCLUDE [prod_short](includes/prod_short.md)].

### Ejemplo: Finance (Cobros)

Para ver lo que sus clientes le deben, quizás desglosado en intervalos de tiempo para saber cuándo vencen los importes, siga estos pasos:

1. Abra la lista [Movimientos de cliente](https://businesscentral.dynamics.com/?page=25) y elija :::image type="content" source="media/analysis-mode-icon.png" alt-text="Entrar en el modo de análisis."::: para activar el modo de análisis.
1. Vaya al menú **Columnas** y elimine todas las columnas (seleccione la casilla junto al campo *Buscar* a la derecha).
1. Active la opción **Modo* dinámico** (ubicada encima del campo **Buscar** de la derecha).
1. Arrastre el campo **Nombre del cliente** al área **Grupos de filas** y arrastre **Importe restante** hacia el área **Valores**.
1. Arrastre el campo **Fecha de vencimiento (mes)** y arrástrelo al área **Etiquetas de columna**.
1. Para realizar el análisis para un año o trimestre determinado, aplique un filtro en el menú **Filtros de análisis** (ubicado debajo del menú **Columnas** de la derecha).
1. Cambie el nombre de su pestaña de análisis a **Cuentas antiguas por mes** o algo que describa este análisis.

### Ejemplos de análisis de datos ad hoc por área funcional

Muchas de las áreas funcionales en [!INCLUDE[prod_short](includes/prod_short.md)] tienen artículos con ejemplos de análisis de datos ad hoc.

[!INCLUDE[ad-hoc-analysis-scenarios-table](includes/ad-hoc-analysis-scenarios-table.md)]

## Limitaciones en el primer lanzamiento de versiones de 2023 (vista previa)

La vista previa pública de esta característica tiene las siguientes limitaciones:

- La vista del modo análisis tiene un límite de 100 000 filas. Si supera este límite, recibirá un mensaje indicándoselo. Para solucionar esta limitación, configure los filtros en la página antes de cambiar al modo de análisis, si es posible. Tal vez desee analizar un determinado grupo de clientes o solo desee datos del año en curso. También puede elegir una vista predefinida si funciona para su análisis.
- La función de análisis de datos compartidos no está disponible.
- La capacidad de guardar opciones de análisis de datos preferidas en páginas de lista y guardar menús de análisis por pestaña de análisis no está disponible actualmente.

## Consulte también

[Análisis de datos ad hoc por área funcional](ad-hoc-data-analysis-by-functional-area.md)   
[Análisis de datos ad hoc](reports-adhoc-analysis.md)  
[Ver y editar en Excel](across-work-with-excel.md)  
