---
title: "Procedimiento: haga tránsito directo de artículos | Documentos de Microsoft"
description: "La funcionalidad de tránsito directo está disponible si ha configurado el almacén para requerir el proceso de recepción y ubicación."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/23/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 25dd4bf914a4bf971e329b48fddac03f7536b00f
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="cross-dock-items"></a>Productos de tránsito directo
La funcionalidad de tránsito directo está disponible si ha configurado el almacén para requerir el proceso de recepción y ubicación.  

Al realizar el tránsito directo de productos, usted procesa productos en la recepción y el envío sin colocarlos en el almacén, simplificando, así, la gestión del producto a través de los procesos de ubicación y picking y limitando la manipulación física de los productos. Puede realizar el tránsito directo de productos para los envíos y las órdenes de producción. Cuando se prepara un envío o se realiza un picking de productos para producción y utiliza ubicaciones, se realizará el picking del producto automáticamente desde una ubicación de tránsito directo antes de considerar el picking desde cualquier otra ubicación. Debe comprobar si los productos que necesita están disponibles en el área tránsito directo antes de traerlos a su área de almacenamiento habitual.  

Si ha calculado cantidades de tránsito directo, las líneas de ubicación a la ubicación de tránsito directo para los cálculos de tránsito directo se crean al registrar la recepción. Las otras líneas de ubicación se crean normalmente.  

Si desea registrar los productos de tránsito directo directamente, para hacerlos disponibles para picking, registre también una ubicación para el resto de productos que se originan desde las líneas de recepción, es decir, los que se tienen que almacenar. Si sólo se va a realizar el tránsito directo de algunos productos de la línea de recepción, debe hacer el esfuerzo de ubicar el resto de los productos tan pronto como sea posible. Alternativamente, su política de almacén podría impulsar el tránsito directo de líneas de recepción completas siempre que sea posible.  

En la instrucción de ubicación, puede aprovecharse de eliminar líneas de instrucción Traer y Colocar para cada línea de recepción que estén relacionadas con las recepciones que se van a ubicar completamente en el almacén. Posteriormente, estas líneas se pueden crear como líneas de ubicación desde la hoja de trabajo de ubicación o la recepción registrada. Cuando se eliminan, puede ubicar y registrar las líneas que están relacionadas con los productos en tránsito directo.  

Si ha seleccionado el campo **Utiliza hoj. trab. ubicación** de la ficha de almacén y ha registrado la recepción con tránsitos directos calculados, todas las líneas de la recepción están disponibles en la hoja de trabajo. La información de tránsito directo se pierde y no puede volver a crearse. Por tanto, si desea utilizar la funcionalidad de tránsito directo, debe pasar las líneas a la hoja de trabajo de ubicación eliminando las instrucciones de ubicación en vez de utilizar la función de paso automático que proporciona el campo **Utiliza hoj. trab. ubicación**.  

Si registra la recepción de almacén y no ha seleccionado el campo **Utiliza hoj. trab. ubicación**, los productos de los que se va a realizar el tránsito directo aparecen como líneas independientes en la instrucción de ubicación. El campo **Información tránsito directo** de cada línea de ubicación muestra si la línea contiene productos de tránsito directo, productos de la misma recepción que se tienen que almacenar o productos que se tienen que almacenar que provienen de una línea de recepción donde se va a realizar el tránsito directo de algunos productos. Con este campo, los empleados pueden ver fácilmente por qué no se ha colocado en el almacén toda la cantidad recibida.  

El programa no mantiene registros independientes de los productos de los que se ha realizado el tránsito directo, si no que los registra como instrucciones de ubicación normales.  

## <a name="to-set-up-the-warehouse-for-cross-docking"></a>Para configurar el almacén para tránsito directo  
1.  Si utiliza ubicaciones configure al menos una ubicación de tránsito directo. Si utiliza ubicación y picking directos configure una zona de tránsito directo.  

    Una ubicación de tránsito directo tiene el campo de **Ubicación tránsito directo** seleccionado y debe tener seleccionadas las ubicaciones **Recepción** y **Picking**. Para obtener más información, consulte [Crear ubicaciones](warehouse-how-to-create-individual-bins.md) y [Configurar tipos de ubicación](warehouse-how-to-set-up-bin-types.md).  

    Si utiliza zonas, cree una para sus ubicaciones de tránsito directo y seleccione el campo **Zona ubicac. tráns. directo**. Para obtener más información, consulte [Configure lugares para utilizar las ubicaciones](warehouse-how-to-set-up-locations-to-use-bins.md).  

2.  Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Almacén** y, a continuación, seleccione el vínculo relacionado.  
3.  En la ventana **Ubicación**, seleccione la ubicación cuyo tránsito directo del almacén desee configurar y, a continuación, elija la acción **Editar**.  
4.  En la ficha desplegable **Almacén**, seleccione la casilla **Utilizar tránsito directo** y rellene al campo **Calcular fecha vto. tráns. directo** con el periodo de tiempo que el sistema anticipará la búsqueda de oportunidades de tránsito directo.

    La opción **Utiliza tránsito directo** sólo está disponible si ha seleccionado los campos **Recepción requerida**, **Envío requerido**, **Picking requerido** y **Ubicación requerida**.  

5.  Si utiliza ubicaciones, en la ficha desplegable **Zonas y Ubic.**, rellene el campo **Cód. ubicac. tránsito directo** con el código de la ubicación que desea utilizar como ubicación de tránsito directo genérica.  
6.  Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Unidad de almacenam.** y seleccione el vínculo relacionado.  
7.  Para cada artículo o unidad de almacenamiento donde desea que se pueda realizar el tránsito directo, seleccione el artículo y, a continuación, elija la acción **Editar**.
8. En la ventana **Ficha ud. de almacenam.**, active la casilla **Utilizar tránsito directo**.  

> [!NOTE]  
>  La funcionalidad de tránsito directo sólo es posible si el almacén está configurado para requerir los procesos de recepción y ubicación.  

## <a name="to-cross-dock-items-without-viewing-the-opportunities"></a>Para realizar el tránsito directo de productos sin ver las oportunidades  
1.  Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Recepciones almacén** y, a continuación, seleccione el vínculo relacionado.  
2.  Cree las recepciones de un almacén para un artículo que ha llegado y pueda probablemente tener tránsito directo. Para obtener más información, consulte [Recibir productos](warehouse-how-receive-items.md).  
3.  Rellene el campo **Cdad. para recibir** y, a continuación, elija la acción **Calcular tránsito directo**.  

    Se identifican los documentos de origen de salida que solicitan los productos que están programados para salir del almacén en el periodo de tiempo de la fórmula de fecha.  [!INCLUDE[d365fin](includes/d365fin_md.md)] calcula las cantidades para que pueda realizar el tránsito directo en cuanto sea posible y evitar tener que ubicar los productos sin que se amontonen demasiados en el área de tránsito directo. El valor del campo **Cdad. a tránsito directo** fes la suma de todas las líneas de salida que solicitan el producto en el periodo anticipado menos la cantidad de productos que ya se han colocado en el área de tránsito directo, o es el valor del campo **Cantidad a recibir** de la línea de la recepción, que siempre es menor. No puede realizar el tránsito directo de más productos de los que ha recibido.  

4.  Si desea hacer el tránsito directo de la cantidad sugerida registre la recepción. También es posible que decida cambiar la cantidad de la que se va a hacer el tránsito directo y, a continuación, registrar la recepción.  

    Los importes de los que se va a realizar el tránsito directo aparecen como líneas en la instrucción de ubicación, asumiendo que el campo **Utiliza hoj. trab. ubicación** esté desactivado. Las cantidades que no entran en tránsito directo se convierten en líneas en la instrucción de ubicación.  

    Si tiene ubicaciones, los productos de tránsito directo se habrán asignado a la ubicación de tránsito directo genérica definida en la ficha de almacén.  

5.  Elimine las líneas **Traer** y **Colocar** de los productos de los que no se va a realizar el tránsito directo.  
6.  Imprima la instrucción de ubicación del resto de las líneas y coloque las cantidades de la recepción que se tienen que almacenar en las ubicaciones o el área de almacén adecuada. Coloque los productos de tránsito directo en el área o la ubicación diseñada para ellos en la política de almacén. A veces, es posible que la política de almacén le requiera dejarlos en el área de recepción.  
7.  Para registrar los productos de tránsito directo que se van a ubicar y hacer disponible para picking, elija la acción **Registrar**.  

## <a name="to-cross-dock-items-after-viewing-the-opportunities"></a>Para realizar el tránsito directo de productos después de ver las oportunidades  
1.  Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Recepciones almacén** y, a continuación, seleccione el vínculo relacionado.  
2.  Cree las recepciones de un almacén para un artículo que ha llegado y pueda probablemente tener tránsito directo. Para obtener más información, consulte [Recibir productos](warehouse-how-receive-items.md).  

    Debe ver las líneas del documento de origen que solicitan el artículo para poder registrar la recepción.  
3.  Elija la acción **Calcular tránsito directo**.  

    En la ventana **Oportunidad tráns.direc.** puede ver los detalles más importantes de las líneas que solicitan el producto, como el tipo de documento, la cantidad solicitada y la fecha de vencimiento. Esta información puede ayudarle a decidir la cantidad de producto de tránsito directo, dónde colocar los productos en el área de tránsito directo o cómo agruparlos.  

4.  Elija la acción **Rellenar cdad. manipulada autom.** para ver cómo se calculan las cantidades en las líneas de la recepción. Cuando se modifica el número de artículos en el campo **Cdad. en tránsito directo** en cada línea, se actualiza el cálculo mientras se realizan los cambios. Esto no significa que la recepción o la orden de producción determinada reciban realmente los productos sugeridos para tránsito directo, porque estas manipulaciones sólo sirven como pruebas. No obstante, el proceso puede ser informativo si está implicada más de una unidad de medida.  
5.  Si desea reservar una cantidad de producto para una línea de pedido determinada, coloque el cursor en esa línea y, a continuación, elija la acción **Reservar**. En la ventana de **Reserva**, ahora puede reservar cualquier cantidad disponible del artículo para este pedido específico. Esta reserva es como cualquier otra, y no tiene mayor prioridad porque se haya creado junto con el tránsito directo. Para obtener más información, consulte [Reservar productos](inventory-how-to-reserve-items.md).   
6.  Al terminar el cálculo o la reserva, seleccione **Aceptar** para traer los cálculos según los ha revisado al campo **Cdad. a tránsito directo** de la línea de la recepción, o seleccione **Cancelar** si desea volver a la recepción de almacén, donde puede calcular de nuevo el tránsito directo.  
7.  Ahora registre la recepción, y puede continuar en las instrucciones de ubicación tal como se describe en los pasos 3 a 7 en la sección “A los artículos de tránsito directo sin consultar la sección de las oportunidades”.  

> [!NOTE]  
>  En la ubicación de almacén, puede continuar cambiando las cantidades que se van a ubicar en el almacén o de las que se va a realizar el tránsito directo, según sea necesario. Por ejemplo, es posible que decida realizar un tránsito directo de una cantidad adicional para simplificar el registro de tránsito directo.  

## <a name="to-view-cross-docked-items-in-a-shipment-or-pick-worksheet"></a>Para ver productos de tránsito directo en un envío u hoja de trabajo de picking  
Si utiliza ubicaciones, puede ver, cada vez que abra un envío o una hoja de trabajo de picking, un cálculo actualizado de la cantidad de cada producto en las ubicaciones de tránsito directo. Esta es una información valiosa si espera la entrada de un producto. Al ver que el producto está disponible en la ubicación de tránsito directo, puede crear rápidamente un picking de todos los productos del envío. En la hoja de trabajo de picking, puede modificar las líneas que considere y, a continuación, crear un picking.  

Tiene que buscar productos en el área de tránsito directo cuando va a realizar el picking de productos para enviarlos. Si no se ha dado cuenta durante el proceso de recepción de los documentos de origen que eran la base para el tránsito directo, ahora tiene una idea mejor de si se pueden encontrar los productos en el área de tránsito directo.  

Al lanzar una orden de producción, las líneas están disponibles en la hoja de trabajo de picking se pueden ver en el campo **Cdad. en ubic. tráns. directo** si los productos que espera han llegado y se han colocado en las ubicaciones de tránsito directo. Al crear una instrucción de picking, el programa sugiere que primero realice el picking de los productos de tránsito directo y sólo después buscará los productos en las ubicaciones de almacenamiento.  

Si no utiliza ubicaciones, recuerde comprobar el área de tránsito directo de vez en cuando o deberá confiar en las notificaciones de recepción que han llegado productos para producción.  

## <a name="see-also"></a>Consulte también  
[Gestión almacén](warehouse-manage-warehouse.md)  
[Grupos contables inventario](inventory-manage-inventory.md)  
[Configuración de la gestión del almacén](warehouse-setup-warehouse.md)     
[Gestión de ensamblaje](assembly-assemble-items.md)    
[Detalles de diseño: Gestión de almacén](design-details-warehouse-management.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

