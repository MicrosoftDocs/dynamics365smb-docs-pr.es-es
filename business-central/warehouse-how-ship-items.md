---
title: Enviar productos
description: En este artículo se describe cómo enviar productos desde su almacén.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.date: 02/22/2023
ms.custom: bap-template
ms.search.form: '7335, 7337, 7339, 7340, 7341, 7362, 9008'
---

# <a name="ship-items-with-a-warehouse-shipment"></a>Enviar productos con envío de almacén

En [!INCLUDE[prod_short](includes/prod_short.md)], la selección y el envío de productos se realizan mediante uno de los cuatro métodos, como se describe en la siguiente tabla.

|Método|Proceso de salida|Picking requerido|Envío requerido|Nivel de complejidad (Obtenga más información en [Descripción general de la gestión de almacenes](design-details-warehouse-management.md))|  
|------|----------------|-----|---------|-------------------------------------------------------------------------------------|  
|A|Registro de picking y envío desde la línea de pedido|||No hay ninguna actividad de almacén dedicada.|  
|B|Registro de picking y envío desde un documento de picking de existencias|Activado||Básico: Pedido por pedido|  
|P|Registro de picking y envío desde un documento de envío de almacén||Activado|Básico: Publicación consolidada de recepción/envío para múltiples pedidos.|  
|D|Registro de picking desde un documento de picking de almacén y registro de envío de un documento de envío de almacén|Activado|Activado|Avanzado|  

Para obtener más información sobre el envío de productos, vaya a [Flujo de salida del almacén](design-details-outbound-warehouse-flow.md).

Este artículo hace referencia a los métodos C y D de la tabla. En ambos métodos, se empieza creando un documento de envío a partir de un documento de origen empresarial. A continuación, seleccione los productos especificados para el envío.

Cuando una ubicación requiere envíos de almacén, puede enviar productos en función de los documentos de origen que se hayan enviado al almacén. La liberación de documentos de origen hace que los productos que contienen estén listos para ser manipulados en el almacén. Los siguientes son ejemplos de documentos de origen:

* Pedidos de venta
* Pedidos de devolución compra
* Pedidos de transferencia
* Pedidos de servicio

Puede crear un envío de almacén de dos maneras:

* De manera forzada, cuando el trabajo se realiza pedido por pedido. Elija la acción **Crear envío de almacén** en el documento de origen para crear un envío de almacén para el documento.
* De forma forzada, donde usa la acción **Liberar** en el documento de origen para liberarlo al almacén. Un empleado de almacén crea una **Envío de almacén** para uno o varios documentos de origen emitidos. El siguiente procedimiento describe cómo crear un envío de almacén de manera forzada.

## <a name="to-ship-items-using-a-warehouse-shipment-document"></a>Para enviar productos con un documento de envío de almacén

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Envíos de almacén** y luego elija el enlace relacionado.  
2. Elija **Nuevo**.  
3. En el campo **N.º**, seleccione la serie de números que se usará para crear una identificación para el envío.  
4. En el campo **Código de ubicación**, elija el almacén desde el que realiza el envío. 

    Al recuperar las líneas del documento de origen, se copia parte de la información desde el almacén en cada línea.  
5. Si el almacén requiere ubicaciones, rellene el campo **Código de ubicación** . Dependiendo de su configuración, [!INCLUDE[prod_short](includes/prod_short.md)]] puede agregar el código de ubicación por usted. Obtenga más información en [Códigos de zona y de ubicación](warehouse-how-ship-items.md#zone-and-bin-codes).  
6. Puede obtener el documento de origen de dos maneras:

    * Seleccione la acción **Traer doc. origen**. Se abre la página **Documentos origen: Salida**. Aquí puede seleccionar uno o más documentos de origen enviados al almacén que requieren envío.
    * Elija la acción **Utiliz. filt. para traer docs.**. Se abre la página **Filtros para traer docs. orig.** Puede seleccionar el filtro del documento de origen y aplicarlo. Todas las líneas del documento de origen liberadas que cumplen los criterios de filtro se agregan en la página **Envío de almacén** . Obtenga más información en [Cómo utilizar filtros para traer documentos de origen](warehouse-how-ship-items.md#how-to-use-filters-to-get-source-documents).

    > [!NOTE]
    > Si el almacén utiliza tránsito directo y ubicaciones, para cada línea, puede revisar la cantidad de productos colocados en las ubicaciones de tránsito directo. [!INCLUDE [prod_short](includes/prod_short.md)] calcula las cantidades automáticamente cada vez que se actualicen los campos en el envío. Si son los productos del envío que está preparando, puede crear un picking de todos los productos y, a continuación, completar el envío. Obtenga más información en [Productos de tránsito directo](warehouse-how-to-cross-dock-items.md).

7. Cree un picking de almacén. Si el almacén requiere picking, puede crear actividades de picking para envíos de almacén de una de dos maneras:

    * De forma automática, donde utiliza la acción **Crear selección**. Seleccione las líneas para elegir y especifique información sobre las selecciones. Por ejemplo, de qué ubicaciones tomar y en cuáles colocar, y cuántas unidades manejar. Las ubicaciones se pueden predefinir para la ubicación del almacén o el recurso.
    * De forma pull, donde utiliza la acción **Liberar**. En la página **Hoja trabajo picking** , use la acción **Traer documentos almacén** para obtener las selecciones asignadas. Cuando los picking de almacén están totalmente registrados, se eliminan las líneas en **Hoja trabajo picking**. Obtenga más información en [Realizar un picking de los artículos para el envío de almacén](warehouse-how-to-pick-items-for-warehouse-shipment.md).

    > [!TIP]
    > Para un almacén que no requiere picking, puede imprimir el envío del almacén y usarlo como una lista de picking.

8. Especifique la cantidad que se enviará.  

    Para una ubicación que requiere picking, el campo **Cdad. a enviar** se actualiza automáticamente cuando se registra el picking. De lo contrario, el campo **Cantidad a enviar** se rellena con la cantidad pendiente de cada línea cuando se crea la línea de envío de almacén.

    Puede cambiar la cantidad, pero no puede enviar más productos que el número en el campo **Cdad. pendiente** en la línea del documento de origen o en el campo **Cdad. preparada pedido** si se requiere selección.

    Para establecer el valor en el campo **Cdad. a enviar** de todas las líneas en cero, elija la acción **Eliminar cdad. a enviar**. Por ejemplo, establecer las cantidades en cero es útil si está utilizando un escáner de código de barras para actualizar las cantidades enviadas. Para agregar la cantidad disponible para el envío, elija la acción **Rellenar cdad. a enviar autom.**

9. Registre el envío.

    [!INCLUDE [preview-posting-shipment](includes/preview-posting-shipment.md)]

## <a name="how-to-use-filters-to-get-source-documents"></a>Cómo utilizar filtros para obtener documentos de origen

Desde un envío de almacén, puede utilizar la página **Filtros para traer docs. orig.** para recuperar las líneas del documento de origen lanzado que definen los productos para recibir o enviar.

1. En el envío de almacén, elija la acción **Utiliz. filt. para traer docs.**. 
2. Para configurar un nuevo filtro introduzca un código descriptivo en el campo **Código** y, a continuación, elija la acción **Modificar**.

    Se abrirá la página **Ficha filtro documento origen - Saliente**.

3. Utilice los filtros para definir el tipo de líneas del documento de origen que desea recuperar. Por ejemplo, puede seleccionar tipos de documentos de origen, como pedidos de venta o de transferencia.
4. Elija **Ejecutar**.  

Todas las líneas del documento original liberado que cumplan los criterios de filtrado se añaden en la página **Envío almacén** en la que haya establecido los filtros.

Puede crear un número ilimitado de combinaciones de filtros. Los filtros se guardan en la página **Filtros para traer docs. orig.** y están disponibles la próxima vez que las necesite. Puede modificar los criterios en cualquier momento eligiendo la acción **Modificar**.

## <a name="zone-and-bin-codes"></a>Códigos de zona y ubicación

Si los contenedores son obligatorios en la ubicación, [!INCLUDE [prod_short](includes/prod_short.md)] sugiere una zona y un código de ubicación en el documento de envío del almacén.

* Para configuraciones avanzadas en las que el almacén utiliza un almacén y picking dirigidos,  [!INCLUDE [prod_short](includes/prod_short.md)] utiliza la ubicación especificada en el campo **Cód. ubicación envío** en el campo **Ficha de almacén**. Si no se especifica un **Cód. ubicación envío**, el campo está en blanco. Si el producto y la ubicación de envío no coinciden, [!INCLUDE [prod_short](includes/prod_short.md)] deja la ubicación de envío en blanco.
* En otros casos, [!INCLUDE [prod_short](includes/prod_short.md)] siempre utiliza la ubicación especificada en el campo **Cód. ubicación envío** de la **Ficha almacén** primero. Si no se especifica un código de ubicación de envío, [!INCLUDE [prod_short](includes/prod_short.md)] usa el código de ubicación del documento de origen.

## <a name="handling-assemble-to-order-items-in-warehouse-shipments"></a>Tratamiento de productos ensamblar para pedido en los envíos de almacén

En escenarios de ensamblar para pedido, use el campo **Cdad. a enviar** de las líneas de envío de almacén para registrar cuántas unidades se ensamblan. La cantidad se registra como salida de ensamblado cuando se registra el envío de almacén. Para las demás líneas de envío de almacén, el valor del campo **Cdad. a enviar** es cero.

Cuando los trabajadores terminan de montar parte o toda la cantidad de ensamblar para pedido, la registran en el campo **Cdad. a enviar** de la línea de envío de almacén. A continuación, elija la acción **Registrar envío**. La salida de ensamblado se contabiliza, incluido el consumo de componentes. Un envío de venta para la cantidad se registra para el pedido de venta.

Desde el pedido de ensamblado, puede elegir **Lín. envío almacén ensamblar para pedido** para acceder a la línea de envío de almacén.

Una vez registrado el envío de almacén, los distintos campos de la línea de pedido de venta se actualizan para mostrar el progreso en el almacén. Los siguientes campos también se actualizan para mostrar cuántas cantidades de ensamblar para pedido faltan ensamblar y enviar:

* **Cdad. pdte. almacén de ATO**
* **Cdad. pdte. salida alm. de ATO**

> [!NOTE]
> En escenarios de combinación, en los que una parte de la cantidad debe ensamblarse y la otra se debe enviar desde el inventario, se crean dos líneas de envío de almacén. Uno es para la cantidad de ensamblar para pedido y otro es para la cantidad de existencias.
>
> La cantidad ensamblada para pedido se maneja como se describe en este artículo. La cantidad de inventario se maneja como una línea de envío de almacén regular. Para obtener más información sobre los escenarios de combinación, vaya a [Comprender Ensamblar para pedido y Ensamblar para stock](assembly-assemble-to-order-or-assemble-to-stock.md).

## <a name="see-related-microsoft-training"></a>Consultar la [formación de Microsoft](/training/modules/ship-invoice-items-dynamics-365-business-central/) relacionada.

## <a name="see-also"></a>Consulte también .

[Inventario](inventory-manage-inventory.md)  
[Configuración de Warehouse Management](warehouse-setup-warehouse.md)  
[Gestión de ensamblaje](assembly-assemble-items.md)  
[Información general de la gestión de almacenes](design-details-warehouse-management.md)
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
