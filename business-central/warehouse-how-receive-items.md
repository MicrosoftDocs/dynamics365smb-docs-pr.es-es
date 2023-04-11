---
title: Recibir productos
description: 'Este artículo ofrece una descripción general de las diferentes formas de recibir productos en un almacén, por ejemplo con un recibo de almacén.'
author: brentholtorf
ms.author: bholtorf
ms.topic: how-to
ms.date: 09/02/2022
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '5768, 7330, 7332, 7333, 7342, 7363, 8510, 9008'
---
# Recibir productos con recepción de almacén

En [!INCLUDE[prod_short](includes/prod_short.md)], la recepción y la ubicación se realizan mediante uno de los cuatro métodos, como se describe en la siguiente tabla.

|Método|Proceso de salida|Recepciones requeridas|Ubicaciones requeridas|Nivel de complejidad (Obtenga más información en [Descripción general de la gestión de almacenes](design-details-warehouse-management.md))|  
|------------|---------------------|--------------|----------------|------------|  
|A|Registro de la recepción y ubicación desde la línea de pedido|||No hay ninguna actividad de almacén dedicada.|  
|B|Registro de la recepción y ubicación desde un documento de ubicación del inventario||Activado|Básico: Pedido por pedido|  
|P|Registro de la recepción y ubicación desde un documento de recepción de almacén|Activado||Básico: Publicación consolidada de recepción/envío para múltiples pedidos.|  
|D|Registro de la recepción desde un documento de recepción de almacén y registro de ubicación desde un documento de ubicación de almacén|Activado|Activado|Avanzado|  

Para obtener más información sobre cómo manejar productos entrantes, vaya a [Flujo de entrada en almacén](design-details-inbound-warehouse-flow.md).

El siguiente artículo hace referencia a los métodos C y D de la tabla anterior.

## Recibir productos con recibo de almacén

Cuando los productos llegan a un almacén que está configurado para procesar recepciones de almacén, debe obtener las líneas del documento de origen liberado que desencadenó la recepción. Si usa ubicaciones, puede aceptar la ubicación predeterminada o especificar la ubicación para colocar los productos. Este último puede ser necesario cuando recibe un producto por primera vez. A continuación, rellene las cantidades de los productos que ha recibido y registre la recepción.  

Puede crear una recepción de almacén de dos maneras:

* De manera forzada, cuando el trabajo se realiza pedido por pedido. Elija la acción **Crear recepción de almacén** en el documento de origen, como Pedido de compra, Pedido de devolución de venta o Pedido de transferencia para crear una recepción de almacén para un documento de origen.
* De manera forzada, cuando se utiliza la acción **Liberar** en el documento de origen, como un pedido de compra, una orden de devolución de ventas o un pedido de transferencia para liberar el documento al almacén. Un empleado de almacén crea una **Recepción de almacén** para uno o varios documentos de origen emitidos. El siguiente procedimiento describía cómo crear un recibo de almacén de manera forzada. El siguiente procedimiento describe cómo crear una recepción de almacén de manera forzada.

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Recepciones almacén** y luego elija el enlace relacionado.  
2. Seleccione la acción **Nuevo**.  

    Rellene el campo **Código de almacén** en la ficha desplegable **General**. Al recuperar las líneas del documento de origen, se copia parte de la información en cada línea.

    Para un almacén que requiera ubicaciones, rellene el campo **Código de ubicación** . Dependiendo de su configuración, [!INCLUDE[prod_short](includes/prod_short.md)] puede agregar el código del código de ubicación por usted. Obtenga más información en [Códigos de zona y de ubicación](warehouse-how-receive-items.md#zone-and-bin-codes).  

3. Puede obtener documentos de origen de dos maneras:

    1. Seleccione la acción **Traer doc. origen**. Se abre la página **Documentos origen: Entrada**. Aquí puede seleccionar uno o más documentos de origen enviados al almacén que requieren recepción.
    2. Elija la acción **Utiliz. filt. para traer docs.**. Se abre la página **Filtros para traer docs. orig. - Entrada**. Aquí puede seleccionar el Filtro de documento de origen y ejecutarlo. Todas las líneas del documento de origen liberadas que cumplen los criterios de filtro se agregan en la página **Recepción de almacén** . Obtenga más información en [Cómo utilizar filtros para traer documentos de origen](warehouse-how-receive-items.md#how-to-use-filters-to-get-source-documents).

4. Establece la cantidad a recibir.

    El campo **Cantidad a recibir** contiene la cantidad pendiente de cada línea, pero puede cambiarla según necesite. 

    Para establecer el valor en el campo **Cdad. para recibir** de todas las líneas en cero, elija la acción **Eliminar cdad. a recibir**. Por ejemplo, establecer las cantidades en cero es útil si está utilizando un escáner de código de barras para actualizar las cantidades recibidas. Para volver a agregar las cantidades pendientes del documento de origen, seleccione la acción **Rellenar cdad. a recibir aut.**  

    En un documento de recepción de almacén donde la cantidad recibida sea mayor que la ordenada, introduzca la cantidad realmente recibida en el campo **Cantidad para recibir**. Si el aumento está dentro de la tolerancia especificada por un código de recepción en exceso asignado, el campo **Cantidad de recepción en exceso** se actualiza para mostrar la cantidad en la que se excede el valor del campo **Cantidad**. Si el aumento está por encima de la tolerancia, no se permite la recepción en exceso.

5. Registre la recepción de almacén. Los campos de cantidad se actualizan en el documento de origen y los productos se agregan a las existencias.  

    [!INCLUDE [preview-posting-shipment](includes/preview-posting-shipment.md)]

    > [!TIP]
    > Si usa el almacenamiento del almacén, que se refiere al método D en la tabla al principio de este artículo, los productos se reciben pero no se pueden recolectar hasta que se hayan almacenado. Para obtener más información sobre cómo almacenar productos, vaya a [Ubicar productos con ubic. exist. almacén](warehouse-how-to-put-items-away-with-warehouse-put-aways.md).
    >
    > De lo contrario, considere usar la acción **Registrar e Imprimir**. La acción registrará el recibo y lo imprimirá como una instrucción de ubicación que muestra dónde colocar el producto.

    > [!NOTE]  
    > Si su almacén utiliza tránsito directo, puede comprobar si puede realizar el tránsito directo de productos sin almacenarlos. Para obtener más información sobre el tránsito directo, vaya a [Productos de tránsito directo](warehouse-how-to-cross-dock-items.md).

## Cómo utilizar filtros para obtener documentos de origen

Desde una recepción de almacén, puede utilizar la página **Filtros para traer docs. orig.** para recuperar las líneas del documento de origen lanzado que especifican los productos para recibir.

1. En la recepción de almacén, elija la acción **Utiliz. filt. para traer docs.**.
2. Para configurar un nuevo filtro introduzca un código descriptivo en el campo **Código** y, a continuación, elija la acción **Modificar**.

    Aparecerá la página **Ficha filtro documento origen - Entrante**.

3. Utilice los filtros para definir el tipo de líneas del documento de origen que desea recuperar. Por ejemplo, puede seleccionar tipos de documentos de origen, como pedidos de compra o de transferencia.
4. Elija **Ejecutar**.  

Todas las líneas del documento original liberado que cumplan los criterios de filtrado se añaden en la página **Recepción almacén** en la que haya activado los filtros.

Puede crear un número ilimitado de combinaciones de filtros. Los filtros se guardan en la página **Filtros para traer docs. orig.** y están disponibles la próxima vez que las necesite. Puede modificar los criterios en cualquier momento eligiendo la acción **Modificar**.

## Códigos de zona y ubicación

Para recibir productos con códigos de clase de almacén de la ubicación en el campo **Cód. ubicación** de la cabecera de documento, elimine el campo **Cód. ubicación** en la cabecera antes de recuperar líneas del documento de origen para los productos.  
<!-- TBD, table with comparison of various options-->

Si las ubicaciones son obligatorias para un almacén, los códigos de zona y ubicación se agregan a los documentos de recepción de almacén de la siguiente manera:

* Para configuraciones avanzadas que usan ubicación y recolección dirigidas, [!INCLUDE [prod_short](includes/prod_short.md)] usa el código de ubicación de recepción de la página **Ficha almacén** para la ubicación. Si no se especifica un código de ubicación de recepción, no se especifica ninguna ubicación. Si el producto y las ubicaciones de recepción no coinciden, el código de ubicación de recepción está en blanco.
* En otras configuraciones, si no se especifica un código de ubicación de recepción, [!INCLUDE [prod_short](includes/prod_short.md)] usa el código de ubicación del documento de origen.

## Consultar la [formación de Microsoft](/training/modules/receive-invoice-dynamics-d365-business-central/index) relacionada.

## Consulte también .

[Información general de la gestión de almacenes](design-details-warehouse-management.md)
[Inventario](inventory-manage-inventory.md)  
[Configuración de Warehouse Management](warehouse-setup-warehouse.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
