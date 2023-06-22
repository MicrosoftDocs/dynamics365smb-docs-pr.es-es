---
title: Realizar picking de productos con picking inventario
description: Obtenga información sobre cómo usar pickings de inventario para registrar y publicar información de picking y envío para documentos de origen.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 01/25/2023
ms.custom: bap-template
ms.search.forms: '931, 7377'
---
# <a name="pick-items-with-inventory-picks" />Realizar el picking de productos con picking inventario

En [!INCLUDE[prod_short](includes/prod_short.md)], la selección y el envío de productos se realizan mediante uno de los cuatro métodos, como se describe en la siguiente tabla.

|Método|Proceso de salida|Picking requerido|Envío requerido|Nivel de complejidad (Obtenga más información en [Descripción general de la gestión de almacenes](design-details-warehouse-management.md))|  
|------|----------------|-----|---------|-------------------------------------------------------------------------------------|  
|A|Registro de picking y envío desde la línea de pedido|||No hay ninguna actividad de almacén dedicada.|  
|B|Registro de picking y envío desde un documento de picking de existencias|Activado||Básico: Pedido por pedido|  
|P|Registro de picking y envío desde un documento de envío de almacén||Activado|Básico: Publicación consolidada de recepción/envío para múltiples pedidos.|  
|D|Registro de picking desde un documento de picking de almacén y registro de envío de un documento de envío de almacén|Activado|Activado|Avanzado|  

Obtenga más información en [Flujo de salida del almacén](design-details-outbound-warehouse-flow.md).

Este artículo hace referencia al método B de la tabla.

Cuando su almacén está configurado para requerir proceso de picking, pero no de envío, se utiliza la página **Picking inventario** para registrar la información de picking y envío de sus documentos de origen. Los documentos de salida pueden ser pedidos de ventas, pedidos de devolución de compras y pedidos de transferencia de salida.

> [!NOTE]
> Las necesidades de componentes de orden de producción y ensamblado también representan documentos de origen salientes. Para obtener más información acerca de las órdenes de producción y ensamblado para los procesos internos, consulte [Detalles de diseño: Flujos de almacén internos](design-details-internal-warehouse-flows.md).
>
> Aunque los pedidos de servicio también son documentos de origen de salida, no admiten el nivel básico de complejidad de pedido por pedido.
>
> Cuando se realiza el picking y envío de cantidades de línea de ventas que en están ensambladas al pedido, debe seguir ciertas reglas a la hora de crear las líneas de picking de inventario. Obtenga más información en [Tratamiento de productos de ensamblar para pedido con los picking de inventario](#handling-assemble-to-order-items-with-inventory-picks).  

Puede crear un picking de inventario de tres formas:

* Cree el picking de inventario directamente desde el documento de origen.  
* Cree pickings de inventario para varios documentos de origen al mismo tiempo mediante un trabajo por lotes.
* Solicite el picking en dos pasos; para ello, libere primero el documento de origen, que actúa como una señal para el almacén de que el documento de origen está preparado para el picking.

A continuación, se puede crear el picking de inventario en la página **Picking inventario** según el documento de origen.  

## <a name="to-create-an-inventory-pick-from-the-source-document" />Para crear un picking de inventario desde el documento de origen

1. En el documento de origen, que puede ser un pedido de ventas, un pedido de devolución de compras o un pedido de transferencia de salida, elija la acción **Crear ubicac. invent./picking**.
2. Seleccione la casilla **Crear picking de inventario**.  
3. Elija el botón **Aceptar**. Se creará un nuevo picking de inventario.

## <a name="to-create-multiple-inventory-picks-with-a-batch-job" />Para crear varios picking de inventario con un trabajo por lotes

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Crear almacenamiento/picking/movimiento de inventario** y, a continuación, elija el vínculo relacionado.  
2. En la ficha desplegable **Solicitud almacén**, use los campos **Documento origen** y **Cód. procedencia mov.** para filtrar determinados tipos de documentos o intervalos de números de documento. Por ejemplo, puede crear picking solo de los pedidos de venta.  
3. En la ficha desplegable **Opciones**, seleccione la casilla **Crear picking de inventario**.
4. Elija el botón **Aceptar**.

## <a name="to-create-the-pick-in-two-steps" />Para crear el picking en dos pasos

### <a name="to-request-an-inventory-pick-by-releasing-the-source-document" />Para solicitar un picking de inventario lanzado el documento de origen

En el caso de pedidos de venta, pedidos de devolución de compra y pedidos de transferencia de salida, para crear la solicitud de almacén, lance el pedido. La liberación del pedido hace que los productos estén disponibles para el picking.

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Pedidos de venta** y, a continuación, elija el vínculo relacionado.
2. Seleccione el pedido de venta que desea lanzar, y después seleccione **Lanzar**.

### <a name="to-create-an-inventory-pick-based-on-the-source-document" />Para crear un picking de inventario basado en el documento de origen

Después de liberar un pedido, el empleado del almacén puede crear un picking de inventario.

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Picking inventario** y luego elija el enlace relacionado.  
2. Seleccione la acción **Nuevo**.  
3. En el campo **Documento origen**, seleccione el tipo de documento en el que está realizando el picking.  
4. En el campo **Cód. procedencia mov.**, seleccione el documento de origen.  
5. También, elija la acción **Traer documento origen** para crear una lista de todos los documentos de origen de salida que están preparados para el picking en el almacén.  
6. Elija el botón **Aceptar** para rellenar las líneas de picking según los documentos de origen seleccionados.  

## <a name="to-record-inventory-picks" />Para registrar pickings de inventario

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Picking inventario** y luego elija el enlace relacionado.  
2. En las líneas de picking del campo **Cód. ubicación**, la ubicación desde la cual se debe realizar el picking de productos se sugiere como la ubicación predeterminada del artículo. Si es necesario puede cambiar la ubicación en esta página.  
3. Realice el picking e introduzca la cantidad en el campo **Cdad. a manipular**.

    Si debe realizar el picking de los producto para una línea de más de una ubicación, por ejemplo porque no está toda la cantidad en la ubicación, utilice la acción **Dividir línea** de la ficha desplegable **Líneas**. La acción crea una línea la cantidad restante que se debe administrar.

4. Seleccione la acción **Registrar**.  

    * Registre el envío de las líneas del documento de origen donde se realizó el picking.
    * Si el almacén utiliza ubicaciones, el registro también creará movimientos de almacén para registrar los cambios en la cantidad de la ubicación.  

## <a name="handling-assemble-to-order-items-with-inventory-picks" />Tratamiento de productos de ensamblar para pedido con pickings de inventario

Puede utilizar la página **Picking de inventario** para realizar el picking y envíos para ventas cuando los productos se deben ensamblar antes de que se puedan enviar. Obtenga más información en [Venta de artículos ensamblados para pedido](assembly-how-to-sell-items-assembled-to-order.md).

Los productos de ensamblar para pedido que no están presentes físicamente en una ubicación hasta que se ensamblan y se registran como salida en una ubicación. Realizar el picking de productos de ensamblar para pedido para envíos sigue un flujo especial.

1. De una ubicación, los empleados del almacén toman los productos de ensamblado al muelle de envío y después registran el picking de inventario.
2. El picking de inventario registrado registra la salida de ensamblado, el consumo de componentes y el albarán de venta.

Puede configurar [!INCLUDE[prod_short](includes/prod_short.md)] para que cree automáticamente un movimiento de inventario cuando el picking de inventario para el producto del ensamblado se crea. Seleccione el campo **Crear movimientos automáticamente** en la página **Conf. ensamblado**. Obtenga más información en [Configurar almacenes básicos con áreas de operaciones](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md).

Las líneas de picking de existencias se crean de diferentes modos en función de que no se ensamble ninguna, alguna o toda la cantidad de línea de venta para pedido. En escenarios donde parte de la cantidad se ensambla primero y a otra se le realiza el picking desde el inventario, se crea un mínimo de dos líneas de picking.

En las ventas cuya cantidad total de la línea de pedido de venta se ensambla para pedido, una línea de picking de inventario se crea para esa cantidad. Este valor del campo **Cantidad a ensamblar** es igual al valor del campo **Cdad. a enviar**. El campo **Ensamblar para pedido** está seleccionada en la línea.

Si no se configura ningún flujo de salida de ensamblado para el almacén, el campo **Cód. ubicación** de la línea de picking de inventario contiene el valor de los siguientes campos y en el orden que se indica a continuación.

* ***Cód. ubic. ens.contra-pedido** <!-- not applicable for inv pick-->
* **Cód. ubic. desde ensamblado**

Si no se especifica ningún código de ubicación de la línea de pedido de venta, y no se configura ningún flujo de salida de ensamblado para el almacén, el campo **Cód. ubicación** de la línea de picking de inventario está vacío. El empleado del almacén debe abrir la página **Contenidos ubicación** y seleccionar el almacén donde se ensamblan los productos de ensamblado.

En escenarios donde parte de la cantidad se ensambla primero y a la otra se le debe realizar el picking, se crea un mínimo de dos líneas de picking.

* Una línea de picking es para la cantidad de ensamblado para pedido. [!INCLUDE [prod_short](includes/prod_short.md)] utiliza los siguientes campos, en este orden, para determinar el código de ubicación: **Código de ubicación**, **Cód. ubic. ens.contra-pedido** y, después, **Cód. ubic. desde ensamblado**. Si estos campos están vacíos, el empleado del almacén debe abrir la página **Contenidos de ubicación** y elegir el almacén donde se ensamblan los productos de ensamblado.  
* La otra línea de picking depende de qué ubicación pueden cubrir la cantidad pendiente. Si el producto se guarda en varias ubicaciones, se crearán varias líneas. Esta línea Traer se basa en la cantidad en el campo **Cantidad a enviar**.

> [!NOTE]  
> Si los productos se ensamblan según el pedido, el picking de inventario para el pedido de ventas vinculado crea un movimiento de inventario para todos los componentes del ensamblado.  

## <a name="see-related-microsoft-trainingtrainingpathspick-ship-items-business-central" />Consultar la [formación de Microsoft](/training/paths/pick-ship-items-business-central/) relacionada

## <a name="see-also" />Consulte también .

[Información general de la gestión de almacenes](design-details-warehouse-management.md)
[Inventario](inventory-manage-inventory.md)  
[Configuración de Warehouse Management](warehouse-setup-warehouse.md)  
[Gestión de ensamblaje](assembly-assemble-items.md)  
[Tutorial: Picking y envío en la configuración del almacenamiento básico](walkthrough-picking-and-shipping-in-basic-warehousing.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
