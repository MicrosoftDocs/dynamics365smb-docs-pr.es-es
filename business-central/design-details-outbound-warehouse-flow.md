---
title: Resumen de procesos de almacén salientes
description: Este artículo describe el flujo de trabajo del almacén de salida.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 11/25/2022
ms.custom: bap-template
---
# <a name="outbound-warehouse-processes" />Procesos de almacén salientes

Los procesos de salida en los almacenes comienzan cuando libera un documento de origen para sacar artículos de una ubicación de almacén. Por ejemplo, ya sea para enviar los artículos a algún lugar o para trasladarlos a otra ubicación de la empresa. En principio, el proceso de envío de pedidos salientes consta de dos actividades:

* Recogiendo artículos de los estantes.
* Envío de artículos fuera del almacén.

Los documentos de origen para el flujo de almacén de salida son:  

* Pedido de venta  
* Pedido de transferencia de salida  
* Pedido dev. compra  
* Pedido servicio  

> [!NOTE]
> Los pedidos de producción y ensamblaje con necesidades de componentes también representan documentos de origen salientes. Las órdenes de producción y ensamblaje son un poco diferentes porque normalmente son procesos internos que no involucran envíos. En su lugar, se utilizan para ubicar artículos producidos o mover los componentes necesarios para ensamblar un artículo a un área de ensamblaje. Obtenga más información sobre estos procesos en [Detalles de diseño: flujos internos de almacén](design-details-internal-warehouse-flows.md).  

En [!INCLUDE[prod_short](includes/prod_short.md)], la selección y el envío de productos se realizan mediante uno de los cuatro métodos, como se describe en la siguiente tabla.

|Método|Proceso de salida|Picking requerido|Envío requerido|Nivel de complejidad (Obtenga más información en [Descripción general de la gestión de almacenes](design-details-warehouse-management.md))|  
|------|----------------|-----|---------|-------------------------------------------------------------------------------------|  
|A|Registro de picking y envío desde la línea de pedido|||No hay ninguna actividad de almacén dedicada.|  
|B|Registro de picking y envío desde un documento de picking de existencias|Activado||Básico: Pedido por pedido|  
|P|Registro de picking y envío desde un documento de envío de almacén||Activado|Básico: Publicación consolidada de recepción/envío para múltiples pedidos.|  
|D|Registro de picking desde un documento de picking de almacén y registro de envío de un documento de envío de almacén|Activado|Activado|Avanzado|  

El enfoque que se elige depende de las prácticas de su almacén y del nivel de su complejidad organizativa. Los siguientes son algunos ejemplos que pueden ayudarlo a decidir.

* En un entorno de pedido por pedido con procesos directos y una estructura simple de ubicación, resulta apropiado el método A, selección y envío desde la línea de pedido.
* Si los artículos para una línea de pedido provienen de más de una ubicación, o si los trabajadores del almacén no pueden trabajar con documentos de pedido, es apropiado el uso de documentos de recolección separados, método B.
* Si sus procesos de selección y envío implican varios pedidos y requieren un mayor control y una visión general, puede optar por utilizar un documento de envío de almacén y un documento de selección de almacén para separar las tareas de selección y envío, métodos C y D.  

En los métodos A, B y C, las actividades de selección y envío se agrupan en un paso al registrar un documento como enviado. En el método D, primero registra la selección y después registra el envío desde otro documento.

> [!NOTE]
> Si bien las selecciones de almacén y las selecciones de inventario suenan similares, son documentos diferentes y se utilizan en procesos diferentes.
> * La selección de inventario utilizada en el método B, junto con el registro de la información de selección, también contabiliza el envío del documento de origen.
> * La selección de almacén utilizada en el método D no se puede contabilizar y solo registra la selección. El registro no registra el envío, sino que simplemente hace que los artículos estén disponibles para el envío. En el flujo de salida, la selección en almacén requiere un envío de almacén.

## <a name="no-dedicated-warehouse-activity" />No hay ninguna actividad de almacén dedicada

Los siguientes artículos brindan información sobre cómo procesar recibos para documentos de origen si no tiene actividades de almacén dedicadas.

* [Vender producto](sales-how-sell-products.md)
* [Pedidos de transferencia](inventory-how-transfer-between-locations.md)
* [Procesamiento de devoluciones de compra o cancelaciones](purchasing-how-process-purchase-returns-cancellations.md)
* [Crear pedidos de servicio](service-how-to-create-service-orders.md)

## <a name="basic-warehouse-configurations" />Configuraciones básicas de almacén

En el diagrama siguiente se ilustran los procesos de almacén de salida para diferentes tipos de documento en la configuración básica de almacén. Los números del diagrama corresponden a los pasos de las secciones que siguen el diagrama.  

:::image type="content" source="media/design-details-warehouse-management-outbound-basic-flow.png" alt-text="Muestra los pasos de un flujo de salida básico en un almacén.":::

### <a name="1-release-a-source-document" />1: Lanzar un documento de origen

Cuando utiliza la acción **Liberar** en un documento de origen, como una orden de venta o de transferencia, los artículos del documento están listos para manejarse en el almacén. Por ejemplo, seleccionar y colocar en la ubicación especificada en el documento. Alternativamente, puede crear documentos de selección de inventario para líneas de pedido particulares, en función de las ubicaciones especificadas y de las cantidades que gestionar.  

### <a name="2-create-an-inventory-pick" />2: Crear un picking de inventario

En la página **Selección de inventario**, el trabajador del almacén recupera, de manera pull, las líneas del documento de origen. Las líneas de selección de inventario las puede crear también mediante envío el usuario responsable del documento de origen.  

### <a name="3-post-an-inventory-pick" />3: Registrar un picking de inventario

En cada línea de los productos que se han seleccionado o movido, parcial o totalmente, rellene el campo **Cantidad** y, a continuación, registre la selección de inventario. Los documentos de origen relacionados con el picking de existencias se registran como enviados o consumidos.  

En el caso de selecciones de inventario, se crean movimientos de producto negativos y movimientos de almacén, así como se elimina la solicitud de selección si se ha gestionado íntegramente. Por ejemplo, se actualiza el campo **Cantidad enviada** en la línea de salida del documento de origen. Se crea un documento de envío registrado que refleja el pedido de venta, por ejemplo, y los productos enviados.  

## <a name="advanced-warehouse-configurations" />Configuración avanzada de almacén

En el diagrama siguiente se ilustran los procesos de almacén de salida para diferentes tipos de documento en la configuración avanzada de almacén. Los números del diagrama corresponden a los pasos de las secciones que siguen el diagrama.  

:::image type="content" source="media/design_details_warehouse_management_outbound_advanced_flow.png" alt-text="Muestra los pasos de un flujo de almacén de salida avanzado.":::

### <a name="1-release-a-source-document" />1: Lanzar un documento de origen

Liberar un documento de origen en configuraciones avanzadas hace lo mismo que para las configuraciones básicas. Los artículos pasan a estar disponibles para su manipulación en el almacén. Por ejemplo, se pueden incluir en un envío.  

### <a name="2-create-a-warehouse-shipment" />2: Crear un envío de almacén

Obtenga las líneas del documento de origen liberado en la página **Envío almacén**. Puede combinar líneas de varfios documentos de origen en un envío de almacén.  

### <a name="3-create-a-warehouse-pick" />3: Crear un picking de almacén

En la página **Envío de almacén**, cree actividades de selección de almacén para envíos de almacén de una de estas dos maneras:

- De forma automática, donde utiliza la acción **Crear selección**. Seleccione las líneas que se van a seleccionar y prepare los picking mediante la especificación, por ejemplo, de las ubicaciones de las que se tomarán, las ubicaciones en las que se colocarán y la cantidad de unidades que se manipularán. Las ubicaciones se pueden predefinir para la ubicación del almacén o el recurso.
- De forma pull, donde utiliza la acción **Liberar**. En la página **Hoja trabajo picking**, los empleados del almacén pueden usar la acción **Traer documentos almacén** para obtener los pickings asignados. Cuando los picking de almacén están totalmente registrados, se eliminan las líneas en **Hoja trabajo picking**.

### <a name="4-register-a-warehouse-pick" />4: Registrar una selección de almacén

En la página **Selección de almacén**, un empleado del almacén rellena el campo **Cantidad** de cada línea que han seleccionado parcial o totalmente y luego registra el picking del almacén.

Se crean movimientos de almacén y se eliminan las líneas de picking de almacén, si se ha seleccionado la cantidad completa. El documento de picking de almacén permanecerá abierto hasta que se registre la cantidad total del envío de almacén. El campo **Cdad. preparada pedido** de las líneas de albarán de almacén se actualiza como corresponde.  

### <a name="5-post-the-warehouse-shipment" />5: Registrar el envío de almacén

Cuando todos los productos del documento de envío de almacén están registrados como preparados para las ubicaciones de envío especificadas, el empleado de almacén registra el envío. La contabilización actualiza las entradas del libro mayor de artículos para reflejar la reducción en el inventario. Por ejemplo, se actualiza el campo **Cantidad enviada** en la línea de salida del documento de origen.  

## <a name="see-also" />Consulte también

[Warehouse Management](design-details-warehouse-management.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
