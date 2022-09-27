---
title: Seleccionar producción o ensamblaje en almacén básico
description: Cuando el almacén requiere el proceso de picking, pero no el proceso de envío, utilice la página Picking inventario para organizar y registrar el picking de componentes.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/24/2021
ms.author: edupont
ms.openlocfilehash: 2814fe1f9ca71c3a14bb288427c9b12603d0463a
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/19/2022
ms.locfileid: "9529143"
---
# <a name="pick-for-production-or-assembly-in-basic-warehouse-configurations"></a>Realizar picking para ensamblado o producción en una configuración básica de almacén

La forma de ubicar el picking de componentes para fabricación u órdenes de ensamblado depende de la configuración del almacén. Para obtener más información, consulte [Configuración de la administración de almacén](warehouse-setup-warehouse.md).

## <a name="pick-for-production-in-basic-warehouse-configurations"></a>Realizar el picking para la producción en configuraciones básicas de almacén

El método de baja también afecta al flujo de componentes en producción. Para obtener más información, consulte [Bajar componentes según la producción de la operación](production-how-to-flush-components-according-to-operation-output.md).

En las configuraciones avanzadas de almacén, donde las ubicaciones requieren tanto picking como envíos, debe usar la página **Picking almacén** para llevar los componentes con el método de baja establecido en *Manual*, *Pick + Adelante*, *Pick + Atrás* a las órdenes de producción. Para obtener más información, consulte [Realizar picking para ensamblado o producción en una configuración avanzada de almacén](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md).

En configuraciones de almacén básico en las que se requiere el proceso de picking, pero no el de envío, también puede usar la página **Picking de existencias** para organizar y registrar el picking de componentes con el método de baja establecido en *Manual*. Cuando registra un picking de inventario para una operación interna, como la producción, el consumo de los componentes seleccionados se registra al mismo tiempo. Como alternativa, puede usar **Movimiento de inventario** con referencia a un documento de origen para llevar los componentes con el método de baja establecido en *Manual*, *Pick + Adelante*, *Pick + Atrás* a las órdenes de producción.

Cuando las operaciones de producción se integran con procesos de almacén, ya sea por almacenes o por reubicaciones y picking, la ubicación desde la que los componentes se consumen es la ubicación definida en cada línea de componente de orden de producción. Todos los componentes necesarios deben estar disponibles en esa ubicación. Si no, el registro manual o filtrado de consumo se detiene para ese componente.

**Movimiento inventario** con referencias al documento de origen y **Picking almacén** no se puede usar para realizar el picking de componentes con métodos de baja *Adelante* y *Atrás*. **Picking de existencias** no se puede usar para realizar el picking de componentes con cualquier método de baja, sino *Manual*. Para manipular los componentes restantes, use **Movimiento de inventario** sin referencia a un documento de origen. Para obtener más información, consulte [Mover componentes a un área de operaciones en las configuraciones básicas de almacén](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md).

> [!NOTE]  
>  Los pickings de inventario, los movimientos de inventario y los pickings de almacén tienen las siguientes diferencias importantes:  
>   
>  -   Cuando registra un picking de inventario para una operación interna, como la producción, el consumo de los componentes seleccionados se registra al mismo tiempo. Cuando registra un movimiento de inventario o un picking de almacén para una operación interna, se registra únicamente el movimiento físico de los componentes necesarios en una ubicación del área de operación, sin registrar el consumo.  
> -   Cuando se utiliza el picking de inventario, el campo **Cód. ubicación** de la línea de componente de orden de producción define la ubicación *traer* desde donde los componentes disminuyen cuando se registra el consumo. Al utilizar movimientos de inventario o un picking de almacén, el campo **Código de ubicación** en las líneas de componente de orden de producción define la ubicación *apartado* en el área de la operación donde el empleado de almacén debe colocar los componentes.  

Una condición previa del sistema para picking o traslado de componentes para los documentos de origen es que una solicitud de salida de almacén exista para notificar al área de almacén de la necesidad de componentes. La solicitud de salida de almacén se crea siempre que se cambia el estado de la orden de producción a Lanzada o cuando se crea una orden de producción lanzada.  

## <a name="to-pick-production-components-in-basic-warehouse-configurations-using-inventory-pick"></a>Para realizar el picking de componentes de producción en configuraciones de almacén básicas mediante el picking de inventario

En configuraciones básicas de almacén en donde se configura la ubicación para utilizar picking, podrá escoger los componentes para las actividades de producción con la página **Picking inventario**. Para obtener más información, vea [Realizar picking de productos con picking inventario](warehouse-how-to-pick-items-with-inventory-picks.md).

1.  Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Picking inventario** y luego elija el enlace relacionado.  
2.  Para tener acceso a los componentes de la orden de producción, elija la acción **Traer doc. origen** y, a continuación, seleccione la orden de producción lanzada.  
3.  Realice el picking y, a continuación, registre la información de picking real en el campo **Cdad. a manipular**.  
4.  Cuando las líneas estén preparadas para registrar, elija la acción **Registrar**. El registro crea los movimientos de almacén necesarios y registra el consumo de los productos.  

También puede crear **Picking existencias** directamente de la orden de producción lanzada. Seleccione la acción **Crear ubicación/picking/movimiento de inventario**, seleccione la casilla **Crear pick exist.** y, a continuación, seleccione el botón **Aceptar**.

Como alternativa, puede usar el **Movimiento de inventario** con referencia al documento de origen para mover productos entre ubicaciones. Deberá registrar el consumo por separado. Para obtener más información, consulte [Registrar consumibles de producción por lotes](production-how-to-post-consumption.md)

## <a name="pick-for-assembly-in-basic-warehouse-configurations"></a>Realizar el picking para el ensamblado en configuraciones básicas de almacén

En configuraciones avanzadas de almacén, donde las ubicaciones requieren tanto picking como envíos, debe usar la página **Picking de almacén** para llevar los componentes a los pedidos de ensamblado. Para obtener más información, consulte [Realizar picking para ensamblado o producción en una configuración avanzada de almacén](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md).

En configuraciones básicas de almacén, también puede realizar el picking para los pedidos de ensamblado con la página **Movimiento inventario**. 

En configuraciones básicas de almacén donde la ubicación requiere el proceso de picking pero no el proceso de envío, la página **Picking de existencias** también se usa para realizar el picking, ensamblar y enviar para pedidos de venta donde los productos deben ensamblarse antes de poder enviarse. Para obtener más información, consulte [Gestión de productos de ensamblar para pedido con picking de inventario](warehouse-how-to-pick-for-production.md#handling-assemble-to-order-items-with-inventory-picks).  

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

## <a name="filling-the-consumption-bin"></a>Rellenando la ubicación del consumo

Este organigrama muestra cómo se rellena el campo de **Código de ubicación** en las líneas del componente de la orden de producción según la ubicación.

![Diagrama de flujo de ubicación.](media/binflow.png "BinFlow")

## <a name="see-related-microsoft-training"></a>Consultar la [formación de Microsoft](/training/paths/pick-ship-items-business-central/) relacionada

## <a name="see-also"></a>Consulte también .

[Warehouse Management](warehouse-manage-warehouse.md)  
[Inventario](inventory-manage-inventory.md)  
[Configuración de Warehouse Management](warehouse-setup-warehouse.md)  
[Gestión de ensamblaje](assembly-assemble-items.md)  
[Detalles de diseño: Warehouse Management](design-details-warehouse-management.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
