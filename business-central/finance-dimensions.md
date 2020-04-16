---
title: Trabajar con dimensiones | Documentos de Microsoft
description: Puede utilizar dimensiones para clasificar movimientos, por ejemplo, por departamentos o proyecto, por lo que le será muy fácil realizar un seguimiento de los datos y analizarlos.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, history, track
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 61e39b15042a4c3bd21ef1297d90803496305f8f
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/01/2020
ms.locfileid: "3183793"
---
# <a name="working-with-dimensions"></a>Trabajar con dimensiones
Para simplificar la realización de análisis en documentos, como pedidos de venta, puede utilizar dimensiones. Las dimensiones son atributos y valores que clasifican los movimientos de modo que pueda realizar el seguimiento y el análisis de ellos. Por ejemplo, las dimensiones pueden indicar de qué proyecto o departamento procede un movimiento.  

Por ejemplo, en lugar de tener que configurar cuentas contables generales independientes para cada departamento y proyecto puede usar dimensiones. De este modo, dispone de la posibilidad de análisis, sin crear un plan de cuentas complicado. Para obtener más información, consulte [Inteligencia empresarial](bi.md).

Otro ejemplo es configurar una dimensión que se llame *Departamento* y usarla junto con esta dimensión cuando registre documentos de ventas. Así podrá usar herramientas la de inteligencia empresarial para ver qué departamento vende cada producto.
Cuantas más dimensiones use, más detallados serán los informes en los que pueda basar sus decisiones empresariales. Por ejemplo, un movimiento de ventas individual puede incluir información de múltiples dimensiones, por ejemplo:  

* La cuenta en la que se registró la venta del producto  
* Dónde se vendió el producto
* Quién lo vendió
* El tipo de cliente que lo compró  

## <a name="analyzing-by-dimensions"></a>Analizar por dimensiones
La funcionalidad Dimensiones desempeña una función importante en la inteligencia empresarial, por ejemplo al definir vistas de análisis. Para obtener más información, vea [Analizar datos por dimensiones](bi-how-analyze-data-dimension.md).

> [!TIP]
> Como una forma rápida de analizar datos transaccionales por dimensiones, puede filtrar por dimensiones los totales del plan de cuentas y movimientos en todas las páginas **Movimientos**. Busque la acción **Establecer filtro de dimensiones**.

## <a name="dimension-sets"></a>Grupos de dimensiones
Un grupo de dimensiones es una combinación única de valores de dimensión. Se almacena como movimientos de grupo de dimensiones en la base de datos. Cada movimiento de grupo de dimensiones representa un valor de dimensión único. El grupo de dimensiones se identifica por medio de un id común del grupo de dimensiones que está asignado a cada movimiento de grupo de dimensiones que pertenece al grupo de dimensiones.  

Cuando crea una línea de diario, cabecera de documentos o línea de documentos, puede especificar una combinación de valores de dimensión. En lugar de explícitamente guardar cada valor de dimensión en la base de datos, un Id. de grupo de dimensiones se asigna a la línea de diario, cabecera de documentos o línea de documentos para especificar el grupo de dimensiones.  

## <a name="setting-up-dimensions"></a>Configurar dimensiones
Puede definir las dimensiones y los valores de dimensión para clasificar los diarios y los documentos, como pedidos de venta y pedidos de compra. Las dimensiones se configuran en la página **Dimensiones**, donde se crea una línea para cada dimensión, como *Proyecto*, *Departamento*, *Área* y *Vendedor*.

También se configuran los valores de dimensión. Por ejemplo, los valores pueden ser departamentos de su empresa. Los valores de dimensiones se pueden configurar en una estructura jerárquica similar al plan de cuentas, de modo que los datos se puedan desglosar en diversos niveles de granularidad y se puedan totalizar subconjuntos de valores de dimensiones. Puede definir tantas dimensiones y valores de dimensión como necesite y cualquier usuario de su empresa puede usarlos.

Cuando se configuran las dimensiones y los valores, se pueden definir dimensiones globales y abreviadas en la página **Configuración de contabilidad**, que siempre estarán disponibles para seleccionar como campos en las líneas del diario y del documento, sin tener que abrir primero la página **Dimensiones**. Para obtener más información, vea [Para configurar dimensiones globales y abreviadas](finance-dimensions.md#to-set-up-global-and-shortcut-dimensions).

* Las **dimensiones globales** se usan como filtros, por ejemplo, en informes, trabajos por lotes y XMLports. Solo puede utilizar dos dimensiones globales, por lo que debería elegir las dimensiones que use a menudo.
* Las **dimensiones abreviadas** están disponibles como campos en líneas de diario y documento. Puede crear un máximo de seis.  

### <a name="to-set-up-default-dimensions-for-customers-vendors-and-other-accounts"></a>Para configurar dimensiones predeterminadas para clientes, proveedores y otras cuentas
Puede asignar una dimensión predeterminada para una determinada cuenta. La dimensión se copiará en el diario o el documento cuando introduzca el número de cuenta en una línea, pero puede eliminar o cambiar el código de la línea si es necesario. También puede convertir una dimensión en obligatoria para registrar un movimiento con un tipo de cuenta específico.  

1.  Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), introduzca **Dimensiones** y, a continuación, elija el enlace relacionado.  
2.  En la página **Dimensiones**, seleccione la dimensión correspondiente y elija la acción **Dimensión predet. tipo cta**.  
4.  Rellene una línea para cada nueva dimensión predeterminada que quiera configurar. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]  
>  Si desea hacer que una dimensión sea obligatoria pero no desea asignar un valor predeterminado a la dimensión, deje el campo **Cód. valor dimensión** en blanco y seleccione **Obligatorio** en el campo **Registro valor**.  

> [!WARNING]  
>  Si una cuenta se utiliza en el trabajo por lotes de **Ajustar tipo cambio** o el trabajo por lotes de **Reg. var. inventario en cont.**, no seleccione **código obligatorio** o **código igual**. Estos procesos no pueden utilizar códigos de dimensión.  

> [!NOTE]  
>  Si es necesario asignar a una cuenta una dimensión distinta a la dimensión predeterminada ya configurada para el tipo de cuenta, deberá configurar una dimensión predeterminada para dicha cuenta. La dimensión predeterminada de la cuenta en concreto sustituirá a la dimensión predeterminada del tipo de cuenta.  

### <a name="to-set-up-default-dimension-priorities"></a>Para configurar prioridades de dimensiones predeterminadas  
Distintos tipos de cuentas, por ejemplo, una cuenta de cliente y una cuenta de producto, pueden tener configuradas dimensiones predeterminadas diferentes. Como resultado, un movimiento puede tener más de una propuesta de dimensión predeterminada para una dimensión. Para evitar este tipo de conflictos, puede aplicar reglas de prioridad a los diversos orígenes.  

1.  Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), introduzca **Prioridades de dimensión** y luego elija el enlace relacionado.  
2.  En la página **Prioridades dimensión predet.**, en el campo **Cód. origen**, escriba el código de origen para la tabla de movimientos para la que se aplicarán las prioridades de dimensión predeterminadas.  
3.  Rellene una línea para cada prioridad de dimensión predeterminada que desee para el código de origen seleccionado.
4.  Repita el procedimiento para la cada código de origen para el que quiera configurar prioridades de dimensión predeterminadas.  

> [!IMPORTANT]  
>  Si configura dos tablas con la misma prioridad en un mismo código de origen, [!INCLUDE[d365fin](includes/d365fin_md.md)] seleccionará siempre la tabla con el Id. de tabla inferior.  

### <a name="to-set-up-dimension-combinations"></a>Para configurar combinaciones de dimensión  
Para evitar registrar movimientos con dimensiones contradictorias o irrelevantes, puede bloquear o limitar determinadas combinaciones de dos dimensiones. Una dimensión está bloqueada si no es posible registrar ambas dimensiones en el mismo movimiento independientemente de los valores de dimensión. Una combinación de dimensión limitada le permite registrar ambas dimensiones en el mismo movimiento, pero únicamente para determinadas combinaciones de valores de dimensión.

1.  Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), introduzca **Combinaciones de dimensión** y, a continuación, elija el enlace relacionado.  
2.  En la página **Combinación dimensión**, seleccione el campo de la combinación de dimensión y seleccione una de las opciones siguientes.  

    |Campo|Description|
    |----------------------------------|---------------------------------------|  
    |**Nº limitaciones**|Esta combinación de dimensión no tiene restricciones. Se permiten todos los valores de dimensión.|  
    |**Limitado**|Esta combinación de dimensión tiene determinadas restricciones en función de los valores de dimensión que introduzca. Debe definir las limitaciones en la página **Combinación valor dimensión**.|  
    |**Bloqueado**|Esta combinación de dimensión no está permitida.|  

3.  Si selecciona la opción **Limitado**, debe definir las combinaciones de valores de dimensión que están bloqueadas. Para ello, elija el campo para definir la combinación de dimensión.  
4.  A continuación, seleccione una combinación de valores de dimensión que esté bloqueada y escriba **Bloqueado** en el campo. Un campo en blanco significa que la combinación de valores de dimensión está permitida. Repita el proceso con múltiples dimensiones bloqueadas.  

> [!NOTE]  
>  Las mismas dimensiones se repiten tanto en las filas como en las columnas, por lo que todas las combinaciones de dimensiones aparecen dos veces. [!INCLUDE[d365fin](includes/d365fin_md.md)] muestra automáticamente el valor en ambos campos. No puede realizar ninguna selección en los campos de la esquina superior izquierda hacia abajo, ya que estos campos tienen la misma dimensión tanto en las filas como en las columnas.  
>   
>  La opción seleccionada no será visible hasta que no salga del campo.  
>   
>  Para mostrar el nombre de la dimensión en lugar del código, seleccione el campo **Muestra nombre columna**.

### <a name="to-set-up-global-and-shortcut-dimensions"></a>Para configurar dimensiones globales y abreviadas
Las dimensiones globales y abreviadas se pueden utilizar como un filtro en cualquier parte de [!INCLUDE[d365fin](includes/d365fin_md.md)], incluyendo en informes, procesos y vistas de análisis. Las dimensiones globales y abreviadas están siempre disponibles para ser insertadas directamente sin tener que abrir primero la página **Dimensiones**. En las líneas de diario y de documento, puede seleccionar dimensiones globales y abreviadas en un campo de la línea. Puede configurar dos dimensiones globales y ocho abreviadas. Elija las dimensiones que utiliza con más frecuencia.

> [!Important]  
> La modificación de una dimensión global o abreviada requiere que se actualicen todos los movimientos registrados con la dimensión. Puede realizar esta tarea con la función **Cambiar dimen. globales**, pero puede llevar mucho tiempo y puede afectar al rendimiento. Por lo tanto, elija cuidadosamente sus dimensiones globales y abreviadas para no tener que cambiarlas más tarde.

> [!Note]
> Al añadir o cambiar una dimensión global o abreviada, se cierra automáticamente la sesión y se vuelve a iniciar para que el nuevo valor esté preparado para su uso en toda la aplicación.

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Configuración de contabilidad** y luego elija el enlace relacionado.
2. En la ficha desplegable **Dimensiones**, rellene los campos. [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

#### <a name="to-change-global-dimensions"></a>Para cambiar las dimensiones globales
1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), introduzca **Cambiar dimensiones globales** y, a continuación, elija el enlace relacionado.
2. Pase el cursor por encima de las acciones y campos de la página para aprender a cambiar las dimensiones globales y abreviadas.

### <a name="example-of-dimension-setup"></a>Ejemplo de configuración de dimensiones
Supongamos que su empresa desea realizar un seguimiento de las transacciones en función de la estructura organizativa y las ubicaciones geográficas. Para ello, puede configurar dos dimensiones en la página **Dimensiones**:

* **ÁREA**  
* **DEPARTAMENTO**  

| Código | Name | Título código | Título filtro |
| --- | --- | --- | --- |
| ÁREA |Área |Código de área |Filtro Área |
| DPTO |Departamento |Código de departamento |Filtro departamento |

Para **ÁREA**, agregue los siguientes valores de dimensión:

| Código | Name | Tipo valor dimensión |
| --- | --- | --- |
| 10 |América |Principio-Total |
| 20 |América del Norte |Estándar |
| 30 |Pacífico |Estándar |
| 40 |Sudamérica |Estándar |
| 50 |América, total |Fin-Total |
| 60 |Europa |Principio-Total |
| 70 |UE |Estándar |
| 80 |No perteneciente a la UE |Estándar |
| 90 |Europa, Total |Fin-Total |

Para las dos áreas geográficas principales, América y Europa, agregue subcategorías para las regiones aplicando sangría a los valores de dimensión. De esta manera podrá elaborar informes sobre ventas o gastos en regiones, y obtener totales de las áreas geográficas más grandes. También puede usar países o regiones como valores de dimensión, o condados o poblaciones, dependiendo de la empresa.

> [!NOTE]  
>   Para configurar una jerarquía, los códigos deben estar en orden alfabético. Esto incluye los códigos de los valores de dimensión que se proporcionan en [!INCLUDE[d365fin](includes/d365fin_md.md)].  

Para **DEPARTAMENTO**, agregue los siguientes valores de dimensión:

| Código | Name | Tipo valor dimensión |
| --- | --- | --- |
| ADMIN |Administración |Estándar |
| PROD |Producción |Estándar |
| CCIAL |Ccial |Estándar |

Con esta configuración, puede agregar las dos dimensiones como las dos dimensiones globales en la página **Configuración de contabilidad**. Esto significa que puede usar ÁREA Y DEPARTAMENTO como filtros para los movimientos de contabilidad, así como en todos los informes y esquemas de cuentas. También están disponibles ambas dimensiones globales de forma automática para el uso en líneas de movimientos y cabeceras de documentos, como dimensiones abreviadas.

## <a name="getting-an-overview-of-dimensions-used-multiple-times"></a>Obtener una visión general de las dimensiones utilizadas varias veces
La página **Dimensiones predet.-Múltiple** especifica cómo un grupo de cuentas usa dimensiones y valores de dimensión. Puede hacerlo resaltando varias cuentas y, a continuación, especificando las dimensiones y los valores de dimensión predeterminados para todas las cuentas que ha resaltado en la lista de cuentas. Al especificar las dimensiones predeterminadas para las cuentas resaltadas, la aplicación sugerirá estas dimensiones y valores de dimensión cuando se utilice una de ellas, por ejemplo, en una línea de diario. Esto facilita el registro de movimientos, ya que los campos de dimensión se rellenan automáticamente. No obstante, los valores de dimensión sugeridos se pueden cambiar en, por ejemplo, una línea de diario.

La página **Dimensiones predet.-Múltiple** contiene los campos siguientes:

|Campo|Description|
|-----|-----------|  
|**Cód. dimensión**|Muestra todas las dimensiones que se han definido como dimensiones predeterminadas en una o varias cuentas resaltadas. Seleccionando el campo, puede ver una lista de todas las dimensiones disponibles. Si selecciona una dimensión, la dimensión seleccionada se definirá como la dimensión predeterminada para todas las cuentas resaltadas.|
|**Cód. valor dimensión**|Muestra un valor de dimensión único o el término (Problema). Si en el campo se muestra un valor de dimensión, todas las cuentas resaltadas tendrán el mismo valor de dimensión predeterminado para una dimensión. Si en el campo se muestra el término (Problema), no todas las cuentas resaltadas tendrán el mismo valor de dimensión predeterminado para una dimensión. Al seleccionar el campo, podrá ver una lista de todas las dimensiones que están disponibles para una dimensión. Si selecciona un valor de dimensión, el valor de dimensión seleccionado se definirá como el valor de dimensión predeterminado para todas las cuentas resaltadas.|
|**Registro valor**|Muestra una regla de valor al registrar única o el término (Problema). Si en el campo se muestra la regla de valor al registrar, todas las cuentas resaltadas tendrán la misma regla de valor al registrar para un valor de dimensión. Si en el campo se muestra el término (Problema), no todas las cuentas resaltadas tendrán la misma regla de valor al registrar para un valor de dimensión. Al seleccionar el campo Valor al registrar, podrá ver una lista de reglas de valor al registrar. Si selecciona una regla de valor al registrar, la regla de valor al registrar seleccionada se aplicará a todas las cuentas resaltadas.|

## <a name="using-dimensions"></a>Usar dimensiones
En un documento como un pedido de ventas, puede agregar información de dimensión de una línea en particular y del mismo documento. Por ejemplo, en la página **Pedido de ventas**, puede introducir valores de dimensión para las dos primeras dimensiones abreviadas en las líneas de venta individuales y puede agregar más información de dimensión si elige el botón **Dimensiones**.  

Si trabaja con un diario, puede agregar información de dimensiones a un movimiento del mismo modo, si ha configurado dimensiones abreviadas como campos directamente en las líneas de diario.  

Puede configurar dimensiones predeterminadas para cuentas o tipos de cuenta, para que esas dimensiones o valores de dimensión se completen automáticamente.

### <a name="to-view-global-dimensions-in-ledger-entry-pages"></a>Para ver dimensiones globales en páginas de movimientos de contabilidad  
El nombre y la definición de las dimensiones globales los establece la empresa. Para ver las dimensiones globales correspondientes a su empresa, abra la página **Configuración contabilidad**.  

En una página de movimiento de contabilidad, puede ver si hay dimensiones globales para los movimientos. Las dos dimensiones globales difieren del resto de las dimensiones porque se pueden utilizar como filtros en cualquier lugar de [!INCLUDE[d365fin](includes/d365fin_md.md)].  

1.  Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Plan de cuentas** y luego elija el enlace relacionado.  
2.  En la página **Plan de cuentas**, seleccione la acción **Movimientos**.  
3.  Para ver únicamente los movimientos relevantes, establezca uno o más filtros en la página.  
4.  Para ver todas las dimensiones de un movimiento, seleccione el movimiento y elija la acción **Dimensiones**.  

> [!NOTE]  
>  La página **Dimensiones movimiento** muestra las dimensiones de un movimiento de contabilidad cada vez. A medida que se desplaza por los movimientos de contabilidad, el contenido de la página **Dimensiones movimiento** va cambiando según corresponda.

## <a name="troubleshooting-dimensions-errors"></a>Solución de errores de dimensiones
Cuando se registran documentos o líneas de diario que contienen dimensiones, pueden producirse varios errores que suelen estar relacionados con una configuración o asignación de dimensiones errónea.

> [!NOTE]
> En la siguiente lista de posibles mensajes de error, los códigos *%X* son marcadores de posición para las variables de datos que el mensaje real contendrá en la interfaz de usuario dependiendo del contexto. Por ejemplo, *%1 %2 está bloqueado.* podría aparecer en la interfaz de usuario como "Código de dimensión ÁREA bloqueado".  

|Problema|Mensaje de error|Solución posible|
|-----|-------------|-----------------|
|Dimensión bloqueada|%1 %2 está bloqueado.|-Busque documentos no registrados que contengan el grupo de dimensiones con la dimensión bloqueada y desbloquéela.<br />-Elimine el grupo de dimensiones para la dimensión bloqueada.|
|Dimensión eliminada|%1 %2 no puede encontrarse.|-Restaure la dimensión que falta.<br />-Busque documentos no registrados que contengan el grupo de dimensiones con la dimensión que falta y agréguela.<br />-Elimine el grupo de dimensiones para la dimensión que falta.|
|Valor de dimensión bloqueada|%1 %2 - %3 está bloqueado.|-Busque documentos no registrados que contengan el grupo de dimensiones con el valor de dimensión bloqueada y desbloquéelo.<br />-Elimine el grupo de dimensiones para el valor de dimensión bloqueada.|
|Valor de dimensión eliminada|   Falta %1 para %2.|-Restaure el valor de dimensión que falta.<br />-Busque documentos no registrados que contengan el grupo de dimensiones con el valor de dimensión que falta y agréguela.<br />-Elimine el grupo de dimensiones para el valor de dimensión que falta.|
|Valor de dimensión no permitido|El tipo de valor de dimensión para %1 %2 - %3 no puede ser %4.|-Cambie el campo **Tipo valor dimensión** en la página **Valores de dimensión** a **Estándar** o **Principio-Total**.<br />-Elimine el grupo de dimensiones para el valor de dimensión bloqueada.|
|Combinación de dimensiones bloqueadas|Las dimensiones %1 y %2 no pueden usarse simultáneamente.|-Busque documentos no registrados que contengan el grupo de dimensiones con la combinación de dimensiones bloqueadas y desbloquéela.<br />-Modifique una de las líneas del conjunto de permisos en conflicto para la combinación de dimensiones.|
|Combinación de valores de dimensiones bloqueadas|Las combinaciones de dimensiones %1 - %2 y %3 - %4 no pueden utilizarse simultáneamente.|-Busque documentos no registrados que contengan el grupo de dimensiones con la combinación de valores de dimensiones bloqueadas y desbloquéela.<br />-Modifique una de las líneas del conjunto de permisos en conflicto para la combinación de valores de dimensiones.|
|Código de valor de dimensión en blanco para la dimensión predeterminada cuando el campo **Registro valor** contiene **Código Obligatorio**|- Seleccione un %1 para el %2 %3.<br />- Seleccione un %1 para el %2 %3 para %4 %5.|-Cambie el campo **Registro valor** en la página **Dimensión predeterminada**.<br />-Introduzca un valor de dimensión no vacío para la dimensión en conflicto en el grupo de dimensiones.|
|Código de valor de dimensión erróneo para la dimensión predeterminada cuando el campo **Registro valor** contiene **Igual código**|- Seleccione %1 %2 para el %3 %4.<br />- Seleccione %1 %2 para el %3 %4 para %5 %6.|-Cambie el campo **Registro valor** en la página **Dimensión predeterminada**.<br />-Introduzca un valor de dimensión requerido para la dimensión en conflicto en el grupo de dimensiones.|
|Código de valor de dimensión no vacío para la dimensión predeterminada en blanco cuando el campo **Registro valor** contiene **Igual código**|-%1 %2 debe estar en blanco.<br />-%1 %2 debe estar en blanco para %3 %4.|-Cambie el campo **Registro valor** en la página **Dimensión predeterminada**.<br />-Introduzca un código de valor de dimensión en blanco para la dimensión en conflicto en el grupo de dimensiones.|
|Valor de dimensión inesperado para la dimensión predeterminada cuando el campo **Registro valor** contiene **Sin código**|-%1 %2 no debe ser mencionado.<br />-%1 %2 no debe ser mencionado para %3 %4|-Cambie el campo **Registro valor** en la página **Dimensión predeterminada**.<br />-Elimine la línea conflictiva del grupo de dimensiones.|

## <a name="see-related-training-at-microsoft-learn"></a>Consulte Formación relacionada en [Microsoft Learn](/learn/modules/dimensions-dynamics-365-business-central/index)

## <a name="see-also"></a>Consulte también
[Inteligencia empresarial](bi.md)  
[Finanzas](finance.md)  
[Analizar datos por dimensiones](bi-how-analyze-data-dimension.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
