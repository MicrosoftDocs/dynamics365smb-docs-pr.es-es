---
title: Realizar picking de productos con picking inventario
description: Si la configuración de un almacén requiere proceso de picking pero no de envío, utilice documentos de picking de inventario para registrar la información de picking y de envío para documentos de origen.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: b0f0bf09670620a36ee696fdc9d1483a2c33f77b
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2022
ms.locfileid: "8144338"
---
# <a name="pick-items-with-inventory-picks"></a>Realizar el picking de productos con picking inventario

Cuando su almacén está configurado para requerir proceso de picking, pero no de envío, utilice la página **Picking inventario** para registrar la información de picking y envío de sus documentos de origen. El documento de origen de salida puede ser un pedido de venta, una devolución de compras, un pedido de transferencia de salida o una orden de producción cuyos componentes están preparados para picking.

> [!NOTE]  
> Los componentes para los pedidos de ensamblado no se seleccionar o registrar con picking de inventario. En lugar de eso, use la página **Movimiento inventario**. Para obtener más información, consulte [Mover componentes a un área de operaciones en el almacenamiento básico](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md).
>
> Cuando las cantidades de la línea de picking y envío que se ensamblan para el pedido, debe seguir ciertas reglas al crear las líneas de picking de inventario. Para obtener más información, vea la sección [Tratamiento de productos ensamblar para pedido con los picking de inventario](#handling-assemble-to-order-items-with-inventory-picks).  

Puede crear un picking de inventario de tres formas:  

- Cree el picking en dos pasos solicitando primero un picking de inventario mediante el lanzamiento del documento de origen. Esto indica al almacén que el documento de origen está preparado para el picking. A continuación, se puede crear el picking de inventario en la página **Picking inventario** según el documento de origen.  
- Cree el picking de inventario directamente desde el propio documento de origen.  
- Con el trabajo por lotes, puede crear picking de inventario para varios documentos de origen al mismo tiempo.  

## <a name="to-request-an-inventory-pick-by-releasing-the-source-document"></a>Para solicitar un picking de inventario lanzado el documento de origen

En el caso de pedidos de venta, pedidos de devolución de compra y pedidos de transferencia de salida, para crear la solicitud de almacén, lance el pedido. A continuación se describe cómo hacerlo des de un pedido de venta.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Pedidos de venta** y, a continuación, elija el vínculo relacionado.
2. Seleccione el pedido de venta que desea lanzar, y después seleccione **Lanzar**.

Para las órdenes de producción, cree la solicitud de almacén automáticamente para el picking de componentes, llamado *método de baja* cuando cambie el estado de la orden de producción a **Lanzado** o cuando se cree la orden de producción lanzada. Para obtener más información, consulte [Picking para producción o ensamblado](warehouse-how-to-pick-for-production.md).

Cuando se ha creado la solicitud de almacén, un empleado del almacén asignado a realizar el picking de productos puede ver que el documento de origen está preparado para el picking y puede crear un nuevo documento de picking basado en la solicitud de almacén.  

## <a name="to-create-an-inventory-pick-based-on-the-source-document"></a>Para crear un picking de inventario basado en el documento de origen

Ahora que se ha creado la solicitud, el empleado del almacén puede crear un nuevo picking de inventario basado en el documento de origen lanzado.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Picking inventario** y luego elija el enlace relacionado.  
2. Seleccione la acción **Nuevo**.  
    Asegúrese de que el campo **N.º** en desplegable **General** se haya rellenado.
3. En el campo **Documento origen**, seleccione el tipo de documento de origen en el que está realizando el picking.  
4. En el campo **Cód. procedencia mov.**, seleccione el documento de origen.  
5. También, elija la acción **Traer documento origen** para seleccionar un documento de una lista de documentos de origen de salida que están preparados para el picking en el almacén.  
6. Elija el botón **Aceptar** para rellenar las líneas de picking según el documento de origen seleccionado.  

## <a name="to-create-an-inventory-pick-from-the-source-document"></a>Para crear un picking de inventario desde el documento de origen

1. En el documento de origen, que puede ser un pedido de ventas, una devolución de compras, un pedido de transferencia de salida o un pedido de producción, elija la acción **Crear ubicac. invent./picking**.
2. Active la casilla **Crear pick exist.**.  
3. Elija el botón **Aceptar**. Se creará un nuevo picking de inventario.

## <a name="to-create-multiple-inventory-picks-with-a-batch-job"></a>Para crear varios picking de inventario con un trabajo por lotes

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Crear ubicac./pick. exist.** y, a continuación, elija el vínculo relacionado.  
2. En la ficha desplegable **Solicitud almacén**, use los campos **Documento origen** y **Cód. procedencia mov.** para filtrar determinados tipos de documentos o intervalos de números de documento. Por ejemplo, puede crear picking solo de los pedidos de venta.  
3. En la ficha desplegable **Opciones**, seleccione la casilla **Crear pick exist.**
4. Elija el botón **Aceptar**. Se crean los picking de inventario especificados.

> [!NOTE]  
> Si las cantidades de la línea de picking y envío que se ensamblan para el pedido, debe seguir ciertas reglas al crear las líneas de picking de inventario. Para obtener más información, vea la sección [Tratamiento de productos ensamblar para pedido con los picking de inventario](#handling-assemble-to-order-items-with-inventory-picks).  
>
> En la configuración del almacenamiento básico, se realiza picking de los productos que se ensamblan para pedidos de venta del pedido de venta relacionado, como se explica en este tema. Para obtener más información, vea la sección [Tratamiento de productos ensamblar para pedido con los picking de inventario](#handling-assemble-to-order-items-with-inventory-picks).  

## <a name="to-record-the-inventory-picks"></a>Para registrar los picking de inventario

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Picking inventario** y luego elija el enlace relacionado.  
2. En las líneas de picking del campo **Cód. ubicación**, la ubicación desde la cual se debe realizar el picking de productos se sugiere como la ubicación predeterminada del artículo. Si es necesario puede cambiar la ubicación en esta página.  
3. Realice el picking e introduzca la información de la cantidad de ubicación real en la ventana **Cdad. a manipular**.

    Si es necesario realizar el picking de productos para otra línea des de varias ubicaciones porque no están disponibles en la ubicación designada, por ejemplo, utilice la función **Dividir línea** en la ficha desplegable **Líneas**. Para obtener más información acerca de cómo dividir líneas, consulte[Dividir las líneas de actividad de almacén](warehouse-how-to-split-warehouse-activity-lines.md).  
4. Cuando haya realizado el picking, elija la acción **Registrar**.  

El proceso de registro registrará el envío de las líneas del documento de origen de las que se ha realizado el picking, o en el caso de las órdenes de producción, el proceso de registro registrará el consumo. Si el almacén utiliza ubicaciones, el registro también creará movimientos de almacén para registrar los cambios de cantidad en la ubicación.  

## <a name="to-delete-inventory-pick-lines"></a>Para eliminar líneas de picking de inventario

Si los productos del picking de inventario no están disponibles, puede eliminar tales líneas de picking de inventario después de registrarlos y posteriormente eliminar el documento respectivo. El documento de origen, como un pedido de venta o un pedido de producción, dispondrá de productos restantes susceptibles de picking, que se pueden obtener a través de un nuevo picking de inventario cuando los productos estén disponibles.  

> [!WARNING]  
> Este proceso no será posible si números de serie/lote se especifica en el documento de origen. Por ejemplo, si una línea de pedido de venta contiene un número de serie/lote, dicha especificación de seguimiento de producto se eliminará si se borra una línea de picking de inventario para ese número de serie/lote.  
>
> Si las líneas de picking de inventario tienen números de lote/serie que no están disponibles, no debe eliminar las líneas en cuestión. En su lugar, debe cambiar campo **Cdad. a manipular** a cero, registrar los picking reales y eliminar el documento de picking de inventario. Esto asegura que las líneas de picking de inventario de tales números de lote/serie se pueden volver a crear a partir del pedido de venta más adelante.  

## <a name="handling-assemble-to-order-items-with-inventory-picks"></a>Tratamiento de productos de ensamblar para pedido con los picking de inventario

La página **Picking de inventario** también se utiliza para realizar el picking y envíos para ventas cuando los productos se deben ensamblar antes de que se puedan enviar. Para obtener más información, consulte [Venta de artículos ensamblados para pedido](assembly-how-to-sell-items-assembled-to-order.md).

Los productos que se van a enviar no están presentes físicamente en una ubicación hasta que se ensamblan y se registran como salida en una ubicación de la zona de ensamblado. Esto significa que realizar el picking de productos ensamblar para pedido para el envío sigue un flujo especial. De una ubicación, los empleados del almacén toman los productos de ensamblado al muelle de envío y después registran el picking de inventario. El picking de inventario registrado registra a continuación la salida de ensamblado, el consumo de componentes y el albarán de venta.

Puede configurar [!INCLUDE[prod_short](includes/prod_short.md)] para que cree automáticamente un movimiento de inventario cuando el picking de inventario para el producto del ensamblado se crea. Para habilitarlo, debe seleccionar el campo **Crear movimientos automáticamente** en la página **Conf. ensamblado**. Para obtener más información, consulte [Mover componentes a un área de operaciones en el almacenamiento básico](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md).

Las líneas de picking de existencias se crean de diferentes modos en función de que no se ensamble ninguna, alguna o toda la cantidad de línea de venta para pedido.

En ventas normales en las que se utiliza el picking de inventario para registrar el envío de cantidades de inventario, para cada línea de pedido de venta se crea una línea de picking de inventario, o varias si el producto se coloca en ubicaciones diferentes. Esta línea de picking se basa en la cantidad en el campo **Cantidad a enviar**.

De las ventas de ensamblar para pedido cuya cantidad total de la línea de pedido de venta se ensambla para pedido, una línea de picking de inventario se crea para esa cantidad. Esto significa que el valor del campo Cantidad a ensamblar es igual al valor del campo **Cdad. a enviar**. El campo **Ensamblar para pedido** está seleccionada en la línea.

Si un flujo de salida de ensamblado está configurado para el almacén, el valor del campo **Cód. ubic. ens.contra-pedido** o el valor en el campo **Cód. ubic. desde ensamblado**, en ese orden, se inserta en el campo **Cód. ubicación** de la línea de picking de inventario.

Si no se especifica ningún código de ubicación de la línea de pedido de venta, y no se configura ningún flujo de salida de ensamblado para el almacén, el campo **Cód. ubicación** de la línea de picking de inventario está vacío. El empleado del almacén debe abrir la página **Contenidos ubicación** y seleccionar el almacén donde se ensamblan los productos de ensamblado.

En escenarios de combinación, donde parte de la cantidad debe ensamblarse primero y a la otra se le debe realizar el picking de inventario, un mínimo de dos líneas de picking de inventario se crea. Una línea de picking es para la cantidad de ensamblado para pedido. La otra línea de picking depende de qué ubicación pueden cubrir la cantidad pendiente de inventario. Los códigos de ubicación en las dos líneas se completan de formas distintas según se describe para los dos tipos de venta respectivamente. Para obtener más información, consulte la sección "Escenarios de combinación" en [Comprender Ensamblar para pedido y Ensamblar para stock](assembly-assemble-to-order-or-assemble-to-stock.md).

## <a name="see-also"></a>Consulte también

[Gestión almacén](warehouse-manage-warehouse.md)  
[Inventario](inventory-manage-inventory.md)  
[Configuración de la gestión del almacén](warehouse-setup-warehouse.md)  
[Gestión de ensamblaje](assembly-assemble-items.md)  
[Tutorial: picking y envío en la configuración del almacenamiento básico](walkthrough-picking-and-shipping-in-basic-warehousing.md)  
[Detalles de diseño: Gestión de almacén](design-details-warehouse-management.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]