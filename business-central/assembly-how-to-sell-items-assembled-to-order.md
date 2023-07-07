---
title: Venta de artículos ensamblados para pedido
description: Vea cómo vender un artículo que se ensamble para pedido.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 11/23/2022
ms.search.keywords: 'kit, kitting, substitute items'
ms.search.form: '900, 901, 902, 903, 904, 907, 910, 916, 920, 921, 922, 923, 940, 941, 942, 930, 931, 932, 914, 915, 905'
ms.custom: bap-template
---
# <a name="sell-items-assembled-to-order"></a>Venta de artículos ensamblados para pedido

Los elementos que se configuran para Ensamblar para pedido, no se espera que se encuentren en el inventario y se ensamblarán cuando se incluyan en un pedido de venta. Un artículo está configurado para ensamblado bajo pedido cuando el campo **Política de ensamblado** en la ficha del artículo contiene **Ensamblado bajo pedido**. Cuando especifique el producto en una línea de pedido de venta, automáticamente se creará un pedido de ensamblado y se vinculará al pedido de venta.  

> [!NOTE]  
> Si los productos de ensamblar para pedido ya se encuentran en el inventario, puede descontar esa cantidad de pedido de ensamblado y reservarla del inventario. Más información en [Vender productos de inventario en los flujos de ensamblar para pedido](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md).  

En este procedimiento, procesa la venta de un producto que se ensamblará según las especificaciones que solicita el cliente. Los pasos incluyen: 

* Creación de una línea de pedido de venta.
* Personalización del elemento de ensamblaje mediante la edición de sus componentes y recursos.
* Consulta de la disponibilidad para establecer una fecha de entrega.
* Liberación de la orden de venta para ser ensamblada y despachada inmediatamente.  

> [!NOTE]  
> El procedimiento siguiente no incluye los pasos para crear un pedido de ventas estándar antes del paso donde introduce el producto de ensamblar para pedido en una línea de pedido de venta. Obtenga más información sobre cómo crear pedidos de venta en [Vender productos con un pedido de venta de cliente](sales-how-sell-products.md).  

## <a name="to-sell-an-item-that-is-assembled-to-order"></a>Para vender un artículo que se ensamble para pedido

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Pedidos de venta** y, a continuación, elija el vínculo relacionado.  
2. Cree un pedido de ventas. 
3. En el campo **N.º**, introduzca un producto configurado para ensamblarse para pedido.  
4. En el campo **Cód. almacén**, defina de qué almacén se venderá el producto. El proceso de ensamblado se producirá en ese almacén.  
5. En el campo **Cantidad**, especifique cuántas unidades vender.  

    > [!NOTE]  
    >  Si uno o más componentes de la cantidad solicitada del producto del ensamblado no están disponibles, se abrirá una página de advertencia de disponibilidad. <!-- Check whether the field help would be useful. For more information, see Assembly Availability.  -->

    Se creará un pedido de ensamblado y se vinculará a la línea de pedido de venta. La fecha de vencimiento del pedido de ensamblado es la fecha de envío de la línea de pedido de venta.  

    La cantidad que vender se copia en el campo **Cdad. al ensamblar para pedido**, que indica que la configuración del producto espera que ensamble la cantidad total en la línea de venta. Puede reducir la cantidad que ensamblar para pedido, por ejemplo, si sabe que algunos productos ya están disponibles. Más información en [Vender productos de inventario en los flujos de ensamblar para pedido](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md).  

6. Si el cliente desea un artículo adicional en un kit, en la ficha desplegable **Líneas**, seleccione las acciones **Línea**, **Ensamblar para pedido** y, a continuación, **Ensamblar para líneas de pedido** para ver y modificar los componentes del ensamblado estándar. También puede elegir el campo **Cdad. al ensamblar para pedido**.  
7. En la página **Ensamblar para líneas de pedido**, cree una nueva línea del tipo **Producto** para el componente del ensamblado adicional.  

    También puede personalizar el pedido incrementando la cantidad de un producto estándar del kit. Puede hacerlo incrementando el valor del campo **Cantidad por** en la línea específica de pedido de ensamblado.  

    > [!NOTE]  
    >  La página **Ensamblar para líneas de pedido** contiene solo los campos básicos para personalizar la lista de componentes, añadir los números de seguimiento de producto o resolver problemas de disponibilidad de componentes. Para añadir más información del pedido de ensamblado, como la fecha inicial del pedido de ensamblado, elija la acción **Mostrar los documentos**. De esta manera, se abrirá una vista completa del pedido de ensamblado vinculado a la línea de pedido de venta. No puede cambiar el contenido de la mayoría de los campos en el encabezado de la orden de ensamblado y no puede publicar la salida del ensamblado desde allí. Debe registrar el envío de la línea de orden de venta.  
    >
    >  En las órdenes de ensamblado vinculadas, solo se puede cambiar el campo **Fecha de inicio** . Cambiar la fecha de inicio permite a los trabajadores de ensamblaje especificar que comenzarán el ensamblaje antes de la fecha de vencimiento. Todos los campos de las líneas del pedido de ensamblado vinculado pueden cambiar de forma que los empleados del almacén puedan introducir las cifras de consumo durante el proceso.  

8. Revise o reaccione a incidencias de disponibilidad de componentes. Por ejemplo, seleccione un artículo sustituto.  
9. Cierre la página **Ensamblar para líneas de pedido**. El pedido de ensamblado vinculado está preparado y los trabajadores pueden comenzar a ensamblar los productos personalizados.  
10. En el pedido de venta, seleccione la acción **Lanzar** para notificar al departamento de ensamblado que el proceso de ensamblado puede comenzar. Obtenga más información en [Ensamblar productos](assembly-how-to-assemble-items.md).  

> [!NOTE]  
> Las sustituciones de productos no reemplazan un producto automáticamente por otro producto, por ejemplo, al crear un pedido de cliente o en una lista de materiales. En cambio, se le alertará sobre el hecho de que hay una sustitución disponible.

## <a name="see-related-microsoft-training"></a>Consultar la [formación de Microsoft](/training/modules/assemble-to-order-dynamics-365-business-central/) relacionada

## <a name="see-also"></a>Consulte también .

[Gestión de ensamblaje](assembly-assemble-items.md)  
[Trabajar con L.M. de ensamblado](assembly-how-work-assembly-boms.md)  
[Registro de productos nuevos](inventory-how-register-new-items.md)  
[Inventario](inventory-manage-inventory.md)  
[Información general de la gestión de almacenes](design-details-warehouse-management.md)
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
