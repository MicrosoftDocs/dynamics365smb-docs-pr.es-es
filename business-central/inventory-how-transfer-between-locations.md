---
title: Transferir productos entre almacenes
description: Aprenda a mover el inventario de un lugar o almacén a otro con el diario de reclasificación o con pedidos de transferencia.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: how-to
ms.date: 02/21/2023
ms.custom: bap-template
ms.search.keywords: 'move, warehouse'
ms.search.forms: '5746, 5745, 5759, 5753, 5743, 5758, 5752, 5744, 5749, 5740, 5741, 5742, 5757, 5748, 5747, 9285, 5756, 5755'
---
# <a name="transfer-inventory-between-locations"></a>Transferir el inventario entre almacenes

Puede transferir inventarios de productos entre almacenes creando pedidos de transferencia. También puede usar el diario de reclasificación de productos.

> [!NOTE]
> Para transferir productos, debe configurar los almacenes y las rutas de transferencia. Para obtener más información sobre cómo configurar almacenes, vaya a [Configurar almacenes](inventory-how-setup-locations.md). No puede usar pedidos de transferencia para almacenes *en blanco*.

## <a name="transfer-orders"></a>Pedidos de transferencia

Puede enviar una transferencia de salida desde un almacén y recibir una transferencia de entrada en el destino. Con él, puede:

* Seguimiento de una cantidad en tránsito
* Defina calendarios, rutas y tiempos de manejo de entrada y salida para el cálculo y la planificación de fechas. Para obtener más información sobre la planificación, vaya a [Sobre la funcionalidad de la planificación](production-about-planning-functionality.md).
* Use diferentes funciones de almacén para los almacenes de entrada y salida.
* Con algunas limitaciones, puede usar pedidos de transferencia para transferencias directas.

## <a name="item-reclassification-journals"></a>Diarios de reclasificación de productos

* Transferencia sencilla y directa de productos entre almacenes.
* Mueva productos entre ubicaciones. Para obtener más información sobre la transferencia de productos entre ubicaciones, vaya a [Mover productos no planificados en configuraciones básicas de almacén](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md).
* Cambie un número de serie o lote por un nuevo número de serie o lote. Para obtener más información sobre cómo reclasificar los números de serie o lote, vaya a [Reclasificar números de serie o lote](inventory-how-work-item-tracking.md#to-reclassify-serial-or-lot-numbers).
* Cambie la fecha de caducidad a una nueva fecha.
* Reclasifique productos desde un almacén *en blanco* hasta un almacén real.
* Las actividades de almacén no se administran. Se crearán movimientos de almacén.

## <a name="to-transfer-items-with-a-transfer-order"></a>Para transferir productos con un pedido de transferencia

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Pedidos de transferencia** y luego elija el enlace relacionado.
2. En la página **Pedido de transferencia**, rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    >   Si ha rellenado los campos **Cód. en tránsito**, **Cód. transportista** y **Cód. servicio transportista** en la página **Ruta transf. espec.** al configurar la ruta de transferencia, los campos correspondientes del pedido de transferencia se rellenan automáticamente.

    Cuando se especifica un valor en el campo **Servicio transportista**, se calcula la fecha de recepción en el almacén de destino de la transferencia, sumando el tiempo de envío del transportista a la fecha de envío.

3. Hay varias formas de rellenar las líneas:

    |Opción  |Descripción  |
    |---------|---------|
    |Manualmente     | En la ficha desplegable **Líneas**, rellene una línea para un producto o use la acción **Seleccionar articulos** para elegir varios productos.        |
    |Automáticamente     | * Elija la acción **Traer contenido de ubicación** para seleccionar productos existentes de una ubicación específica del almacén.<br><br>* Elija la acción **Obtener líneas de albarán** para seleccionar productos que acaban de llegar al almacén de transferencia.        |

    Ahora puede enviar los productos.
4. Seleccione la acción **Registrar**, seleccione la opción **Envío** y seleccione el botón **Aceptar**.

    Los productos ahora se encuentran en tránsito entre las ubicaciones especificadas, según la ruta de transferencia especificada.

    Como trabajador de almacén en el almacén de procedencia de la transferencia, continúe con la recepción de los productos. Las líneas del pedido de transferencia son las mismas que en el envío y no se pueden editar.
5. Seleccione la acción **Registrar**, seleccione la opción **Recepción** y seleccione el botón **Aceptar**.

### <a name="post-multiple-transfer-orders-in-a-batch"></a>Contabilizar varios pedidos de transferencia en un lote

El siguiente procedimiento explica cómo contabilizar pedidos de transferencia en un lote.

1. 1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Pedidos de transferencia** y luego elija el enlace relacionado.  
2. En la página **Pedidos de transferencia**, seleccione los pedidos a contabilizar.
3. En el campo **N.º**, campo, abra el menú contextual y elija **Seleccionar más**.
4. Seleccione la casilla de las líneas de cada pedido que desee contabilizar.
5. Elija la acción **Contabilizar** y, a continuación, seleccione **Lote de contabilidad**.
6. En la página **Pedido de transferencia de lote de contabilidad**, rellene los campos según sea necesario.

   > [!TIP]
    > Para pedidos de transferencia que utilizan una ubicación en tránsito, puede elegir entre **Enviar** o **Recibir**. Repita este paso si necesita hacer ambas cosas. Para pedidos donde **Contabilidad directa** está activado, ambas opciones funcionan de la misma manera y contabilizan el pedido por completo.

7. Seleccione **Aceptar**.
8. Para ver posibles problemas, abra la página **Registro de mensajes de error**.

    > [!NOTE]
    > La contabilización de varios documentos puede llevar algún tiempo y bloquear a otros usuarios. Considere habilitar la publicación en segundo plano. Para obtener más información, consulte [Uso de colas de proyectos para programar tareas](/dynamics365/business-central/admin-job-queues-schedule-tasks).

### <a name="schedule-a-job-queue-entry-to-post-multiple-documents-in-a-batch"></a>Programar una entrada de la cola de trabajos para contabilizar varios documentos en un lote

Como alternativa, puede usar la cola de trabajos para programar la contabilidad, para que se realice en un momento que sea conveniente para su organización. Por ejemplo, para su empresa puede tener sentido ejecutar ciertas rutinas cuando la mayor parte de la introducción de datos del día ha concluido.

El siguiente procedimiento muestra cómo configurar el informe **Contabilizar pedidos venta en lote** para que se registren automáticamente los pedidos de transferencia a las 4:00 p. m. en días laborables. Ese tiempo es solo un ejemplo. Los pasos son los mismos para otros documentos.  

1. Busque la página **Entradas de la cola de trabajos** y luego elija el vínculo relacionado.  
2. Seleccione la acción **Nuevo**.  
3. En el campo **Tipo objeto para ejecutar**, seleccione **Informe**.  
4. En el campo **Id. de objeto a ejecutar**, seleccione **5707, Contabilidad en lote de pedidos de transferencia**.
5. Seleccione la casilla **Página de solicitud de informe**.
6. En la página de solicitud **Contabilidad en lote de pedidos de transferencia** elija la opción **Enviar**, filtre en **Transferencia directa** y luego seleccione **Aceptar**.

   > [!IMPORTANT]
   > Es importante establecer filtros. De lo contrario, [!INCLUDE [prod_short](includes/prod_short.md)] contabilizará todos los documentos, incluso si no están listos. Considere establecer un filtro en el campo **Estado** para el valor **Publicado** y un filtro en el campo **Fecha de publicación** para el valor **..hoy**. Para obtener más información sobre los filtros, vaya a [Clasificación, búsqueda y filtrado](/dynamics365/business-central/ui-enter-criteria-filters).

7. Seleccione todas las casillas de **Ejecutar los lunes** hasta **Ejecutar los viernes**.
8. En el campo **Hora inicial**, introduzca **4 p. m.**.
9. Elija la acción **Establecer estado en Preparado**.

## <a name="to-transfer-items-with-the-item-reclassification-journal"></a>Para transferir productos con el diario de reclasificación de productos

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Diarios reclasif. producto**, y luego elija el enlace relacionado.
2. En la página **Diarios reclasif. producto**, rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. En el campo **Cód. almacén**, escriba la el almacén donde se almacenan los productos actualmente.

    > [!NOTE]  
    > Para transferir productos que no tienen código de almacén, deje en blanco el campo **Cód. almacén**.
4. En el campo **Cód. almacén destino**, especifique el almacén al que desee transferir los productos.
5. Seleccione la acción **Registrar**.

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]

## <a name="undo-a-transfer-shipment"></a>Deahacer un envío de transferencia

Si encuentra un error en una cantidad en una orden de transferencia contabilizada, siempre que no se reciba el envío, puede corregir fácilmente la cantidad. En la página **Envío de transferencia contabilizado**, la acción **Deshacer envío** crea líneas correctivas, de la siguiente manera:

* El valor del campo **Cantidad enviada** disminuye en la cantidad que ha deshecho.
* El valor del campo **Cantidad a enviar** se incrementa en la cantidad que ha deshecho.
* Se activa la casilla **Corrección** para las líneas.

Si la cantidad se ha enviado en un envío de almacén, se crea una línea de corrección en el envío de almacén contabilizado.

Para completar la corrección, vuelva a abrir la orden de transferencia, introduzca la cantidad correcta y luego contabilice el pedido. Si utiliza un envío de almacén para enviar el pedido, cree y contabilice un nuevo envío de almacén.

## <a name="see-related-microsoft-training"></a>Consultar la [formación de Microsoft](/training/modules/transfer-items/) relacionada

## <a name="see-also"></a>Consulte también .

[Gestionar inventario](inventory-manage-inventory.md)  
[Configurar ubicaciones](inventory-how-setup-locations.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Cambiar las funciones que se muestran](ui-experiences.md)  
[Funciones empresariales generales](ui-across-business-areas.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
