---
title: Picking y envío en la configuración del almacenamiento básico
description: En este artículo se describen varios niveles de complejidad en los procesos de picking y envío.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.date: 02/27/2023
ms.custom: bap-template
ms.search.form: '7335, 7337, 7339, 7340, 7341, 7362, 9008'
---
# <a name="walkthrough-picking-and-shipping-in-basic-warehouse-configurations"></a><a name="walkthrough-picking-and-shipping-in-basic-warehouse-configurations"></a><a name="walkthrough-picking-and-shipping-in-basic-warehouse-configurations"></a>Tutorial: picking y envío en la configuración del almacenamiento básico

En [!INCLUDE[prod_short](includes/prod_short.md)], la selección y el envío de productos se realizan mediante uno de los cuatro métodos, como se describe en la siguiente tabla.

|Método|Proceso de salida|Picking requerido|Envío requerido|Nivel de complejidad (Obtenga más información en [Descripción general de la gestión de almacenes](design-details-warehouse-management.md))|  
|------|----------------|-----|---------|-------------------------------------------------------------------------------------|  
|A|Registro de picking y envío desde la línea de pedido|||No hay ninguna actividad de almacén dedicada.|  
|B|Registro de picking y envío desde un documento de picking de existencias|Activado||Básico: Pedido por pedido|  
|P|Registro de picking y envío desde un documento de envío de almacén||Activado|Básico: Publicación consolidada de recepción/envío para múltiples pedidos.|  
|D|Registro de picking desde un documento de picking de almacén y registro de envío de un documento de envío de almacén|Activado|Activado|Avanzado|  

Obtenga más información en [Flujo de salida del almacén](design-details-outbound-warehouse-flow.md).

En el siguiente tutorial se demuestra el método B de la tabla anterior.  

## <a name="about-this-walkthrough"></a><a name="about-this-walkthrough"></a><a name="about-this-walkthrough"></a>Acerca de este tutorial

En la configuración del almacenamiento básico, donde el almacén está configurado para requerir proceso de picking, pero no de envío, utiliza la página **Picking inventario** para registrar la información de picking y envío de los documentos de origen salientes. El documento de origen de salida puede ser un pedido de venta, un pedido de devolución de compra, un pedido de transferencia de salida o una orden de producción con necesidad de componentes.  

En este tutorial, se demuestran las siguientes tareas:  

- Configuración del almacén SUR para el picking de inventario.  
- Crear un pedido de venta para el cliente 10000 para 30 lámparas Ámsterdam.  
- Liberar el pedido de venta para la manipulación en almacén.  
- Crear un picking de existencias basado en un documento de origen lanzado.  
- Registrar el movimiento de almacén desde el almacén y, al mismo tiempo, registrar el albarán de venta para el pedido de venta de origen.  

## <a name="roles"></a><a name="roles"></a><a name="roles"></a>Funciones

En este tutorial, se demuestran las tareas realizadas por los siguientes roles de usuario:  

- Responsable de almacén  
- Procesador de pedidos  
- Trabajador de almacén  

<!-- ## Prerequisites

To complete this walkthrough, you will need:  

- For [!INCLUDE[prod_short](includes/prod_short.md)] online, a company based on the **Advanced Evaluation - Complete Sample Data** option in a sandbox environment. For [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, CRONUS installed.
 -->

## <a name="story"></a><a name="story"></a><a name="story"></a>Historia

Ellen, la administradora del almacén en CRONUS, configura el almacén SUR para la manipulación de picking básica donde los trabajadores de almacén procesan los pedidos de salida individualmente. Susana, la encargada de procesamiento de pedidos, crea un pedido de venta de 30 unidades del producto 1928-S que se deben enviar al cliente 10000 desde el almacén SUR. Juan, el trabajador de almacén debe comprobar que el envío se prepara y envía al cliente. Juan controla todas las tareas relacionadas con la página **Picking inventario**, que señala automáticamente a las ubicaciones donde se almacena 1928-S.

[!INCLUDE[set_up_location.md](includes/set_up_location.md)]

### <a name="setting-up-the-bin-codes"></a><a name="setting-up-the-bin-codes"></a><a name="setting-up-the-bin-codes"></a>Configuración los códigos de ubicación

Una vez que haya configurado el almacén, debe agregar dos ubicaciones.

#### <a name="to-setup-the-bin-codes"></a><a name="to-setup-the-bin-codes"></a><a name="to-setup-the-bin-codes"></a>Para configurar los códigos de ubicación

1. Seleccione la acción **Ubicaciones**.
2. Crea dos ubicaciones, con los códigos *S-01-0001* y *S-01-0002*.

### <a name="making-yourself-a-warehouse-employee-at-location-south"></a><a name="making-yourself-a-warehouse-employee-at-location-south"></a><a name="making-yourself-a-warehouse-employee-at-location-south"></a>Convertirse en un empleado de almacén en el almacén SUR

Para utilizar esta funcionalidad, debe agregarse al almacén como trabajador del almacén. 

#### <a name="to-make-yourself-a-warehouse-employee"></a><a name="to-make-yourself-a-warehouse-employee"></a><a name="to-make-yourself-a-warehouse-employee"></a>Para convertirte en un empleado de almacén

  1. Elija el icono ![Bombilla que abre la función Dígame primero.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Empleados de almacén** y luego elija el enlace relacionado.  
  2. Elija el campo **Id. de usuario** y seleccione su propia cuenta de usuario en la página **Empleados de almacén**.
  3. En el campo **Cód. almacén**, elija SUR.  
  4. Seleccione el campo **Predeterminado** y, a continuación, seleccione el botón **Sí**.  

### <a name="making-item-1928-s-available"></a><a name="making-item-1928-s-available"></a><a name="making-item-1928-s-available"></a>Hacer que el producto 1928-S esté disponible

Para que el producto 1928-S esté disponible en el almacén SUR siga estos pasos:  

  1. Elija el icono ![Bombilla que abre la función Dígame segundo.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Diarios de productos**, y luego elija el enlace relacionado.  
  2. Abra el diario predeterminado y después cree dos líneas del diario del producto con la siguiente información en la fecha de trabajo (23 de enero).  

        |Tipo mov.|Número de producto|Código de ubicación|Cód. ubicación|Cantidad|  
        |----------------|-----------------|-------------------|--------------|--------------|  
        |Entradas|1928-S|SUR|S-01-0001|nº 20|  
        |Entradas|1928-S|SUR|S-01-0002|nº 20|  

        De forma predeterminada, el campo **Código de ubicación** de las líneas de ventas están ocultos, por lo que deberá mostrarlos. Para hacer esto, necesita personalizar la página. Para más información, vea [Para comenzar a personalizar una página a través del banner de personalización](ui-personalization-user.md#to-start-personalizing-a-page-through-the-personalizing-banner).

  3. Elija **Acciones**, **Registro** y, a continuación, elija **Registrar**.  
  4. Seleccione el botón **Sí**.  

## <a name="creating-the-sales-order"></a><a name="creating-the-sales-order"></a><a name="creating-the-sales-order"></a>Crear el pedido de venta

Los pedidos de venta son el tipo más común de documento de origen de salida.  

### <a name="to-create-the-sales-order"></a><a name="to-create-the-sales-order"></a><a name="to-create-the-sales-order"></a>Para crear el pedido de venta

1. Elija el icono ![Bombilla que abre la función Dígame tercero.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Pedidos de venta** y, a continuación, elija el vínculo relacionado.  
2. Seleccione la acción **Nuevo**.  
3. Crea un pedido de venta para el cliente 10000 en la fecha de trabajo (23 de enero) con la línea de pedido de venta siguiente.  

    |Producto|Código de ubicación|Cantidad|  
    |----|-------------|--------|  
    |1928-S|SUR|30|  

     Empiece a notificar el almacén para el que el pedido de venta está preparado para la manipulación en almacén.  

4. Seleccione la acción **Liberar**.  

    Juan comienza a realizar el picking y a enviar a productos vendidos.  

## <a name="picking-and-shipping-items"></a><a name="picking-and-shipping-items"></a><a name="picking-and-shipping-items"></a>Picking y envío de productos

En la página **Picking inventario**, puede administrar todas las actividades de almacén de salida para un documento de origen determinado, como un pedido de venta. [!INCLUDE[tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  

### <a name="to-pick-and-ship-items"></a><a name="to-pick-and-ship-items"></a><a name="to-pick-and-ship-items"></a>Realizar el picking y el envío de productos

1. Elija el icono ![Bombilla que abre la función Dígame cuarto.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Picking inventario** y luego elija el enlace relacionado.  
2. Seleccione la acción **Nuevo**.  

    Asegúrese de que el campo **N.º** en desplegable **General** se haya rellenado.
3. Seleccione el campo **Documento origen** y luego **Pedido venta**.  
4. Seleccione el campo **Nº origen**, la línea para la venta al cliente 10000 y, a continuación, el botón **Aceptar**.  

    De forma alternativa, seleccione la acción **Obtener documento de origen** y, a continuación, seleccione el pedido de ventas.  
5. Seleccione la acción **Autorrellenar el campo Cdad. para manipular**.  

    También, en el campo **Cdad. a manipular**, introduzca 10 y 20 respectivamente en las dos líneas del picking de existencias.  
6. Seleccione la acción **Registrar**, seleccione **Enviar** y, a continuación, el botón **Aceptar**.  

    Los 30 lámparas Ámsterdam ahora se registran como preparados desde las ubicaciones S-01-0001 y S-01-0002, y un movimiento de producto negativo se crea para reflejar el histórico de albaranes de venta.  

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Consultar la [formación de Microsoft](/training/paths/pick-ship-items-business-central/) relacionada

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Consulte también .

[Realizar el picking de productos con picking inventario](warehouse-how-to-pick-items-with-inventory-picks.md)  
[Realizar un picking de los artículos para el envío de almacén](warehouse-how-to-pick-items-for-warehouse-shipment.md)  
[Configurar almacenes básicos con áreas de operaciones](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md)  
[Picking para producción o ensamblado](warehouse-how-to-pick-for-production.md)  
[Mover productos ad hoc en configuraciones básicas de almacén](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md)  
[Detalles de diseño: Flujo de salida del almacén](design-details-outbound-warehouse-flow.md)  
[Tutoriales de procesos empresariales](walkthrough-business-process-walkthroughs.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
