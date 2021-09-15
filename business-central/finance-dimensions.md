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
ms.openlocfilehash: 982f61396f1d49eeaa688d580801c14ac9c33ccb
ms.sourcegitcommit: 04055135ff13db551dc74a2467a1f79d2953b8ed
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/08/2021
ms.locfileid: "7482227"
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

> [!NOTE]
> Las vistas de análisis suelen utilizar datos de dimensiones. Si descubre que se ha usado una dimensión incorrecta en los movimientos de contabilidad, puede corregir los valores de dimensión y actualizar sus vistas de análisis. Eso ayudará a que sus informes y análisis financieros sean precisos. Para obtener más información, vea [Solucionar problemas y corregir dimensiones](finance-troubleshooting-correcting-dimensions.md#changing-dimension-assignments-after-posting)

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

> [!NOTE]
> Después de utilizar una nueva dimensión en cualquier entrada, como una línea o un nuevo registro, no puede eliminar la dimensión, incluso si no publica la entrada. Esto es porque [!INCLUDE[prod_short](includes/prod_short.md)] crea inmediatamente un conjunto de dimensiones para la línea o registro. Para obtener más información, vea [Conjuntos de dimensiones](finance-dimensions.md#dimension-sets).

### <a name="to-set-up-default-dimensions-for-customers-vendors-and-other-accounts"></a>Para configurar dimensiones predeterminadas para clientes, proveedores y otras cuentas
Puede asignar una dimensión predeterminada para una determinada cuenta. La dimensión se copiará en el diario o el documento cuando introduzca el número de cuenta en una línea, pero puede eliminar o cambiar el código de la línea si es necesario. También puede convertir una dimensión en obligatoria para registrar un movimiento con un tipo de cuenta específico.  

1.  Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Dimensiones** y luego elija el enlace relacionado.  
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

1.  Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Prioridades de dimensión** y luego elija el enlace relacionado.  
2.  En la página **Prioridades dimensión predet.**, en el campo **Cód. origen**, escriba el código de origen para la tabla de movimientos para la que se aplicarán las prioridades de dimensión predeterminadas.  
3.  Rellene una línea para cada prioridad de dimensión predeterminada que desee para el código de origen seleccionado.
4.  Repita el procedimiento para la cada código de origen para el que quiera configurar prioridades de dimensión predeterminadas.  

> [!IMPORTANT]  
>  Si configura dos tablas con la misma prioridad en un mismo código de origen, [!INCLUDE[prod_short](includes/prod_short.md)] seleccionará siempre la tabla con el Id. de tabla inferior.  

### <a name="to-set-up-dimension-combinations"></a>Para configurar combinaciones de dimensión  
Para evitar registrar movimientos con dimensiones contradictorias o irrelevantes, puede bloquear o limitar determinadas combinaciones de dos dimensiones. Una dimensión está bloqueada si no es posible registrar ambas dimensiones en el mismo movimiento independientemente de los valores de dimensión. Una combinación de dimensión limitada le permite registrar ambas dimensiones en el mismo movimiento, pero únicamente para determinadas combinaciones de valores de dimensión.

1.  Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Combinaciones de dimensiones** y luego elija el enlace relacionado.  
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

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración de contabilidad**, y luego elija el enlace relacionado.
2. En la ficha desplegable **Dimensiones**, rellene los campos. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

#### <a name="to-change-global-dimensions"></a>Para cambiar las dimensiones globales
Al cambiar una dimensión global o abreviada, se actualizan todos los movimientos registrados con la dimensión en cuestión. Debido a que este proceso puede llevar mucho tiempo y afectar al rendimiento, se proporcionan dos modos diferentes de adaptar el proceso al tamaño de la base de datos.  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración de contabilidad**, y luego elija el enlace relacionado.
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

1.  Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Plan de cuentas** y luego elija el enlace relacionado.  
2.  En la página **Plan de cuentas**, seleccione la acción **Movimientos**.  
3.  Para ver únicamente los movimientos relevantes, establezca uno o más filtros en la página.  
4.  Para ver todas las dimensiones de un movimiento, seleccione el movimiento y elija la acción **Dimensiones**.  

> [!NOTE]  
>  La página **Dimensiones movimiento** muestra las dimensiones de un movimiento de contabilidad cada vez. A medida que se desplaza por los movimientos de contabilidad, el contenido de la página **Dimensiones movimiento** va cambiando según corresponda.

## <a name="see-related-training-at-microsoft-learn"></a>Consulte Formación relacionada en [Microsoft Learn](/learn/modules/dimensions-dynamics-365-business-central/index)

## <a name="see-also"></a>Consulte también
[Inteligencia empresarial](bi.md)  
[Finanzas](finance.md)  
[Analizar datos por dimensiones](bi-how-analyze-data-dimension.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]