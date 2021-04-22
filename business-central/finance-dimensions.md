---
title: Trabajar con dimensiones para rastrear y analizar datos fácilmente
description: Puede utilizar dimensiones para clasificar movimientos, por ejemplo, por departamentos o proyecto, por lo que le será muy fácil realizar un seguimiento de los datos y analizarlos para ayudarle a tomar buenas decisiones empresariales.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, history, track, business intelligence
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: aa97686299648b81e68aef1a3701e0c32d73138a
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2021
ms.locfileid: "5774085"
---
# <a name="working-with-dimensions"></a>Trabajar con dimensiones
Las dimensiones son valores que clasifican los movimientos de modo que pueda realizar el seguimiento y el análisis de los documentos, como pedidos de venta. Las dimensiones pueden, por ejemplo, indicar de qué proyecto o departamento procede un movimiento.  

Por ejemplo, en lugar de configurar cuentas de libro mayor separadas para cada departamento y proyecto, puede utilizar las dimensiones como base para el análisis y evitar tener que crear un plan de cuentas complicado. Para obtener más información, consulte [Inteligencia empresarial](bi.md).

Otro ejemplo es configurar una dimensión que se llame *Departamento* y usarla junto con esta dimensión cuando registre documentos de ventas. Así podrá usar herramientas la de inteligencia empresarial para ver qué departamento vende cada producto. Cuantas más dimensiones use, más detallados serán los informes en los que pueda basar sus decisiones empresariales. Por ejemplo, un movimiento de ventas individual puede incluir información de múltiples dimensiones, como:  

* La cuenta en la que se registró la venta del producto  
* Dónde se vendió el producto
* Quién lo vendió
* El tipo de cliente que lo compró  

## <a name="analyzing-by-dimensions"></a>Analizar por dimensiones
Las Dimensiones desempeñan una función importante en la inteligencia empresarial, por ejemplo al definir vistas de análisis. Para obtener más información, vea [Analizar datos por dimensiones](bi-how-analyze-data-dimension.md).

> [!TIP]
> Una forma rápida de analizar datos transaccionales por dimensiones es usar la acción **Establecer filtro de dimensiones** para filtrar los totales por dimensiones en el plan de cuentas y en páginas de movimientos.

## <a name="dimension-sets"></a>Grupos de dimensiones
<!--we describe what they are, but not their value.-->
Un grupo de dimensiones es una combinación única de valores de dimensión. Se almacena como movimientos de grupo de dimensiones en la base de datos. Cada movimiento de grupo de dimensiones representa un valor de dimensión único. El grupo de dimensiones se identifica por medio de un id común del grupo de dimensiones que está asignado a cada movimiento de grupo de dimensiones que pertenece al grupo de dimensiones.  

Cuando crea una línea de diario, cabecera de documentos o línea de documentos, puede especificar una combinación de valores de dimensión. En lugar de explícitamente guardar cada valor de dimensión en la base de datos, un Id. de grupo de dimensiones se asigna a la línea de diario, cabecera de documentos o línea de documentos para especificar el grupo de dimensiones.  

## <a name="setting-up-dimensions"></a>Configurar dimensiones
Puede definir las dimensiones y los valores de dimensión para clasificar los diarios y los documentos, como pedidos de venta y pedidos de compra. Las dimensiones se configuran en la página **Dimensiones**, donde se crea una línea para cada dimensión, como *Proyecto*, *Departamento*, *Área* y *Vendedor*.

También se configuran los valores de dimensión. Por ejemplo, los valores pueden ser departamentos de su empresa. Los valores de dimensiones se pueden configurar en una estructura jerárquica similar al plan de cuentas, de modo que los datos se puedan desglosar en diversos niveles de granularidad y se puedan totalizar subconjuntos de valores de dimensiones. Puede definir tantas dimensiones y valores de dimensión como necesite y cualquier usuario de su empresa puede usarlos.

Cuando se configuran las dimensiones y los valores, se pueden definir dimensiones globales y abreviadas en la página **Configuración de contabilidad**, que siempre estarán disponibles para seleccionar como campos en las líneas del diario y del documento, y los movimientos contables, sin tener que abrir primero la página **Dimensiones**. Para obtener más información, vea [Para configurar dimensiones globales y abreviadas](finance-dimensions.md#to-set-up-global-and-shortcut-dimensions).

* Las **dimensiones globales** se usan como filtros, por ejemplo, en informes, trabajos por lotes y XMLports. Solo puede utilizar dos dimensiones globales, por lo que debería elegir las dimensiones que use a menudo.
* Las **dimensiones abreviadas** están disponibles como campos en diarios, líneas de documento y movimienos contables. Puede crear un máximo de ocho.  

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
>  Si es necesario tener una dimensión distinta a la dimensión predeterminada para el tipo de cuenta, debe configurar una dimensión predeterminada para dicha cuenta. La dimensión predeterminada de la cuenta sustituirá a la dimensión predeterminada del tipo de cuenta.  

### <a name="to-set-up-default-dimension-priorities"></a>Para configurar prioridades de dimensiones predeterminadas  
Distintos tipos de cuentas, por ejemplo, una cuenta de cliente y una cuenta de producto, pueden tener configuradas dimensiones predeterminadas diferentes. Como resultado, un movimiento puede tener más de una propuesta de dimensión predeterminada para una dimensión. Para evitar este tipo de conflictos, puede aplicar reglas de prioridad a los diversos orígenes.  

1.  Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), introduzca **Prioridades de dimensión** y luego elija el enlace relacionado.  
2.  En la página **Prioridades dimensión predet.**, en el campo **Cód. origen**, escriba el código de origen para la tabla de movimientos para la que se aplicarán las prioridades de dimensión predeterminadas.  
3.  Rellene una línea para cada prioridad de dimensión predeterminada que desee para el código de origen seleccionado.
4.  Repita el procedimiento para la cada código de origen para el que quiera configurar prioridades de dimensión predeterminadas.  

> [!IMPORTANT]  
>  Si configura dos tablas con la misma prioridad en un mismo código de origen, [!INCLUDE[prod_short](includes/prod_short.md)] seleccionará siempre la tabla con el Id. de tabla inferior.  

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
>  Las mismas dimensiones se repiten tanto en las filas como en las columnas, por lo que todas las combinaciones de dimensiones aparecen dos veces. [!INCLUDE[prod_short](includes/prod_short.md)] muestra automáticamente el valor en ambos campos. No puede realizar ninguna selección en los campos de la esquina superior izquierda hacia abajo, ya que estos campos tienen la misma dimensión tanto en las filas como en las columnas.  
>   
>  La opción seleccionada no será visible hasta que no salga del campo.  
>   
>  Para mostrar el nombre de la dimensión en lugar del código, seleccione el campo **Muestra nombre columna**.

### <a name="to-set-up-global-and-shortcut-dimensions"></a>Para configurar dimensiones globales y abreviadas
Las dimensiones globales y abreviadas se pueden utilizar como filtros en cualquier parte de [!INCLUDE[prod_short](includes/prod_short.md)], incluyendo en informes, trabajos por lotes, páginas de movimientos y vistas de análisis. Las dimensiones globales y abreviadas están siempre disponibles para ser insertadas directamente sin tener que abrir primero la página **Dimensiones**. En las líneas de diario y de documento, puede seleccionar dimensiones globales y abreviadas en un campo de la línea. Puede configurar dos dimensiones globales y ocho abreviadas. Elija las dimensiones que utiliza con más frecuencia.

> [!Important]  
> La modificación de una dimensión global o abreviada requiere que se actualicen todos los movimientos registrados con la dimensión. Para cambiar una dimensión global, use la función **Cambiar dimen. globales**, pero puede llevar mucho tiempo y puede afectar al rendimiento y a las tablas que pueden estar bloqueadas durante la actualización. Por lo tanto, elija cuidadosamente sus dimensiones globales y abreviadas para no tener que cambiarlas más tarde. Para cambiar una dimensión de acceso directo, utilice la acción **Cambiar dimensiones**. <br /><br />
> Para obtener más información, consulte [Para cambiar dimensiones globales](finance-dimensions.md#to-change-global-dimensions).

> [!Note]
> Al añadir o cambiar una dimensión global o abreviada, se cierra automáticamente la sesión y se vuelve a iniciar para que el nuevo valor esté preparado para su uso.

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), introduzca **Configuración de contabilidad** y luego elija el enlace relacionado.
2. En la ficha desplegable **Dimensiones**, rellene los campos. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

#### <a name="to-change-global-dimensions"></a>Para cambiar las dimensiones globales
Al cambiar una dimensión global o abreviada, se actualizan todos los movimientos registrados con la dimensión en cuestión. Debido a que este proceso puede llevar mucho tiempo y afectar al rendimiento, se proporcionan dos modos diferentes de adaptar el proceso al tamaño de la base de datos.  

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Configuración de contabilidad** y luego elija el enlace relacionado.
2. Elija la acción **Cambiar dimensiones globales**.
3. En la parte superior de la página, seleccione una de las siguientes opciones para definir en qué modo se ejecuta el trabajo por lotes.

    |Opción|Descripción|
    |-|-|
    |**Secuencial**|(Predeterminado) Todo el cambio de dimensión se realiza en una transacción que revierte todos los movimientos a las dimensiones que tenían antes del cambio.<br /><br />Se recomienda esta opción si la empresa contiene relativamente pocos movimientos registrados donde se tardará el menor tiempo posible en completarse. El proceso bloquea varias tablas y bloquea a otros usuarios hasta que se realice. Tenga en cuenta que en bases de datos grandes, es posible que el proceso no pueda completarse en este modo. En ese caso, use la opción **En paralelo**.|
    |**En paralelo**|El cambio de dimensión ocurre en múltiples sesiones en segundo plano y la operación se divide en múltiples transacciones. Para usar esta opción, active el control de alternancia **Procesamiento en paralelo**. <br /><br />Recomiendamos esta opción para bases de datos grandes o empresas con muchos movimientos registrados porque se tardará el menor tiempo posible en completarse. Tenga en cuenta que, con este modo, el proceso de actualización no se iniciará si hay más de una sesión de base de datos activa.|  

4. En los campos **Cód. dimensión global 1** o **Cód. dimensión global 2**, escriba las nuevas dimensiones. Las dimensiones actuales se muestran en gris detrás de los campos.
5. Según el modo, realice una de las siguientes acciones:
    * En el modo **Secuencial**, elija la acción **Iniciar**.
    * En el modo **Paralelo**, elija la acción **Preparar**.

    La pestaña **Movs. reg.** se rellena con información acerca de las dimensiones que se cambiarán.
7. Cierre la sesión de [!INCLUDE[prod_short](includes/prod_short.md)] y luego vuelve a iniciar sesión.
8. Elija la acción **Iniciar** para iniciar el procesamiento en paralelo de los cambios de dimensión. <!--is this also dependent on the mode?-->

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
>   Para configurar una jerarquía, los códigos deben estar en orden alfabético. Esto incluye los códigos de los valores de dimensión que se proporcionan en [!INCLUDE[prod_short](includes/prod_short.md)].  

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

En una página de movimiento de contabilidad, puede ver si hay dimensiones globales para los movimientos. Las dos dimensiones globales difieren del resto de las dimensiones porque se pueden utilizar como filtros en cualquier lugar de [!INCLUDE[prod_short](includes/prod_short.md)].  

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
|Valor de dimensión eliminada|    Falta %1 para %2.|-Restaure el valor de dimensión que falta.<br />-Busque documentos no registrados que contengan el grupo de dimensiones con el valor de dimensión que falta y agréguela.<br />-Elimine el grupo de dimensiones para el valor de dimensión que falta.|
|Valor de dimensión no permitido|El tipo de valor de dimensión para %1 %2 - %3 no puede ser %4.|-Cambie el campo **Tipo valor dimensión** en la página **Valores de dimensión** a **Estándar** o **Principio-Total**.<br />-Elimine el grupo de dimensiones para el valor de dimensión bloqueada.|
|Combinación de dimensiones bloqueadas|Las dimensiones %1 y %2 no pueden usarse simultáneamente.|-Busque documentos no registrados que contengan el grupo de dimensiones con la combinación de dimensiones bloqueadas y desbloquéela.<br />-Modifique una de las líneas del conjunto de permisos en conflicto para la combinación de dimensiones.|
|Combinación de valores de dimensiones bloqueadas|Las combinaciones de dimensiones %1 - %2 y %3 - %4 no pueden utilizarse simultáneamente.|-Busque documentos no registrados que contengan el grupo de dimensiones con la combinación de valores de dimensiones bloqueadas y desbloquéela.<br />-Modifique una de las líneas del conjunto de permisos en conflicto para la combinación de valores de dimensiones.|
|Código de valor de dimensión en blanco para la dimensión predeterminada cuando el campo **Registro valor** contiene **Código Obligatorio**|- Seleccione un %1 para el %2 %3.<br />- Seleccione un %1 para el %2 %3 para %4 %5.|-Cambie el campo **Registro valor** en la página **Dimensión predeterminada**.<br />-Introduzca un valor de dimensión no vacío para la dimensión en conflicto en el grupo de dimensiones.|
|Código de valor de dimensión erróneo para la dimensión predeterminada cuando el campo **Registro valor** contiene **Igual código**|- Seleccione %1 %2 para el %3 %4.<br />- Seleccione %1 %2 para el %3 %4 para %5 %6.|-Cambie el campo **Registro valor** en la página **Dimensión predeterminada**.<br />-Introduzca un valor de dimensión requerido para la dimensión en conflicto en el grupo de dimensiones.|
|Código de valor de dimensión no vacío para la dimensión predeterminada en blanco cuando el campo **Registro valor** contiene **Igual código**|-%1 %2 debe estar en blanco.<br />-%1 %2 debe estar en blanco para %3 %4.|-Cambie el campo **Registro valor** en la página **Dimensión predeterminada**.<br />-Introduzca un código de valor de dimensión en blanco para la dimensión en conflicto en el grupo de dimensiones.|
|Valor de dimensión inesperado para la dimensión predeterminada cuando el campo **Registro valor** contiene **Sin código**|-%1 %2 no debe ser mencionado.<br />-%1 %2 no debe ser mencionado para %3 %4|-Cambie el campo **Registro valor** en la página **Dimensión predeterminada**.<br />-Elimine la línea conflictiva del grupo de dimensiones.|
|Una corrección de dimensión no se completa correctamente.||-Elija **Restablecer** para revertir la corrección a un estado de borrador. Esto restablece los cambios y puede ejecutar de nuevo la corrección.|

## <a name="changing-dimension-assignments-after-posting"></a>Cambio de asignaciones de dimensión después del registro
Si descubre que se ha usado una dimensión incorrecta en los movimientos de contabilidad, puede corregir los valores de dimensión y actualizar sus vistas de análisis. Eso ayudará a que sus informes y análisis financieros sean precisos.

### <a name="setting-up-dimension-corrections"></a>Configuración de correcciones de dimensión
Hay dos cosas a tener en cuenta al configurar correcciones de dimensión:

* ¿Hay dimensiones que no desea que la gente cambie? En la página **Configuración de corrección de dimensión**, especifique las dimensiones que desea bloquear para cambios.
* ¿A quién quiere permitir que cambie de dimensión? Para permitir que las personas realicen cambios, asigne el permiso **CORRECCIÓN DIM. D365** a los usuarios. Los permisos les permiten crear correcciones de dimensión, ejecutarlas y deshacerlas si es necesario. También podrán especificar dimensiones bloqueadas. Para obtener más información, vea [Asignar permisos a usuarios y grupos](ui-define-granular-permissions.md). 

### <a name="correcting-a-dimension"></a>Corrección de una dimensión
Puede seleccionar manualmente uno o varios movimientos de contabilidad o usar filtros para seleccionar conjuntos de movimientos. Si es necesario, también puede agregar o eliminar dimensiones. 

1. Para iniciar una corrección de dimensión, use una de las siguientes páginas:

* En la página **Registro contabilidad**, seleccionando un registro y luego eligiendo la acción **Corregir dimensiones**. Esto inicia una corrección para los movimientos en el registro seleccionado.
* En la página **Movs. contabilidad**, eligiendo la acción **Corrección de dimensión**. 

2. En el campo **Descripción**, introduzca cualquier información sobre el cambio. Otras personas pueden usar esta información más adelante para comprender lo que se hizo.
3. En la ficha desplegable **Movimientos seleccionados**, elija los movimientos pertinentes.

> [!IMPORTANT]
> Cuando cambia una selección, se restablecen los valores de la ficha desplegable **Cambios de corrección de dimensión**. Por lo tanto, seleccione siempre los movimientos antes de especificar cambios en el valor de dimensión.

   La siguiente tabla describe las opciones.

   |Opción  |Descripción  |
   |---------|---------|
   |Agregar movimientos relacionados     |Agregue movimientos contables que estén en el mismo registro de movimientos de contabilidad.|   
   |Agregar por filtro     |Use criterios de filtros cuando agregue movimientos de contabilidad.|
   |Selección manual     |Seleccione movimientos de contabilidad específicos.         |
   |Agregar por dimensiones     |Filtre movimientos de contabilidad por dimensiones.         |
   |Quitar movimientos     |Anule la selección de movimientos de contabilidad.         |
   |Administrar criterios de selección     |Realice un seguimiento del proceso de selección y deshaga las selecciones si es necesario.         |

4. En la ficha desplegable **Cambios de corrección de dimensión**, elija la dimensión que desea cambiar en el campo **Código de dimensión** y el nuevo valor en el campo **Nuevo código de valor de dimensión**.
5. Para validar la corrección, elija **Validar cambios de dimensión**. Para obtener más información, consulte [Validación de correcciones de dimensión](finance-dimensions.md#validating-dimension-corrections).
6. Elija **Ejecutar**.

### <a name="validating-dimension-corrections"></a>Validación de correcciones de dimensión
Antes de ejecutar una corrección, es una buena idea validarla primero. La validación comprueba las restricciones sobre el valor al registrar para las cuentas de contabilidad, las restricciones para las dimensiones y si los valores de las dimensiones están bloqueados. Durante la validación, el estado de la corrección se establece en **Validación en proceso**. Después de validar una corrección, el resultado se muestra en el campo **Estado de validación**. Si se encontraron errores, puede usar la acción **Ver errores** para investigarlos. Después de corregir un error, debe usar la acción **Reabrir** para ejecutar la corrección o una nueva validación.

Puede ejecutar una corrección inmediatamente o programarla para que se ejecute más adelante. Si está ejecutando correcciones en un conjunto de datos grande, le recomendamos que lo programe para que se ejecute fuera del horario comercial. Para obtener más información, consulte [Correcciones de dimensión en grandes conjuntos de datos](finance-dimensions.md#dimension-corrections-on-large-data-sets).

### <a name="undoing-a-correction"></a>Deshacer una corrección
Después de corregir una dimensión, si no le gusta lo que ve, puede usar la acción **Deshacer** para restablecer el valor anterior. Sin embargo, solo puede deshacer la corrección más reciente. Antes de deshacer una corrección, puede validar los cambios que hará la anulación. Por ejemplo, esto resulta útil si las restricciones de dimensión han cambiado después de que se realizase la corrección.

Si la acción Deshacer no está disponible, por ejemplo, porque ha realizado muchas correcciones, puede usar la acción **Copiar a borrador** para iniciar una nueva corrección para las mismas entradas.

### <a name="dimension-corrections-on-large-data-sets"></a>Correcciones de dimensión en grandes conjuntos de datos
Tenga cuidado al corregir grandes conjuntos de entradas, por ejemplo, conjuntos que incluyan más de 10 000 entradas. Si puede, le recomendamos que use los filtros para ejecutar las correcciones en conjuntos de datos más pequeños. También es una buena idea realizar correcciones fuera del horario comercial habitual. 

### <a name="using-analysis-views-with-dimension-corrections"></a>Usar vistas de análisis con correcciones de dimensión
Si **Actualizar al registrar** está habilitado para una vista de análisis, [!INCLUDE[prod_short](includes/prod_short.md)] puede ver cuándo se registran los documentos y diarios. También puede actualizar las vistas con esta configuración habilitada con los resultados de las correcciones de dimensión. Para ello, active el control de alternancia **Actualizar vistas de análisis**. La actualización de las vistas de análisis puede afectar al rendimiento, especialmente para grandes conjuntos de datos, por lo que le recomendamos que actualice las vistas de análisis solo para conjuntos de datos pequeños.  

### <a name="viewing-historical-dimension-corrections"></a>Visualización de correcciones de dimensión históricas
Si se ha corregido un movimiento de contabilidad, puede investigar el cambio usando la acción **Historial de correcciones de dimensión**.

### <a name="handling-incomplete-corrections"></a>Gestión de correcciones incompletas
Si una corrección no se completa, aparecerá una advertencia en la ficha de corrección. Si eso sucede, puede usar la acción **Restablecer** para revertir la corrección a un estado de borrador y deshacer los cambios. A continuación, puede volver a ejecutar la corrección.

> [!NOTE]
> Restablecer una corrección incompleta no afectará a las actualizaciones de las vistas de análisis porque se producen al final del proceso de corrección.

### <a name="using-cost-accounting-with-corrected-gl-entries"></a>Usar la contabilidad de costes con movimientos de contabilidad corregidos
Después de corregir las dimensiones, sus datos para la contabilidad de costes no estarán sincronizados. La contabilidad de costes usa dimensiones para agregar cantidades para centros de coste y objetos de coste, y para ejecutar asignaciones de costes. Cambiar las dimensiones para movimientos de contabilidad probablemente signifique volver a ejecutar sus modelos de contabilidad de costes. Si solo necesita eliminar algunos registros de costes y volver a ejecutar asignaciones, o si necesita eliminar todo y volver a ejecutar todos sus modelos, depende de los datos que se hayan actualizado y de cómo estén configuradas sus capacidades de contabilidad de costes. Identificar dónde afectarán las correcciones de dimensión a la contabilidad de costes y dónde se necesitan actualizaciones es un proceso manual. [!INCLUDE[prod_short](includes/prod_short.md)] no ofrece actualmente una forma automatizada de hacerlo.  

## <a name="see-related-training-at-microsoft-learn"></a>Consulte Formación relacionada en [Microsoft Learn](/learn/modules/dimensions-dynamics-365-business-central/index)

## <a name="see-also"></a>Consulte también
[Inteligencia empresarial](bi.md)  
[Finanzas](finance.md)  
[Analizar datos por dimensiones](bi-how-analyze-data-dimension.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]