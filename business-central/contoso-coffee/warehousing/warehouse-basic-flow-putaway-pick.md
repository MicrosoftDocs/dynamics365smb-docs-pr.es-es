---
title: 'Recepción, almacenamiento, selección y envío en la configuración del almacenamiento básico'
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

# <a name="walkthrough-of-inbound-and-outbound-flow-in-basic-warehouse-configurations"></a><a name="walkthrough-of-inbound-and-outbound-flow-in-basic-warehouse-configurations"></a><a name="walkthrough-of-inbound-and-outbound-flow-in-basic-warehouse-configurations"></a><a name="walkthrough-of-inbound-and-outbound-flow-in-basic-warehouse-configurations"></a>Tutorial de flujo entrante y saliente en las configuraciones de almacén básico

Este tutorial muestra cómo completar los flujos entrantes y salientes en la configuración básica: pedido por pedido. Para obtener más información, consulte [Resumen de las diferentes opciones de configuración](../../design-details-warehouse-management.md#overview-of-different-configuration-options).

## <a name="prerequisites"></a><a name="prerequisites"></a><a name="prerequisites"></a><a name="prerequisites"></a>Requisitos previos
Para completar este tutorial, deberá convertirse en empleado de almacén en el almacén *PLATA*, siguiendo estos pasos:  
1. Elija el icono ![Bombilla que abre la característica Dígame 1.](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Empleados de almacén** y luego elija el enlace relacionado.  
2. Elija el campo **Id. de usuario** y seleccione su propia cuenta de usuario en la página **Usuarios**.  
3. En el campo **Código de almacén**, especifique *PLATA*.  

## <a name="inbound-flow-receiving-and-putting-away-in-basic-warehouse-configurations"></a><a name="inbound-flow-receiving-and-putting-away-in-basic-warehouse-configurations"></a><a name="inbound-flow-receiving-and-putting-away-in-basic-warehouse-configurations"></a><a name="inbound-flow-receiving-and-putting-away-in-basic-warehouse-configurations"></a>Flujo entrante: recepción y almacenamiento en la configuración del almacenamiento básico

En [!INCLUDE[prod_short](../../includes/prod_short.md)], los procesos de entrada para la recepción y la ubicación se pueden realizar de cuatro maneras utilizando distintas funciones según el nivel de complejidad del almacén.  

|Método|Proceso de salida|Ubicaciones|Recepciones|Ubicaciones|Nivel de complejidad (consulte [Detalles de diseño: Configuración de almacén](../../design-details-warehouse-setup.md))|  
|------------|---------------------|----------|--------------|----------------|--------------------------------------------------------------------------------------------------------------------|  
|A|Registro de la recepción y ubicación desde la línea de pedido|X|||2|  
|P|Registro de la recepción y ubicación desde un documento de ubicación del inventario|||X|3|  
|C|Registro de la recepción y ubicación desde un documento de recepción de almacén||X||5/4/6|  
|D|Registro de la recepción desde un documento de recepción de almacén y registro de ubicación desde un documento de ubicación de almacén||X|X|5/4/6|  

Para obtener más información, consulte [Detalles de diseño: Flujo de entrada del almacén](../../design-details-inbound-warehouse-flow.md).  

En el siguiente tutorial se demuestra el método B de la tabla anterior.  

### <a name="scenario"></a><a name="scenario"></a><a name="scenario"></a><a name="scenario"></a>Escenario
Alicia, la agente de compras, crea una orden de compra para diversos granos tostados. Cuando la entrega llega al almacén, John, el trabajador del almacén, coloca los productos en las ubicaciones adecuadas. Cuando John contabiliza el almacenamiento, los productos se contabilizan como como recibidos en el inventario y disponibles para la venta u otra demanda.  

### <a name="steps"></a><a name="steps"></a><a name="steps"></a><a name="steps"></a>Pasos
1. Configure la página **Tarjeta de almacén** para definir los flujos entrantes de almacén de la empresa.  

    1.  Elija el icono ![Bombilla que abre la característica Dígame 2.](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Ubicaciones** y luego elija el enlace relacionado.  
    2.  Abra la ficha de almacén *PLATA*.  
    3.  Active la casilla **Ubicación requerida**.  

2. Defina una ubicación predeterminada para el producto, para controlar dónde se ubica

    1.  Elija la acción **Ubicaciones** en la **Tarjeta de ubicación**
    2.  Seleccione la primera fila, para la ubicación *S-1-01*, y después seleccione **Contenidos**.  
    3.  Seleccione la acción **Nuevo**.  
    4.  Seleccione los campos **Fijo** y **Predet.**.  
    5.  En el campo **N.º producto**, introduzca *WRB-1000*.  

3. Cree el pedido de compra, que es el tipo más común de documento de origen de entrada.  

    1.  Elija el icono ![Bombilla que abre la característica Dígame 3.](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Pedidos de compra** y, a continuación, elija el vínculo relacionado.  
    2.  Seleccione la acción **Nuevo**.  
    3.  Cree un pedido de compra para el proveedor 10000 con las líneas de pedido de compra siguientes. Utilice las herramientas de personalización si el campo **Código de ubicación** no está visible. Para obtener más información, consulte [Personalizar el área de trabajo](../../ui-personalization-user.md). 

    |Producto|Cód. almacén|Cód. ubicación|Cantidad|  
    |----------|----------|---------|--------------|  
    |WRB-1000|PLATA|S-1-01|nº 20|  
    |WRB-1001|PLATA||30|

    El código de ubicación del primero se rellena conforme a la configuración. El código de ubicación del segundo producto está vacío, porque no tiene valores predeterminados. Manténgalo de esta manera.  

    4.  Elija la acción **Liberar** para notificar al almacén para el que el pedido de compra está preparado para la manipulación en almacén cuando llegue la entrega.  

4. Crear **Ubicación de almacenamiento** para recibir y ubicar los productos entregados  

    1. Elija el icono ![Bombilla que abre la característica Dígame 4.](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Ubicación de inventario** y luego elija el enlace relacionado.  
    2. Seleccione la acción **Nuevo**. 
    3. En el campo **Código de almacén**, especifique *PLATA*.
    4. Seleccione el campo **Documento origen** y luego **Pedido compra**.  
    5. Seleccione el campo **Número de origen** , seleccione la línea para la compra del proveedor 10000 y luego elija el botón **Aceptar** para rellenar las líneas de almacenamiento según el documento de origen seleccionado.

        De forma alternativa, seleccione la acción **Obtener documento de origen** y, a continuación, seleccione el pedido de compra.  

5. Modifique el almacenamiento del inventario en función de la ubicación real de los productos y el documento de publicación

    Al colocar elementos en ubicaciones, John notó que la ubicación predeterminada ya contiene algunos elementos, por lo que decidió usar otra ubicación. John también coloca otros productos en las ubicaciones siguientes, ya que la cantidad recibida no se ajusta a la capacidad.

    1. En la primera línea, cambie **Código de ubicación** desde *S-1-01*, que se copió de la orden de compra, a *S-1-02*. 
    2.  Introduzca 20 en el campo **Cantidad a manipular** de la línea de almacenamiento de inventario del producto WBR-1000.  
    3. En la segunda línea, introduzca 20 en el campo **Cantidad a manejar** y elija la acción **Dividir línea**. Aparecerá una nueva línea, que es una copia de la línea original, excepto en que el campo **Cdad. a manipular** contiene la cantidad que ha eliminado de la línea original. 
    4. Complete los códigos de ubicaciones para el producto WBR-1001:

    |Producto|Cód. ubicación|Cantidad|  
    |----------|-------------------|--------------|  
    |WRB-1001|S-1-03|nº 20|  
    |WRB-1001|S-1-04|10|

    5.  Seleccione la acción **Registrar**, elija la acción **Recibir** y seleccione el botón **Aceptar**.  

### <a name="results"></a><a name="results"></a><a name="results"></a><a name="results"></a>Resultados
 - los granos tostados ahora se registran como almacenados en ubicaciones especificadas
 - se crea **Ubicado el inventario contabilizado**
 - se crea **Recepción de compra contabilizada**
 - el pedido de compra tiene la **Cantidad recibida** actualizada para las líneas recibidas
 - el producto **Inventario** aumenta en la cantidad elegida
    

## <a name="outbound-flow-picking-and-shipping-in-basic-warehouse-configurations"></a><a name="outbound-flow-picking-and-shipping-in-basic-warehouse-configurations"></a><a name="outbound-flow-picking-and-shipping-in-basic-warehouse-configurations"></a><a name="outbound-flow-picking-and-shipping-in-basic-warehouse-configurations"></a>Flujo saliente: selección y envío en la configuración del almacenamiento básico

En [!INCLUDE[prod_short](../../includes/prod_short.md)], los procesos de salida para el picking y el envío se pueden realizar de cuatro maneras utilizando distintas funciones según el nivel de complejidad del almacén.  

|Método|Proceso de salida|Ubicaciones|Picking|Envíos|Nivel de complejidad (consulte [Detalles de diseño: configuración de almacén](../../design-details-warehouse-setup.md))|  
|------------|---------------------|----------|-----------|---------------|--------------------------------------------------------------------------------------------------------------------|  
|A|Registro de picking y envío desde la línea de pedido|X|||2|  
|P|Registro de picking y envío desde un documento de picking de existencias||X||3|  
|C|Registro de picking y envío desde un documento de envío de almacén|||X|5/4/6|  
|D|Registro de picking desde un documento de picking de almacén y registro de envío de un documento de envío de almacén||X|X|5/4/6|  

Para obtener más información, consulte [Detalles de diseño: Flujo de salida del almacén](../../design-details-outbound-warehouse-flow.md).  

En el siguiente tutorial se demuestra el método B de la tabla anterior.

### <a name="scenario-1"></a><a name="scenario-1"></a><a name="scenario-1"></a><a name="scenario-1"></a>Escenario
Susan, la procesadora de pedidos, crea un pedido de venta de diversos granos tostados y lo pasa al almacén. Juan, el trabajador de almacén debe comprobar que el envío se prepara y envía al cliente. John controla todas las tareas relacionadas con la página **Selección de inventario**, que señala automáticamente las ubicaciones donde se almacenan los granos tostados.

### <a name="steps-1"></a><a name="steps-1"></a><a name="steps-1"></a><a name="steps-1"></a>Pasos
Esto es una continuación de [Flujo entrante: recepción y almacenamiento en la configuración del almacenamiento básico](#inbound-flow-receiving-and-putting-away-in-basic-warehouse-configurations).

1. Configure la página **Tarjeta de almacén** para definir los flujos entrantes de almacén de la empresa.  

    1.  Elija el icono ![Bombilla que abre la característica Dígame 5.](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Ubicaciones** y luego elija el enlace relacionado.  
    2.  Abra la ficha de almacén *PLATA*.  
    3.  Active la casilla **Picking requerido**.  

2. Cree el pedido de venta, que es el tipo más común de documento de origen de salida.  

    1. Elija el icono ![Bombilla que abre la característica Dígame 6.](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Pedidos de venta** y, a continuación, elija el vínculo relacionado.  
    2. Seleccione la acción **Nuevo**.  
    3. Cree un pedido de venta para el cliente 10000 con la siguiente línea de pedido de venta.  

    |Producto|Cód. almacén|Cantidad|  
    |----|-------------|--------|  
    |WRB-1000|PLATA|nº 20|  
    |WRB-1001|PLATA|30|  

    Los códigos de ubicación se completan automáticamente con las ubicaciones predeterminadas.

    4. Elija la acción **Crear ubicación/selección de inventario** .
    5. Active la casilla **Crear pick exist.**.  
    6. Elija el botón **Aceptar**. Se creará un nuevo picking de inventario.

3. Seleccionar y enviar productos

    1. Elija el icono ![Bombilla que abre la característica Dígame 7.](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Picking inventario** y luego elija el enlace relacionado.  
    2. Seleccione la selección de inventario para las ventas al cliente 10000
    
    La selección de inventario creada ignoró la ubicación definida para el producto *WRB-1000*, ya que no contiene inventario y usó otra ubicación. Las segundas líneas, con el producto *WRB-1001*, se dividieron automáticamente para elegir entre varias ubicaciones.
    
4. Seleccione la acción **Autorrellenar el campo Cdad. para manipular**.  

5. Seleccione la acción **Registrar**, seleccione **Enviar** y, a continuación, el botón **Aceptar**.  

### <a name="results-1"></a><a name="results-1"></a><a name="results-1"></a><a name="results-1"></a>Resultados
 - los granos tostados ahora se registran como seleccionados en ubicaciones especificadas
 - se crea **Selección de inventario contabilizado**
 - se crea el **Histórico de albaranes de venta**
 - el pedido de venta tiene la **Cantidad enviada** actualizada para las líneas enviadas
 - el producto **Inventario** disminuye en la cantidad elegida


## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Consulte también
[Almacenar productos con almacenamientos de inventario](../../warehouse-how-to-put-items-away-with-inventory-put-aways.md) 
[Configurar almacenes básicos con zonas de operaciones](../../warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md) 
[Detalles de diseño: flujo entrante de almacén](../../design-details-inbound-warehouse-flow.md) 
[Seleccionar productos con selecciones de inventario](../../warehouse-how-to-pick-items-with-inventory-picks.md) 
[Detalles de diseño: flujo saliente de almacén](../../design-details-outbound-warehouse-flow.md) 
[Ver la disponibilidad de los productos](../../inventory-how-availability-overview.md) 
