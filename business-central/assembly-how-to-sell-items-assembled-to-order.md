---
title: "Venta de artículos ensamblados para pedido | Documentos de Microsoft"
description: "Si un elemento está configurado para Ensamblar para pedido, no se espera que se encuentre en el inventario y el campo debe ensamblarse específicamente para un pedido de venta. Cuando especifique el producto en una línea de pedido de venta, automáticamente se creará un pedido de ensamblado y se vinculará al pedido de venta."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: kit, kitting
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 5540c45eefb1272c5dfa5c790586f6b33b4f4848
ms.contentlocale: es-es
ms.lasthandoff: 11/26/2018

---
# <a name="sell-items-assembled-to-order"></a>Venta de artículos ensamblados para pedido
Si el campo **Directiva de ensamblado** de la ficha de producto de un elemento del ensamblado es **Ensamblar para pedido**, no se espera que el producto se encuentre en el inventario y el campo debe ensamblarse específicamente para un pedido de venta. Cuando especifique el producto en una línea de pedido de venta, automáticamente se creará un pedido de ensamblado y se vinculará al pedido de venta.  

> [!NOTE]  
>  Si algunos productos de ensamblar para pedido ya se encuentran en el inventario, puede descontar esa cantidad de pedido de ensamblado y reservarla del inventario. Para obtener más información, consulte [Venta de productos de inventario en los flujos de ensamblar para pedido](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md).  

En este procedimiento, procesa la venta de un producto que se ensamblará según las especificaciones que solicita el cliente. Los pasos incluyen la iniciación de la línea de pedido de venta, la personalización del producto del ensamblado mediante la modificación de sus componentes y recursos, la comprobación de disponibilidad para establecer una fecha de entrega y el lanzamiento del pedido de venta para ensamblarse y enviarse de inmediato.  

> [!NOTE]  
>  El procedimiento siguiente no incluye los pasos habituales del pedido de ventas antes del paso donde introduce el producto de ensamblar para pedido en una línea de pedido de venta.  

## <a name="to-sell-an-item-that-is-assembled-to-order"></a>Para vender un artículo que se ensamble para pedido  
1.  Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Pedidos de venta** y luego elija el enlace relacionado.  
2.  Cree un pedido de ventas. Para obtener más información, vea [Vender productos](sales-how-sell-products.md).  
3.  En el campo **N.º**, introduzca un producto configurado para ensamblarse para pedido.  
4.  En el campo **Cód. almacén**, defina de qué almacén se venderá el producto. El proceso de ensamblado se producirá en ese almacén.  
5.  En el campo **Cantidad**, especifique cuántas unidades vender.  

    > [!NOTE]  
    >  Si uno o más componentes de la cantidad solicitada del producto del ensamblado no están disponibles, se abrirá una página de advertencia de disponibilidad detallada. Para obtener más información, consulte Disponibilidad de ensamblado.  

    Entonces se creará un pedido de ensamblado y se vinculará a la línea de pedido de venta automáticamente. La fecha de vencimiento de este pedido de ensamblado está sincronizada con la fecha de envío de la línea de pedido de venta.  

    La cantidad que vender se copia en el campo **Cdad. al ensamblar para pedido**, que indica que la configuración del producto espera que la cantidad total en la línea de venta se ensamble para el pedido. Puede reducir la cantidad que ensamblar para pedido, por ejemplo si sabe que algunos productos ya están disponibles. Para obtener más información, consulte [Venta de productos de inventario en los flujos de ensamblar para pedido](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md).  

6.  Para reflejar que el cliente desea un artículo adicional en un kit, en la ficha desplegable **Líneas**, seleccione las acciones **Línea**, **Ensamblar para pedido** y, a continuación, **Ensamblar para líneas de pedido** para ver y modificar los componentes del ensamblado estándar. También puede elegir el campo **Cdad. al ensamblar para pedido**.  
7.  En la página **Ensamblar para líneas de pedido**, cree una nueva línea del tipo **Producto** para el contenido del kit adicional solicitado. La línea representa un componente de ensamblado adicional.  

    También puede personalizar el pedido incrementando la cantidad de un producto estándar del kit. Puede hacerlo incrementando el valor del campo **Cantidad por** en la línea específica de pedido de ensamblado.  

    > [!NOTE]  
    >  La página **Ensamblar para líneas de pedido** contiene solo los campos básicos que se espera que un vendedor utilice para personalizar la lista de componentes, añadir los números de seguimiento de producto o resolver problemas de disponibilidad de componentes. Para ver más información del pedido de ensamblado, como la fecha inicial del pedido de ensamblado, elija la acción **Mostrar los documentos**. De esta manera, se abrirá una vista completa del pedido de ensamblado vinculado a la línea de pedido de venta. No puede modificar el contenido de la mayoría de los campos de la cabecera del pedido de ensamblado y no puede registrar la salida de ensamblado de él porque debe utilizar el registro de envío de la línea de pedido de venta.  
    >   
    >  En la cabecera de pedidos de ensamblado vinculados, solo el campo **Fecha inicial** se puede cambiar para permitir a los empleados de ensamblado especificar una fecha que sea anterior a la fecha de vencimiento en la que comenzarán el proceso. Todos los campos de las líneas del pedido de ensamblado vinculado pueden cambiar de forma que los empleados del almacén puedan introducir las cifras de consumo durante el proceso.  

8.  Revise o reaccione a incidencias de disponibilidad de componentes. Por ejemplo, seleccione un producto sustitutivo disponible o establezca una fecha de vencimiento posterior.  
9. Cierre la página **Ensamblar para líneas de pedido**. El pedido de ensamblado vinculado ahora está preparado para comenzar a ensamblar los productos personalizados por fecha de vencimiento.  
10. En el pedido de venta, seleccione la acción **Lanzar** para notificar al departamento de ensamblado que el proceso de ensamblado puede comenzar.  
11. En el departamento de ensamblado, realice los pasos de ensamblado de los productos que se venden en este procedimiento. Para obtener más información, consulte [Ensamblar productos](assembly-how-to-assemble-items.md).  

## <a name="see-also"></a>Consulte también  
[Gestión de ensamblaje](assembly-assemble-items.md)  
[Trabajar con listas de materiales](inventory-how-work-BOMs.md)  
[Grupos contables inventario](inventory-manage-inventory.md)  
[Detalles de diseño: Gestión de almacén](design-details-warehouse-management.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

