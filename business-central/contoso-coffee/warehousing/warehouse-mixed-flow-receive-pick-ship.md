---
title: 'Recepción, almacenamiento, selección y envío en la configuración del almacenamiento mixta'
description: 'En Business Central, los procesos de entrada y salida se pueden realizar de maneras diferentes, en función del nivel de complejidad del almacén.'
author: andreipanko
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: null
ms.date: 04/01/2021
ms.author: andreipa
---

# <a name="walkthrough-of-inbound-and-outbound-flow-in-mixed-warehouse-configurations"></a>Tutorial de flujo entrante y saliente en las configuraciones de almacén mixto

Este tutorial demuestra cómo completar los flujos de entrada y salida en una configuración mixta, donde el almacén de flujo de entrada se configura como Básico: pedido por pedido y para el flujo de salida se usa la configuración avanzada. Para obtener más información, consulte [Resumen de las diferentes opciones de configuración](../../design-details-warehouse-management.md#overview-of-different-configuration-options).

## <a name="prerequisites"></a>Requisitos previos
Para completar este tutorial, deberá convertirse en empleado de almacén en el almacén *AMARILLO*, siguiendo estos pasos:  
1. Elija el icono ![Bombilla que abre la característica Dígame 1.](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Empleados de almacén** y luego elija el enlace relacionado.  
2. Elija el campo **Id. de usuario** y seleccione su propia cuenta de usuario en la página **Usuarios**.  
3. En el campo **Código de almacén**, especifique *AMARILLO*.  

## <a name="inbound-flow-receiving-and-putting-away-in-basic-warehouse-configurations"></a>Flujo entrante: recepción y almacenamiento en la configuración del almacenamiento básico

En [!INCLUDE[prod_short](../../includes/prod_short.md)], los procesos de entrada para la recepción y la ubicación se pueden realizar de cuatro maneras utilizando distintas funciones según el nivel de complejidad del almacén.  

|Método|Proceso de salida|Ubicaciones|Recepciones|Ubicaciones|Nivel de complejidad (consulte [Detalles de diseño: Configuración de almacén](../../design-details-warehouse-setup.md))|  
|------------|---------------------|----------|--------------|----------------|--------------------------------------------------------------------------------------------------------------------|  
|A|Registro de la recepción y ubicación desde la línea de pedido|X|||2|  
|P|Registro de la recepción y ubicación desde un documento de ubicación del inventario|||X|3|  
|C|Registro de la recepción y ubicación desde un documento de recepción de almacén||X||5/4/6|  
|D|Registro de la recepción desde un documento de recepción de almacén y registro de ubicación desde un documento de ubicación de almacén||X|X|5/4/6|  

Para obtener más información, consulte [Detalles de diseño: Flujo de entrada del almacén](../../design-details-inbound-warehouse-flow.md).  

En el siguiente tutorial se muestra el método C de la tabla anterior.  

### <a name="scenario"></a>Escenario
Alicia, la agente de compras, crea pedidos de compra para diversos granos tostados, según surge la demanda. Cuando la entrega combinada llega al almacén, John, el trabajador del almacén, recibe y coloca los productos. Cuando John contabiliza la recepción, los productos se contabilizan como recibidos en el inventario y estarán disponibles para la venta u otra demanda.  

### <a name="steps"></a>Pasos
1. Configure la página **Tarjeta de almacén** para definir los flujos entrantes de almacén de la empresa.  

    1.  Elija el icono ![Bombilla que abre la característica Dígame 2.](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Ubicaciones** y luego elija el enlace relacionado.  
    2.  Abra la ficha de almacén *AMARILLO*.  
    3.  Desactive el conmutador **Ubicación requerida**.  

2. Liberar los pedidos de compra al almacén.  

    1. Elija el icono ![Bombilla que abre la característica Dígame 3.](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Pedidos de compra** y, a continuación, elija el vínculo relacionado.  
    2. Seleccione los pedidos del proveedor 10000 para la ubicación AMARILLA. Los números de pedidos de proveedores son *Y-1* e *Y-2*. Utilice las herramientas de personalización si el campo **N.º de pedido de proveedor** no es visible. Para obtener más información, consulte [Personalizar el área de trabajo](../../ui-personalization-user.md).
    3. Elija la acción **Liberar** para notificar al almacén de que los pedidos de compra seleccionados están preparados para la manipulación en almacén cuando llegue la entrega.  

3. Crear la recepción de almacenamiento para recibir y almacenar los productos entregados
    1. Elija el icono ![Bombilla que abre la característica Dígame 4.](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Recepciones de almacén** y luego elija el vínculo relacionado.
    2. Seleccione la acción **Nuevo**
    3. En la página de recepción de almacén, presione Entrar para que se seleccione automáticamente un número de recibo de almacén
    4. Introduzca el **Código de almacén** como *AMARILLO*.
    5. Seleccione la acción **Traer documentos de origen...**
    6. Seleccione los pedidos de compra emitidos anteriormente del proveedor 10000 y elija el botón **Aceptar**.
        Las líneas contendrán una nueva entrada para cada línea de pedido de compra.

4. Ajuste la cantidad a la recepción según la cantidad recibida y el documento de contabilidad
    1. Seleccione la línea con el producto *WRB-1000*.
    2. Seleccione *OVERRCPT10* en el campo **Código de exceso de recepción** y cambie el valor del campo **Cantidad a recibir** desde *100* a *110*.
    3. Seleccione la línea con el producto *WRB-1001* y 
    4. en la segunda línea, cambie el valor del campo **Cantidad a recibir** de *200* a *190*.
    5. Elija la acción **Contabilizar recepción**.

### <a name="results"></a>Resultados
 - los granos tostados ahora se registran como almacenados
 - se crea **Recepción de almacén contabilizada**
 - se crea **Recepción de compra contabilizada**
 - el pedido de compra tiene la **Cantidad recibida** actualizada para las líneas recibidas
 - el producto **Inventario** aumenta en la cantidad elegida
    

## <a name="outbound-flow-picking-and-shipping-in-advanced-warehouse-configurations"></a>Flujo saliente: selección y envío en las configuraciones del almacenamiento básico

En [!INCLUDE[prod_short](../../includes/prod_short.md)], los procesos de salida para el picking y el envío se pueden realizar de cuatro maneras utilizando distintas funciones según el nivel de complejidad del almacén.  

|Método|Proceso de salida|Ubicaciones|Picking|Envíos|Nivel de complejidad (consulte [Detalles de diseño: configuración de almacén](../../design-details-warehouse-setup.md))|  
|------------|---------------------|----------|-----------|---------------|--------------------------------------------------------------------------------------------------------------------|  
|A|Registro de picking y envío desde la línea de pedido|X|||2|  
|P|Registro de picking y envío desde un documento de picking de existencias||X||3|  
|C|Registro de picking y envío desde un documento de envío de almacén|||X|5/4/6|  
|D|Registro de picking desde un documento de picking de almacén y registro de envío de un documento de envío de almacén||X|X|5/4/6|  

Para obtener más información, consulte [Detalles de diseño: Flujo de salida del almacén](../../design-details-outbound-warehouse-flow.md).  

En el siguiente tutorial se demuestra el método D de la tabla anterior.

### <a name="scenario-1"></a>Escenario
Susan, la procesadora de pedidos, crea pedidos de venta de diversos granos tostados y lo pasa al almacén. Como todos los pedidos provienen del mismo cliente, Ellen, la gerente del almacén, decide enviarlos juntos. Juan, el trabajador de almacén debe comprobar que el envío se prepara y envía al cliente.

### <a name="steps-1"></a>Pasos
Esto es una continuación de [Flujo entrante: recepción y almacenamiento en la configuración del almacenamiento básico](#inbound-flow-receiving-and-putting-away-in-basic-warehouse-configurations).

1. Libera los pedidos de venta al almacén.  

    1. Elija el icono ![Bombilla que abre la característica Dígame 5.](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Pedidos de venta** y, a continuación, elija el vínculo relacionado.  
    2. Seleccione los pedidos del cliente 10000 para la ubicación AMARILLA. Los números de pedidos externos son *Y-3*, *Y-4* e *Y- 5*. Utilice las herramientas de personalización si el campo **N.º de pedido externo** no es visible. Para obtener más información, consulte [Personalizar el área de trabajo](../../ui-personalization-user.md).
    3. Elija la acción **Liberar** para notificar al almacén que los pedidos de venta seleccionados están preparados para la manipulación en el almacén.  

2. Para enviar productos  
    1. Elija el icono ![Bombilla que abre la característica Dígame 6.](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Envíos de almacén** y luego elija el enlace relacionado.  
    2. Seleccione la acción **Nuevo**.  
    3. En el campo **Código de almacén**, especifique *AMARILLO*.  
    4. Elija la acción **Utiliz. filt. para traer docs.**.  
    5. En el campo **Código**, especifique **CUST10000**.  
    6. En el campo **Descripción** escriba **Cliente 10000**.  
    7. Seleccione la acción **Modificar**.  
    8. En la ficha desplegable **Ventas**, en el campo **Filtro de venta a n.º de cliente**, especifique *10000*.  
    9. Seleccione la acción **Ejecutar**. 
    
    El envío de almacén se rellena con cuatro líneas que representan líneas de pedido de venta para el cliente especificado. El campo **Cantidad a enviar** está vacío, ya que primero se deben seleccionar los productos.

3. Crear la selección de almacén a partir del envío de almacén
    1. En la página del envío de almacén, elija la acción **Crear selección**.
    2. Confirme cualquiera de las configuraciones de selección necesarias, por ejemplo, seleccione *producto* en el campo **Método de clasificación de líneas de actividad** para agrupar los mismos elementos juntos. Elija el botón **Aceptar**.
    3. Recibirá un mensaje de confirmación con el número de selección. 

4. Abrir la selección de almacén
    1. Con el icono ![Bombilla que abre la característica Dígame 7.](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Selecciones de almacén** y elija el vínculo relacionado.
    2. Localice la selección que creó y ábrala.
    3. Actualice la **Cantidad a manejar**, si es necesario.
    4. Elija la acción **Registrar picking**.
    5. La selección de almacén se cerrará y se eliminará si se manejan todas las cantidades.

5. Contabilizar el envío del almacén
   1. Elija el icono ![Bombilla que abre la característica Dígame 8.](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Envíos de almacén** y luego elija el enlace relacionado.  
   2. Localice el envío que creó antes y ábralo.
    Observe que **Cantidad a enviar** está relleno.
    3. Puede actualizar **Fecha de publicación**, **Número de documento externo**, **Código de agente de envío** y **Método de envío**, si es necesario. Los valores que no estén vacíos se propagarán a los documentos de origen.
    4. Elija la acción **Contabilizar envío**.
    5. Confirme la opción **Enviar**.

### <a name="results-1"></a>Resultados
 - los granos tostados ahora se registran como seleccionados 
 - se crea la **Selección de almacén registrada**
 - se crea **Envío de almacén contabilizado**
 - se crean los tres **Históricos de albaranes de venta**
 - el pedido de venta tiene la **Cantidad enviada** actualizada para las líneas enviadas
 - el producto **Inventario** disminuye en la cantidad elegida


## <a name="see-also"></a>Consulte también
[Recibir productos](../../warehouse-how-receive-items.md)
[Configurar almacenes básicos con zonas de operaciones](../../warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md)
[Detalles de diseño: flujo entrante de almacén](../../design-details-inbound-warehouse-flow.md)
[Enviar productos](../../warehouse-how-ship-items.md)
[Seleccionar productos para almacenamiento de inventario](../../warehouse-how-to-pick-items-for-warehouse-shipment.md)
[Detalles de diseño: flujo saliente de almacén](../../design-details-outbound-warehouse-flow.md)
[Ver la disponibilidad de los productos](../../inventory-how-availability-overview.md)
