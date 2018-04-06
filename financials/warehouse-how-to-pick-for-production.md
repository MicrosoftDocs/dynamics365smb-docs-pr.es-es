---
title: "Cómo realizar el picking para la producción en configuraciones básicas de almacén | Microsoft Docs"
description: "Cuando el almacén requiere el proceso de picking, pero no el proceso de envío, utilice la ventana **Picking inventario** para organizar y registrar el picking de componentes."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 68702e384ea750535a8d7e5b83ee619856b6a34b
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="pick-for-production-or-assembly"></a>Selección de producción o la Lista montaje
La forma de ubicar el picking de componentes para fabricación u órdenes de ensamblado depende de la configuración del almacén. Para obtener más información, consulte [Configuración de la administración de almacén](warehouse-setup-warehouse.md).

En configuraciones de almacén básico en las que se requiere el proceso de picking, pero no el de envío, utilice el documento **Picking inventario** para organizar y registrar el picking de componentes.  

En configuraciones básicas de almacén, debe realizar el picking para las órdenes de ensamblado con la ventana **Movimiento inventario**. Para obtener más información, vea la sección "Tratamiento de productos ensamblar para pedido en los picking de inventario" en [Realizar picking de productos con picking inventario](warehouse-how-to-pick-items-with-inventory-picks.md).  

En configuraciones avanzadas de almacén, donde las ubicaciones requieren tanto picking como envíos, utilice la ventana **Picking de almacén** para llevar los componentes a las órdenes de producción o de ensamblado.

> [!NOTE]  
>  Los picking de inventario y los movimientos de inventario tienen las siguientes diferencias importantes:  
>   
>  -   Cuando registra un picking de inventario para una operación interna, como la producción, el consumo de los componentes seleccionados se registra al mismo tiempo. Cuando registra un movimiento de inventario para una operación interna, se registra únicamente el movimiento físico de los componentes necesarios en una ubicación del área de operación, sin registrar el consumo.  
> -   Cuando se utiliza el picking de inventario, el campo **Cód. ubicación** de la línea de componente de orden de producción define la ubicación *traer* desde donde los componentes disminuyen cuando se registra el consumo. Al utilizar movimientos de inventario, el campo **Código de ubicación** en las líneas de componente de orden de producción define la ubicación *apartado* en el área de la operación donde el empleado de almacén debe colocar los componentes.  

Una condición previa del sistema para picking o traslado de componentes para los documentos de origen es que una solicitud de salida de almacén exista para notificar al área de almacén de la necesidad de componentes. La solicitud de salida de almacén se crea siempre que se cambia el estado de la orden de producción a Lanzada o cuando se crea una orden de producción lanzada.  

## <a name="to-pick-components-in-basic-warehouse-configurations"></a>Para realizar el picking de componentes en configuraciones básicas de almacén
En configuraciones básicas de almacén en donde se configura la ubicación para utilizar picking, podrá escoger los componentes para las actividades de producción con la ventana de **Picking inventario**. Para obtener más información, vea [Realizar picking de productos con picking inventario](warehouse-how-to-pick-items-with-inventory-picks.md).

1.  Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Picking inventario** y, a continuación, seleccione el vínculo relacionado.  
2.  Para tener acceso a los componentes de la orden de producción, elija la acción **Traer doc. origen** y, a continuación, seleccione la orden de producción lanzada.  
3.  realice el picking y, a continuación, registre la información de picking real en el campo **Cdad. preparada pedido**.  
4.  Cuando las líneas estén preparadas para registrar, elija la acción **Registrar**. El registro crea los movimientos de almacén necesarios y registra el consumo de los productos.  

También puede crear **Picking existencias** directamente de la orden de producción lanzada. Seleccione la acción **Crear ubicac./ pick. existencias**, seleccione la casilla **Crear pick exist.** y, a continuación, seleccione el botón **Aceptar**.

También podrá utilizar la ventana **Movimiento inventario** para mover los artículos entre las ubicaciones ad hoc (es decir, sin referencia a un documento de origen).
Para obtener más información, consulte [Mover componentes a un área de operaciones en las configuraciones básicas de almacén](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md).

### <a name="handling-assemble-to-order-items-with-inventory-picks"></a>Tratamiento de productos de ensamblar para pedido con los picking de inventario
La ventana **Picking de inventario** también se utiliza para realizar el picking y envíos para ventas cuando los productos se deben ensamblar antes de que se puedan enviar. Para obtener más información, consulte [Venta de artículos ensamblados para pedido](assembly-how-to-sell-items-assembled-to-order.md).

Los productos que se van a enviar no están presentes físicamente en una ubicación hasta que se ensamblan y se registran como salida en una ubicación de la zona de ensamblado. Esto significa que realizar el picking de productos ensamblar para pedido para el envío sigue un flujo especial. De una ubicación, los empleados del almacén toman los productos de ensamblado al muelle de envío y después registran el picking de inventario. El picking de inventario registrado registra a continuación la salida de ensamblado, el consumo de componentes y el albarán de venta.

Puede configurar [!INCLUDE[d365fin](includes/d365fin_md.md)] para que cree automáticamente un movimiento de inventario cuando el picking de inventario para el producto del ensamblado se crea. Para habilitarlo, debe seleccionar el campo **Crear movimientos automáticamente** en la ventana **Conf. ensamblado**. Para obtener más información, consulte [Mover componentes a un área de operaciones en el almacenamiento básico](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md).

Las líneas de picking de existencias se crean de diferentes modos en función de que no se ensamble ninguna, alguna o toda la cantidad de línea de venta para pedido.

En ventas normales en las que se utiliza el picking de inventario para registrar el envío de cantidades de inventario, para cada línea de pedido de venta se crea una línea de picking de inventario, o varias si el producto se coloca en ubicaciones diferentes. Esta línea de picking se basa en la cantidad en el campo **Cantidad a enviar**.

De las ventas de ensamblar para pedido cuya cantidad total de la línea de pedido de venta se ensambla para pedido, una línea de picking de inventario se crea para esa cantidad. Esto significa que el valor del campo Cantidad a ensamblar es igual al valor del campo **Cdad. a enviar**. El campo **Ensamblar para pedido** está seleccionada en la línea.

Si un flujo de salida de ensamblado está configurado para el almacén, el valor del campo **Cód. ubic. ens.contra-pedido** o el valor en el campo **Cód. ubic. desde ensamblado**, en ese orden, se inserta en el campo **Cód. ubicación** de la línea de picking de inventario.

Si no se especifica ningún código de ubicación de la línea de pedido de venta, y no se configura ningún flujo de salida de ensamblado para el almacén, el campo **Cód. ubicación** de la línea de picking de inventario está vacío. El empleado del almacén debe abrir la ventana **Contenidos ubicación** y seleccionar el almacén donde se ensamblan los productos de ensamblado.

En escenarios de combinación, donde parte de la cantidad debe ensamblarse primero y a la otra se le debe realizar el picking de inventario, un mínimo de dos líneas de picking de inventario se crea. Una línea de picking es para la cantidad de ensamblado para pedido. La otra línea de picking depende de qué ubicación pueden cubrir la cantidad pendiente de inventario. Los códigos de ubicación en las dos líneas se completan de formas distintas según se describe para los dos tipos de venta respectivamente. Para obtener más información, consulte la sección "Escenarios de combinación" en [Comprender Ensamblar para pedido y Ensamblar para stock](assembly-assemble-to-order-or-assemble-to-stock.md).

## <a name="to-pick-components-in-advanced-warehouse-configurations"></a>Para realizar el picking de componentes en configuraciones avanzadas de almacén
En la configuración avanzada de almacén en donde se configura la ubicación para utilizar picking y envío, podrá escoger los componentes para las actividades de producción y de ensamblado con la ventana de **Picking almacén**. Para obtener más información, vea [Realizar picking de productos con picking almacén](warehouse-how-to-pick-items-for-warehouse-shipment.md).

También podrá utilizar la ventana **Hoja trabajo movimiento** para mover los artículos entre las ubicaciones ad hoc (es decir, sin referencia a un documento de origen). Para obtener más información, consulte [Mover los artículos en las configuraciones avanzadas de almacén](warehouse-how-to-move-items-in-advanced-warehousing.md).  

No se puede crear un documento de picking de almacén desde cero porque una actividad de picking siempre forma parte de un flujo de trabajo, tanto en un escenario de extracción como de inserción.  

Puede crear el documento de picking de almacén mediante inserción seleccionando la acción **Crear picking almacén** en el documento de origen, como un pedido de ensamblado enviado o un envío de almacén. Para obtener más información, vea [Realizar picking de productos con picking almacén](warehouse-how-to-pick-items-for-warehouse-shipment.md).  

Alternativamente, puede crear el documento de picking de almacén de forma de la extracción utilizando la ventana **Preparar hoj. trab. pedido** para detectar pedidos de picking, tanto para envío y como para operaciones internas y, a continuación crear los documentos de picking de almacén necesarios.  

El procedimiento siguiente explica un escenario de envío en donde se va a realizar el picking de los componentes para un orden de producción lanzada a través de la ventana **Hojas trabajo picking**. El procedimiento también se aplica a pedidos de ensamblado.  

Para crear pedidos de picking, para escenarios de extracción y de empuje, deben lanzarse los documentos de origen en cuestión. Lance los documentos de origen para las operaciones internas de las siguientes formas.  

 |Documento origen|Método de lanzamiento|  
 |---------------------|--------------------|  
 |Orden producción|Cambie el tipo de pedido a orden de producción lanzada.|  
 |Pedido de ensamblado|Cambie el estado a Lanzada.|  

## <a name="to-pick-components-using-the-pick-worksheet"></a>Para realizar el picking de componentes desde la hoja de trabajo de picking  

1.  Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Hoja trabajo picking** y, a continuación, seleccione el vínculo relacionado.  
2.  Elija la acción **Documentos almacén** y seleccione las líneas de componente del pedido de producción lanzado.  
3.  Explore las líneas, ordénelas para asegurar un picking más eficaz y combínelas con otras líneas de hoja de trabajo si es necesario para ahorrar tiempo a los empleados.  
4.  Elija la acción **Crear picking**.  
5.  Defina cómo crear los documentos de picking de almacén y cómo ordenar las líneas de picking rellenando los campos de la ventana **Crear picking**.  
6.  Elija el botón **Aceptar**.

Los documentos de picking de almacén ahora se crean con las líneas de picking para cada componente necesario en la operación interna.

Si el área de operaciones internas, como un suelo de departamento de producción, se ha configurado con una ubicación predeterminada para la colocación de los componentes utilizados en la operación,ese código de ubicación se insertará en las líneas del lugar en el documento de picking de almacén para indicar a los trabajadores del almacén dónde ubicar los artículos. Para obtener más información, consulte [Configurar almacenes básicos con áreas de operaciones](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md).

## <a name="filling-the-consumption-bin"></a>Rellenando la ubicación del consumo
Este organigrama muestra cómo se rellena el campo de **Código de ubicación** en las líneas del componente de la orden de producción según la ubicación.

![Gráfico de flujo de ubicación](media/binflow.png "BinFlow")

## <a name="see-also"></a>Consulte también
[Gestión almacén](warehouse-manage-warehouse.md)  
[Grupos contables inventario](inventory-manage-inventory.md)  
[Configuración de la gestión del almacén](warehouse-setup-warehouse.md)     
[Gestión de ensamblaje](assembly-assemble-items.md)    
[Detalles de diseño: Gestión de almacén](design-details-warehouse-management.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

