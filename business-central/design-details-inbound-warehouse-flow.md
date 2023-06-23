---
title: 'Detalles de diseño: Flujo de entrada en almacén'
description: El flujo del almacén de entrada comienza cuando los artículos llegan al almacén de la empresa y se registran y comparan con los documentos de origen de entrada.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 11/14/2022
ms.author: bholtorf
---
# <a name="design-details-inbound-warehouse-flow" />Detalles de diseño: Flujo de entrada en almacén

El flujo de entrada de un almacén comienza cuando los productos llegan al almacén de la ubicación de empresa, recibidos de orígenes externos o de otra ubicación de empresa. En principio, el proceso de recepción de pedidos entrantes consta de dos actividades:

* Reciba los artículos en el muelle de recepción del almacén, donde los identifica, los relaciona con un documento de origen y registra la cantidad recibida. 
* Guarde los artículos en stock y registre el lugar donde los colocó.

Los documentos de origen para el flujo de almacén de entrada son:

* Pedidos de compra  
* Pedidos de transferencia de entrada  
* Pedidos devolución de venta  

> [!NOTE]
> Las salidas de producción y ensamblado también representan documentos de origen de entrada. Obtenga más información acerca de las salidas de producción y ensamblado para los procesos internos en [Detalles de diseño: Flujos de almacén internos](design-details-internal-warehouse-flows.md).  

En [!INCLUDE[prod_short](includes/prod_short.md)], la recepción y la ubicación se realizan mediante uno de los cuatro métodos, como se describe en la siguiente tabla.

|Método|Proceso de salida|Recepciones requeridas|Ubicaciones requeridas|Nivel de complejidad (Obtenga más información en [Descripción general de la gestión de almacenes](design-details-warehouse-management.md))|  
|------------|---------------------|--------------|----------------|------------|  
|A|Registro de la recepción y ubicación desde la línea de pedido|||No hay ninguna actividad de almacén dedicada.|  
|B|Registro de la recepción y ubicación desde un documento de ubicación del inventario||Activado|Básico: Pedido por pedido|  
|P|Registro de la recepción y ubicación desde un documento de recepción de almacén|Activado||Básico: Publicación consolidada de recepción/envío para múltiples pedidos.|  
|D|Registro de la recepción desde un documento de recepción de almacén y registro de ubicación desde un documento de ubicación de almacén|Activado|Activado|Avanzado|  

La selección de un planteamiento depende de las prácticas de su empresa y del nivel de su complejidad organizativa. Los siguientes son algunos ejemplos que pueden ayudarlo a decidir.

* En un entorno de almacén pedido por pedido, donde la mayoría del personal del almacén trabaja directamente con los documentos de pedido, puede decidir utilizar el método A. 
* Un almacén pedido por pedido que tiene un proceso de ubicación más complejo, o donde el personal del almacén separa sus actividades de ubicación del documento de pedido, podría usar el método B.
* Las empresas que necesitan planificar el manejo de varios pedidos pueden encontrar útil utilizar documentos de recibo de almacén, métodos C y D.  

En los métodos A, B y C, la recepción y ubicación se agrupan en un paso al registrar los documentos como recibidos. En el método D, se registra primero la recepción para registrar la entrada de existencias y que hay productos disponibles para su venta. A continuación, el empleado de almacén registra la ubicación a fin de que los productos estén disponibles para picking para los pedidos salientes. 

> [!NOTE]
> Si bien las ubicaciones de almacén y las ubicaciones de inventario suenan similares, son documentos diferentes y se utilizan en procesos diferentes.
> * El almacenamiento de inventario utilizado en el método B, junto con el registro de la información de almacenamiento, también contabiliza la recepción del documento de origen.
> * La ubicación de almacén utilizada en el método D no se puede contabilizar y solo registra la ubicación. El registro hace que los artículos estén disponibles para el procesamiento posterior, pero no contabiliza el recibo. En el flujo de entrada, la ubicación en almacén requiere un recibo de almacén.

## <a name="no-dedicated-warehouse-activity" />No hay ninguna actividad de almacén dedicada

Los siguientes artículos brindan información sobre cómo procesar recibos para documentos de origen si no tiene actividades de almacén dedicadas.

* [Registrar compras](purchasing-how-record-purchases.md)
* [Pedidos de transferencia](inventory-how-transfer-between-locations.md)
* [Procesar devoluciones de ventas](sales-how-process-sales-returns-orders.md)

## <a name="basic-warehouse-configurations" />Configuraciones básicas de almacén

En una configuración de almacén básica, el conmutador **Requerir ubicación** está activado, pero el conmutador **Requerir recibo** está activado. desactivado en la página Tarjeta de ubicación para la ubicación.

En el diagrama siguiente se ilustran los flujos de almacén de entrada por tipo de documento en la configuración básica de almacén. Los números del diagrama corresponden a los pasos de las secciones que siguen el diagrama.  

:::image type="content" source="media/design_details_warehouse_management_inbound_basic_flow.png" alt-text="El flujo de entrada básico en un almacén.":::

### <a name="1-release-a-source-document-to-create-a-request-for-an-inventory-put-away" />1: Liberar un documento de origen para crear una solicitud de ubicación de inventario

Cuando reciba artículos, libere el documento de origen, como una orden de compra o una orden de transferencia entrante. Al liberar el documento, los artículos quedan disponibles para su ubicación. También puede crear mediante envío documentos de ubicación de inventario para líneas de pedido particulares, en función de las ubicaciones especificadas y de las cantidades que gestionar.  

### <a name="2-create-an-inventory-put-away" />2: Crear una ubicación de inventario

En la página **Ubicación inventario**, mediante extracción, puede obtener las líneas pendientes del documento de origen basándose en las solicitudes de entrada al almacén. De manera automática, también puede crear líneas de ubicación de inventario cuando crea el documento de origen.  

### <a name="3-post-an-inventory-put-away" />3: Registrar un almacenamiento de inventario

En cada línea de los productos que se han ubicado, parcial o totalmente, rellene el campo **Cantidad** y, a continuación, registre la ubicación de inventario. Los documentos de origen que están relacionados con la ubicación de inventario se registran como recibidos.  

* Se crean movimientos de producto positivos
* Las entradas de almacén se crean para ubicaciones que requieren un código de ubicación en todas las transacciones de artículos.
* La solicitud de ubicación se elimina, si se gestiona por completo. Por ejemplo, se actualiza el campo **Cantidad recibida** en la línea de entrada del documento de origen.
* Se crea un documento de recepción registrada que refleja el pedido de compra, por ejemplo, y los productos recibidos.  

## <a name="advanced-warehouse-configurations" />Configuración avanzada de almacén

En una configuración de almacén avanzada, el interruptor **Requerir recibo** está activado en la página Tarjeta de ubicación para la ubicación. El conmutador **Ubicación requerida** es opcional.

En el diagrama siguiente se ilustran los flujos de almacén de entrada por tipo de documento. Los números del diagrama corresponden a los pasos de las secciones que siguen el diagrama.  

:::image type="content" source="media/design_details_warehouse_management_inbound_advanced_flow.png" alt-text="Flujo de entrada avanzado en un almacén.":::

### <a name="1-release-the-source-document" />1: Lanzar el documento de origen

Cuando reciba artículos, libere el documento de origen, como una orden de compra o una orden de transferencia entrante. Al liberar el documento, los artículos quedan disponibles para su ubicación. El almacenamiento contendrá referencias al tipo y el número de documento de origen.

### <a name="2-create-a-warehouse-receipt" />2: Crear una recepción de almacén

Obtenga las líneas del documento de origen de entrada en la página **Recep. almacén**. Puede combinar varias líneas del documento de origen en un documento de recepción de almacén. Rellene el campo **Cdad. a manipular** y seleccione la zona y la ubicación de recepción, si procede.  

### <a name="3-post-the-warehouse-receipt" />3: Registrar la recepción de almacén

Registre la recepción de almacén para crear los movimientos de producto positivos. El campo **Cantidad recibida** en la línea de entrada del documento de origen se actualiza.  

Si el interruptor **Requerir ubicación** no está activado en la tarjeta de ubicación, aquí es donde se detiene el proceso. De lo contrario, al registrar el documento de origen de entrada, los artículos quedan disponibles para su ubicación. El almacenamiento contiene referencias al tipo y el número de documento de origen.  

### <a name="4-optional-generate-put-away-worksheet-lines" />4: (Opcional) Generar líneas de hoja de trabajo de ubicación

Obtenga las líneas de ubicación del almacén en la **Hoja de trabajo de ubicación** basándose en los recibos de almacén registrados o en las operaciones que generan resultados. Elija las líneas para ubicar y especifique la siguiente información:

* Los contenedores para tomar artículos.
* Las ubicaciones para colocar los productos.
* Cuantas unidades manejar.

Las ubicaciones se pueden predefinir mediante la configuración de la ubicación de almacén o el recurso que realizó la operación.  

Cuando todas las ubicaciones se planifican y asignan a empleados de almacén, genere los documentos de ubicación de almacén. Las líneas con ubicación totalmente asignada se eliminan de **Hoja trabajo ubicación**.  

> [!NOTE]  
> Si el control de alternancia **Utilizar hoja trabajo ubicación** no se ha activado en la ficha de almacén, los documentos de ubicación en almacén se crean directamente de acuerdo con las recepciones de almacén registradas. En ese caso, este paso no es necesario.  

### <a name="5-create-a-warehouse-put-away-document" />5: Crear un documento de almacenamiento de almacén

Cree un documento de ubicación de almacén de forma pull, en función del recibo de almacén registrado. Alternativamente, cree el documento de ubicación de almacén y asígnelo a un trabajador de almacén mediante envío.  

### <a name="6-register-a-warehouse-put-away" />6: Registrar una ubicación de almacén

En cada línea de los productos que se han ubicado, parcial o totalmente, rellene el campo **Cantidad** en la página **Ubicación almacén** y, a continuación, registre la ubicación de almacén.  

* Las entradas de almacén se crean para ubicaciones que requieren un código de ubicación en todas las transacciones de artículos.
* Las líneas de ubicación de almacén, si se han manipulado por completo, se eliminan.
* El documento de ubicación de almacén permanecerá abierto hasta que se registre la cantidad total de la recepción de almacén registrada relacionada.
* El campo **Cantidad a ubicar** de las líneas de pedido de recepción de almacén registradas se actualiza.

## <a name="related-tasks" />Tareas relacionadas

En la tabla siguiente se indican una serie de tareas con vínculos a los temas que las describen.

|**Para**|**Vea**|  
|------------|-------------|  
|Registre la recepción de productos en las ubicaciones del almacén o con un recibo de almacén, en caso de procesamiento semi o totalmente automatizado del almacén en la ubicación.|[Recibir productos](warehouse-how-receive-items.md)|
|Ubique los productos pedido a pedido y registre la recepción como parte de la misma actividad, en configuraciones básicas de almacén.|[Ubicar productos con ubicación de inventario](warehouse-how-to-put-items-away-with-inventory-put-aways.md)|  
|Ubique los productos recibidos de múltiples compras, devoluciones de ventas, órdenes de transferencia en una configuración de almacén avanzada.|[Ubicar productos con ubic. exist. almacén](warehouse-how-to-put-items-away-with-warehouse-put-aways.md)|  


## <a name="see-also" />Consulte también

[!INCLUDE[footer-include](includes/footer-banner.md)]
