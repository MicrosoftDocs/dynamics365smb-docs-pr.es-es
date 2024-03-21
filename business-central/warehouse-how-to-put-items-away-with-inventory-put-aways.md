---
title: Ubicación de productos con ubicación de inventario
description: Obtenga información sobre cómo utilizar los documentos de almacenamiento de inventario para registrar y publicar información de almacenamiento y recepción.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.date: 09/19/2023
ms.custom: bap-template
ms.search.forms: '7375,'
---
# Ubicar productos con ubicación de inventario

En [!INCLUDE[prod_short](includes/prod_short.md)], la recepción y la ubicación se realizan mediante uno de los cuatro métodos, como se describe en la siguiente tabla.

|Método|Proceso de salida|Recepciones requeridas|Ubicaciones requeridas|Nivel de complejidad (Obtenga más información en [Descripción general de la gestión de almacenes](design-details-warehouse-management.md))|  
|------------|---------------------|--------------|----------------|------------|  
|A|Registro de la recepción y ubicación desde la línea de pedido|||No hay ninguna actividad de almacén dedicada.|  
|B|Registro de la recepción y ubicación desde un documento de ubicación del inventario||Activado|Básico: Pedido por pedido|  
|P|Registro de la recepción y ubicación desde un documento de recepción de almacén|Activado||Básico: Publicación consolidada de recepción/envío para múltiples pedidos.|  
|D|Registro de la recepción desde un documento de recepción de almacén y registro de ubicación desde un documento de ubicación de almacén|Activado|Activado|Avanzado|  

Obtenga más información en [Flujo de entrada en almacén](design-details-inbound-warehouse-flow.md).

Este artículo hace referencia al método B de la tabla.

Cuando el almacén está configurado para requerir el proceso de ubicación, pero no el proceso de recepción, se utiliza un documento de **Almacenamiento de inventario** para registrar la información de almacenamiento y recepción de sus documentos de origen. Los documentos de entrada pueden ser pedidos de compra, pedidos de devolución de ventas y pedidos de transferencia de entrada.

> [!NOTE]
> Las salidas de producción y ensamblado también representan documentos de origen de entrada. Obtenga más información acerca de las salidas de producción y ensamblado para los procesos internos en [Detalles de diseño: Flujos de almacén internos](design-details-internal-warehouse-flows.md).

Puede crear una ubicación de inventario de tres formas:  

* Cree la ubicación de inventario directamente desde el propio documento de origen.  
* Cree los almacenamientos de inventario para varios documentos de origen al mismo tiempo mediante un trabajo por lotes.  
* Cree el almacenamiento en dos pasos, primero liberando el documento de origen para que los productos estén disponibles para su almacenamiento. Pude crear el almacenamiento de inventario en función del documento de origen usando la página **Almacenamiento de inventario**.  

## Para crear una ubicación de inventario desde el documento de origen

1. En el documento de origen, que puede ser un pedido de compras, un pedido de devolución de ventas o un pedido de transferencia de entrada, elija la acción **Crear almacenamiento/picking de inventario**.  
2. Seleccione la casilla **Crear almacenamiento de inventario**.
3. Elija el botón **Aceptar**. Se crea una ubicación de inventario nueva.

## Para crear varias Ubicaciones de existencias con un proceso

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Crear almacenamiento/picking/movimiento de inventario** y, a continuación, elija el vínculo relacionado. 
2. En la ficha desplegable **Solicitud almacén**, use los campos **Documento origen** y **Cód. procedencia mov.** para filtrar determinados tipos de documentos o intervalos de números de documento. Por ejemplo, puede crear almacenamientos solo para pedidos de compra.
3. En la ficha desplegable **Opciones**, seleccione la casilla **Crear almacenamiento de inventario**.
4. Elija el botón **Aceptar**. Se crean las ubicaciones de inventario especificadas.

## Para crear el almacenamiento de inventario en dos pasos

### Para solicitar una ubicación de inventario lanzando el documento de origen

Cuando libera pedidos de compra, pedidos de devolución de ventas y pedidos de transferencia de entrada, los productos de los pedidos quedan disponibles para su almacenamiento. Los siguientes pasos describen cómo hacer que los productos de un pedido de compra estén listos para el almacenamiento.  

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Pedidos de compra** y, a continuación, elija el vínculo relacionado.
2. Seleccione el pedido de compra que desea lanzar, y después seleccione **Lanzar**.  

### Para crear una ubicación de inventario según el documento de origen

Un empleado del almacén puede crear un nuevo almacenamiento de inventario basado en el documento de origen liberado.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Ubicación de inventario** y luego elija el enlace relacionado.  
2. Seleccione la acción **Nuevo**.  
3. En el campo **Documento origen**, seleccione el tipo de documento de origen que está ubicando.  
4. En el campo **Cód. procedencia mov.**, seleccione el documento de origen.  
5. También, elija la acción **Traer documento origen** para seleccionar un documento de una lista de documentos de origen de entrada que están preparados para la ubicación en el almacén.  
6. Elija el botón **Aceptar** para rellenar las líneas de ubicación según el documento de origen seleccionado.  

## Para registrar las ubicaciones de inventario

1. Abra un documento de almacenamiento creado previamente en la página **Almacenamiento de inventario**.  
2. En las líneas de almacenamiento del campo **Cód. de almacenamiento**, las ubicaciones donde los productos deben almacenarse se sugieren en función de la ubicación predeterminada del producto. Puede cambiar la ubicación si lo necesita.  
3. Lleve a cabo el almacenamiento e indique la información de la cantidad real que se almacenó en el campo **Cdad. a manipular**.

    Si es necesario colocar los productos para otra línea en varias ubicaciones porque la ubicación designada está completa, por ejemplo, utilice la acción **Dividir línea** en la ficha desplegable **Líneas**. La acción crea una línea la cantidad restante que se debe administrar.  
4. Después de almacenar los productos, elija la acción **Registrar**.  

    * Registrar la recepción de las líneas del documento de origen que se han guardado
    * Si el almacén utiliza ubicaciones, el registro también creará movimientos de almacén para registrar los cambios de cantidad en la ubicación.

    [!INCLUDE [preview-posting-warehouse](includes/preview-posting-warehouse.md)]

## Consulte también .

[Información general de la gestión de almacenes](design-details-warehouse-management.md)
[Inventario](inventory-manage-inventory.md)  
[Configuración de Warehouse Management](warehouse-setup-warehouse.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
