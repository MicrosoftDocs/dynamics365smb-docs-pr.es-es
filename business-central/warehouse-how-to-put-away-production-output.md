---
title: Ubicar la salida de producción
description: En este artículo se describe cómo almacenar la salida de producción.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 12/20/2022
ms.custom: bap-template
ms.search.forms: '9326, 99000831, 9315, 7375'
---
# <a name="put-away-production-or-assembly-output" />Ubicar la salida de producción o la salida de ensamblado

La forma de ubicar la salida de su producción depende de cómo esté configurado el almacén. Obtenga más información en [Configuración de Warehouse Management](warehouse-setup-warehouse.md).  

En las configuraciones básicas de almacén, donde el almacén requiere el proceso de almacenamiento, utilice el documento **Almacenamiento de inventario** para la salida de posproducción y registrar los almacenamientos para esta.  

> [!NOTE]  
> El proceso de ensamblado no admite almacenamientos de inventario. PublicRegistre un pedido de ensamblado para registrar la salida. Si usa ubicaciones, puede mover elementos entre ubicaciones más tarde. Obtenga más información en [Mover productos ad hoc en configuraciones básicas de almacén](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md).  

En las configuraciones avanzadas de almacén, donde un almacén no requiere los procesos de almacenamiento y recepción, cree un documento de ubicación interno o un documento de movimiento para ubicar la salida.  

## <a name="to-put-away-production-output-with-an-inventory-put-away" />Para colocar la salida de producción con una colocación de inventario

El primer paso para almacenar la salida es crear la solicitud de almacén de entrada. Esta solicitud informa al almacén de que la salida del pedido de producción o ensamblado está preparada para ubicación.

### <a name="to-create-the-inbound-warehouse-request" />Para crear la solicitud de entrada al almacén

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") icono, escriba **Orden de producción lanzada** y, a continuación, elija el vínculo relacionado.  
2. Elija la orden de producción que está preparada para el almacenamiento y, después, elija la acción **Crear solicitud entrada almacén**.  

> [!NOTE]  
> También puede crear la solicitud de almacén de entrada eligiendo el campo **Crear solicitud de entrada** al actualizar la orden de producción. Obtener más información en [Actualizar o replanificar órdenes de producción](production-how-to-replan-refresh-production-orders.md).  

### <a name="to-put-output-away-with-an-inventory-put-away" />Para ubicar la salida con una ubicación de inventario

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Ubicación existencias** y luego elija el enlace relacionado.  
2. Cree una ubicación de inventario nueva. Obtenga más información en [Almacenar productos con almacenes de inventario](warehouse-how-to-put-items-away-with-inventory-put-aways.md).
3. Para tener acceso a la salida de la orden de producción, elija la acción **Traer doc. origen** y, a continuación, seleccione la orden de producción lanzada.  
4. Rellene las líneas de ubicación como sea necesario.
5. Cuando las líneas estén preparadas para registrar, elija la acción **Registrar**. El registro creará los movimientos de almacén y registrará la salida de los productos.  

    [!INCLUDE [preview-posting-warehouse](includes/preview-posting-warehouse.md)]

También puede crear **Ubicación existencias** directamente de la orden de producción lanzada. Obtenga más información en [Almacenar productos con almacenes de inventario](warehouse-how-to-put-items-away-with-inventory-put-aways.md).  

Al registrar un almacenamiento de inventario, se asume que todas las operaciones se registran según la ruta estándar. Es decir, la cantidad de salida se registra de acuerdo con la última operación. Puede usar el diario de salida para registrar las desviaciones de la cantidad de salida y los tiempos de preparación y ejecución. Si es preciso realizar un registro parcial después de crear el almacenamiento de inventario, puede hacerlo en configuración de tiempos y cantidades de todas las operaciones, excepto la última. La última operación se controla por el almacenamiento de inventario.  

Si solo necesita registrar el tiempo de preparación y ejecución de la última operación, defina la cantidad de salida de la última operación en 0. Puede decidir no registrar la última línea eliminándola.

## <a name="to-put-assembly-and-production-output-away-in-advanced-warehouse-configurations" />Para colocar el ensamblado y la producción en configuraciones avanzadas de almacén

Al registrar la salida de la orden de producción o ensamblado en un almacén que utiliza el almacenamiento y picking dirigidos, la salida se coloca en la ubicación definida en la orden de producción o ensamblado. Obtenga más información sobre las diferentes formas de mover productos en el almacén con las configuraciones avanzadas; vaya a [Mover productos en configuraciones avanzadas de almacén](warehouse-how-to-move-items-in-advanced-warehousing.md#to-move-items-with-the-warehouse-movement-worksheet).

> [!NOTE]  
> No puede indicar el número de documento de origen, como el número de orden de producción, en los documentos de almacenamiento interno, almacenamiento o movimiento para los procesos de salida de ensamblado o producción.  

## <a name="see-also" />Consulte también

[Información general de la gestión de almacenes](design-details-warehouse-management.md)
[Inventario](inventory-manage-inventory.md)  
[Configuración de Warehouse Management](warehouse-setup-warehouse.md)  
[Gestión de ensamblaje](assembly-assemble-items.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
