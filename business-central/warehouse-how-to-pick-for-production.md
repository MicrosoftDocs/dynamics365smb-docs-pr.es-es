---
title: Realizar picking para ensamblado, producción o trabajos en un almacén básico
description: Cuando el almacén requiere que procese el picking, pero no los envíos, utilice la página Picking inventario para registrar los componentes que fueron elegidos.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 08/02/2022
ms.author: bholtorf
ms.openlocfilehash: 859c70ebc51f2649000d41817d173292ed5b0870
ms.sourcegitcommit: b4da421c19c3aa3031b0344ec2829d2038be6642
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/03/2022
ms.locfileid: "9617882"
---
# <a name="pick-for-production-assembly-or-jobs-in-basic-warehouse-configurations"></a>Realizar picking para producción, ensamblado o proyectos en una configuración básica de almacén

La forma de ubicar el picking de componentes para fabricación u órdenes de ensamblado depende de la configuración del almacén. Para obtener más información, consulte [Configuración de la administración de almacén](warehouse-setup-warehouse.md).

## <a name="pick-for-production-in-basic-warehouse-configurations"></a>Realizar el picking para la producción en configuraciones básicas de almacén

Si una ubicación requiere el proceso de picking pero no el procesado de envíos, puede usar la página **Picking existencias**. La página **Picking existencias** le permite organizar y registrar el picking de artículos que tienen su método de descarga establecido en **Manual**. Cuando registra un picking de inventario, se registra el consumo de los componentes seleccionados. También puede usar un **Movimiento de inventario** con referencia a un documento de origen para asignar los componentes con el método de baja establecido en **Manual**, **Pick + Adelante**, **Pick + Atrás** a las órdenes de producción.

Si la producción se integra con procesos de almacén mediante almacenes o por reubicaciones y picking, los componentes se consumen desde la línea de producción. Todos los componentes necesarios deben estar disponibles en esa ubicación. Si no, el registro manual o filtrado de consumo se detiene para ese componente.

> [!NOTE]  
> Los pickings de inventario, los movimientos de inventario y los pickings de almacén tienen las siguientes diferencias importantes:  
>
> - Cuando registra un picking de inventario para una operación interna, como la producción, el consumo de los componentes seleccionados se registra al mismo tiempo. Cuando registra un movimiento de inventario o un picking de almacén para una operación interna, se registra únicamente el movimiento físico de los componentes necesarios en una ubicación del área de operación, sin registrar el consumo.  
> - Cuando se utiliza el picking de inventario, el campo **Cód. ubicación** de la línea de componente de orden de producción define la ubicación *traer* desde donde los componentes disminuyen cuando se registra el consumo. Al utilizar movimientos de inventario o un picking de almacén, el campo **Código de ubicación** en las líneas de componente de orden de producción define la ubicación *apartado* en el área de la operación donde el empleado de almacén debe colocar los componentes.  

Para realizar el pick o mover componentes para los documentos de origen, una solicitud de salida de almacén debe notificar al almacén de la necesidad del componente. La solicitud de almacén de salida se crea cuando hace lo siguiente:

- Cambiar el estado de una orden de producción a Liberado.
- Crear una orden de producción lanzada.  

Los métodos de baja también afectan al flujo de componentes en producción. Para obtener más información, consulte [Bajar componentes según la producción de la operación](production-how-to-flush-components-according-to-operation-output.md). **Movimiento inventario** con referencias al documento de origen y **Picking almacén** no se puede usar para realizar el picking de componentes con métodos de baja *Adelante* y *Atrás*. **Picking de existencias** no se puede usar para realizar el picking de componentes con cualquier método de baja, sino *Manual*. Para manipular los componentes restantes, use **Movimiento de inventario** sin referencia a un documento de origen. Para obtener más información, consulte [Mover componentes a un área de operaciones en las configuraciones básicas de almacén](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md).

En las configuraciones avanzadas de almacén, donde las ubicaciones requieren tanto picking como envíos, debe usar la página **Picking almacén** para llevar los componentes con el método de baja establecido en *Manual*, *Pick + Adelante*, *Pick + Atrás* a las órdenes de producción. Para obtener más información, consulte [Realizar picking para ensamblado o producción en una configuración avanzada de almacén](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md).

## <a name="to-pick-components-for-production-and-jobs-in-basic-warehouse-configurations"></a>Para hacer el picking de componentes para producción y trabajos en configuraciones básicas de álmacen

En configuraciones básicas de almacén en donde se configura la ubicación para utilizar picking, podrá escoger los componentes para las actividades de producción y líneas de planificación de trabajo la página **Picking inventario**. Para obtener más información, vea [Realizar picking de productos con picking inventario](warehouse-how-to-pick-items-with-inventory-picks.md).

> [!NOTE]
> Se agregó la capacidad de seleccionar componentes para las líneas de planificación de trabajos a [!INCLUDE[d365fin](includes/d365fin_md.md)] en el lanzamiento de versiones 2 de 2022. Para empezar a usar la capacidad, un administrador debe activar **Actualización de característica: habilitar el picking de almacén e inventario de los proyectos** en la página **Administración de características**.
>
>[!INCLUDE[prod_short](includes/prod_short.md)] utiliza el valor del campo **Cantidad restante** en la línea de planificación del trabajo cuando crea selecciones de inventario. Para usar selecciones de inventario para trabajos, debe activar la opción **Aplicar enlace de uso** en la página **Tarjeta de trabajo** para el trabajo. Esto le permite rastrear el uso contra su plan. Si no activa la opción, la cantidad restante permanecerá en **0** y la selección de inventario no se creará. Para obtener más información, consulte [Configurar seguimiento de uso de trabajo](projects-how-setup-jobs.md?tabs=current-experience#to-set-up-job-usage-tracking).

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Picking inventario** y luego elija el enlace relacionado.  
2. Para tener acceso a los componentes de la orden de producción, elija la acción **Traer doc. origen** y, a continuación, seleccione la orden de producción lanzada.  
3. Realice el picking del componente, a continuación, registre la información de picking en el campo **Cdad. a manipular**.  
4. Cuando las líneas estén preparadas para registrar, elija la acción **Registrar**. El registro crea los movimientos de almacén necesarios y registra el consumo de los productos.  

También puede crear **Picking existencias** directamente de la orden de producción lanzada. Seleccione la acción **Crear ubicación/picking/movimiento de inventario**, seleccione la casilla **Crear pick exist.** y, a continuación, seleccione el botón **Aceptar**.

Como alternativa, puede usar un **Movimiento de inventario** con referencia al documento de origen para mover productos entre ubicaciones. Deberá registrar el consumo por separado. Para obtener más información, consulte [Registrar consumibles de producción por lotes](production-how-to-post-consumption.md)

## <a name="pick-for-assembly-in-basic-warehouse-configurations"></a>Realizar el picking para el ensamblado en configuraciones básicas de almacén

Use las siguientes páginas para seleccionar pedidos de ensamblado:

- La página **Movimiento de inventario**.
- Si la ubicación requiere picking pero no envíos, use la página **Picking de inventario** también se utiliza para realizar el picking, ensamblaje y envíos para pedidos de ventas cuando los productos se deben ensamblar antes de que se puedan enviar. Para obtener más información, consulte [Gestión de productos de ensamblar para pedido con picking de inventario](warehouse-how-to-pick-for-production.md#handling-assemble-to-order-items-with-inventory-picks).  

En configuraciones avanzadas de almacén, donde las ubicaciones requieren tanto picking como envíos, debe usar la página **Picking de almacén** para llevar los componentes a los pedidos de ensamblado. Para obtener más información, consulte [Realizar picking para ensamblado o producción en una configuración avanzada de almacén](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md).

## <a name="handling-assemble-to-order-items-with-inventory-picks"></a>Tratamiento de productos de ensamblar para pedido con los picking de inventario

La página **Picking de inventario** también se utiliza para realizar el picking y envíos para ventas cuando los productos se deben ensamblar antes de que se puedan enviar. Para obtener más información, consulte [Venta de artículos ensamblados para pedido](assembly-how-to-sell-items-assembled-to-order.md).

Los artículos ensamblar para pedido no se consideran en una ubicación hasta que se ensamblan y se registran como salida en una ubicación de la zona de ensamblado. Por lo tanto, seleccionar estos artículos para su envío sigue un flujo especial. De una ubicación, los empleados del almacén toman los productos de ensamblado al muelle de envío y después registran el picking de inventario. El picking de inventario registrado registra a continuación la salida de ensamblado, el consumo de componentes y el albarán de venta.

Puede configurar [!INCLUDE[prod_short](includes/prod_short.md)] para que cree automáticamente un movimiento de inventario cuando el picking de inventario para el producto del ensamblado se crea. Para crear movimientos automáticamente, elija el campo **Crear movimientos automáticamente** en la página **Conf. ensamblado**. Para obtener más información, consulte [Mover componentes a un área de operaciones en el almacenamiento básico](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md).

[!INCLUDE[prod_short](includes/prod_short.md)] crea líneas de picking de existencias para artículos de ventas de forma distinta, dependiendo de que no se ensamble ninguna, alguna o toda la cantidad de línea de venta para pedido.

- En las ventas en las que utiliza selecciones de inventario para registrar el envío de inventario, [!INCLUDE[prod_short](includes/prod_short.md)] crea una línea de selección de inventario para cada línea de orden de venta. Si el artículo se coloca en contenedores diferentes, se creará más de una línea. Las líneas de picking se basan en la cantidad en el campo **Cantidad a enviar**.
- En las ventas cuya cantidad total de la línea de pedido de venta se ensambla para pedido, una línea de picking de inventario se crea para esa cantidad. Este valor del campo Cantidad a ensamblar es igual al valor del campo **Cdad. a enviar**. El campo **Ensamblar para pedido** está seleccionada en la línea.

Si un flujo de salida de ensamblado está configurado para el almacén, el valor en los campos **Cód. ubic. ens.contra-pedido** o **Cód. ubic. desde ensamblado**, en ese orden, se inserta en el campo **Cód. ubicación** de la línea de picking de inventario.

Si no se especifica ningún código de ubicación de la línea de pedido de venta, y no se configura ningún flujo de salida de ensamblado para el almacén, el campo **Cód. ubicación** de la línea de picking de inventario está vacío. El empleado del almacén debe abrir la página **Contenidos ubicación** y seleccionar el almacén donde se ensamblan los productos de ensamblado.

Cuando parte de la cantidad debe ensamblarse primero y a la otra se le debe realizar el picking de inventario, [!INCLUDE[prod_short](includes/prod_short.md)] crea al menos dos líneas de picking de inventario. Una línea de picking es para la cantidad de ensamblado para pedido. La otra línea de picking depende de qué ubicación pueden cubrir la cantidad pendiente de inventario. Los códigos de ubicación en las dos líneas se completan de formas distintas según se describe para los dos tipos de venta respectivamente. Para obtener más información, consulte la sección "Escenarios de combinación" en [Comprender Ensamblar para pedido y Ensamblar para stock](assembly-assemble-to-order-or-assemble-to-stock.md).

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
