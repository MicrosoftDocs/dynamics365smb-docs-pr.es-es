---
title: "Procedimiento: Cálculo de las fechas de compromiso de entrega de pedido | Documentos de Microsoft"
description: "La función de compromiso de entrega de pedidos es una herramienta para el cálculo de la fecha más temprana posible en la que un producto se encuentra disponible para su envío. También crea líneas de demanda para aquellas fechas que se aceptan."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 01/19/2019
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: b31ba087798c3f54e54403ed418019c82ce3091c
ms.contentlocale: es-es
ms.lasthandoff: 01/30/2018

---
# <a name="calculate-order-promising-dates"></a>Calcular fechas de compromiso de entrega de pedido
Una empresa debe poder informar a los clientes de las fechas de entrega del pedido. La ventana **Líneas compromiso entrega pedido** permite realizar esta operación desde una línea de pedido de venta.  

Basándose en las fechas sabidas y planificadas de disponibilidad de un producto, [!INCLUDE[d365fin](includes/d365fin_md.md)] inmediatamente calcula las fechas de envío y de entrega, que se podrán acordar con el cliente.  

Si escribe una fecha de entrega requerida en una línea del pedido de venta, se utilizará dicha fecha como punto inicial para los cálculos siguientes.  

- Fecha entrega requerida - Hora envío = Fecha envío planeada  
- Fecha envío planeada - Tiempo manip. alm. salida = Fecha envío  

Si los productos están disponibles para el picking en la fecha de envío, el proceso de venta puede continuar. Si no lo están, se mostrará la advertencia de falta de stock.  

Si no especifica una fecha de entrega requerida en una línea del pedido de venta, o si la fecha de entrega requerida no se puede cumplir, se calculará la fecha más próxima en la que estarán disponibles los productos. A continuación se insertará dicha fecha en la línea del campo **Fecha envío** y utiliza los cálculos siguientes para calcular la fecha prevista para el envío de los productos y la fecha de su entrega al cliente:  

- Fecha envío + Tiempo manip. alm. salida = Fecha envío planeada  
- Fecha envío planeada + Hora envío = Fecha entrega planeada  

## <a name="about-order-promising"></a>Acerca del compromiso de entrega
La función compromiso de pedido le permite establecer un compromiso para enviar el pedido en una fecha determinada. Se calcula la fecha en la que un producto está disponible para su compromiso, y se crean las líneas del pedido para las fechas que haya aceptado. La función calcula la fecha más temprana posible en la que un producto se encuentra disponible para su envío. También crea líneas de demanda, en caso de que los artículos deban ser primero compras, para la fechas que usted acepta.

[!INCLUDE[d365fin](includes/d365fin_md.md)]  utiliza dos conceptos fundamentales:  

- Neto no comprometido (NNC)  
- Capaz de comprometer (CTP)  

### <a name="available-to-promise"></a>Neto no comprometido  
El neto (ATP) no comprometido calcula fechas basándose en el sistema de reserva. Llevará a cabo una comprobación de la disponibilidad de las cantidades sin reservar del inventario en relación con la producción, las compras, las transferencias y las devoluciones de ventas previstas. De acuerdo con esta información, [!INCLUDE[d365fin](includes/d365fin_md.md)] calcula automáticamente la fecha de entrega del pedido del cliente porque los productos estarán disponibles, ya sea en el inventario o en recepciones planificadas.  

### <a name="capable-to-promise"></a>Capaz de comprometer  
Capaz de comprometer (CTP) supone un escenario de "qué pasa si", que solo se aplica a cantidades de artículos que no están en el inventario o en pedidos programados. En base a esta situación, [!INCLUDE[d365fin](includes/d365fin_md.md)] calcula la fecha más temprana en la que el producto podría estar disponible si se va a producir, comprar o transferir.

#### <a name="example"></a>Ejemplo
Si hay un pedido de 10 piezas y hay 6 piezas disponibles en el inventario o en pedidos programados, el cálculo de capaz de comprometer se basará en 4 piezas.

### <a name="calculations"></a>Cálculos  
Cuando [!INCLUDE[d365fin](includes/d365fin_md.md)] calcula la fecha de la entrega del cliente, realiza dos tareas:  

- Calcula la fecha de entrega más próxima cuando el cliente no ha solicitado una fecha de entrega concreta.  
- Comprueba si la fecha de entrega solicitada por el cliente o acordada con el cliente es realista.  

Si el cliente no solicita una fecha de entrega concreta, la fecha de envío se establece en el mismo valor que la fecha de trabajo y la disponibilidad se basa en esa fecha. Si el producto está en el inventario, [!INCLUDE[d365fin](includes/d365fin_md.md)] calcula hacia adelante en el tiempo para determinar cuándo se puede entregar el pedido. Esto se logra con las siguientes formulas:  

- Fecha envío + Almacén salida + Envío planeado + Tiempo manipulación = Fecha  
- Fecha envío planeada + Hora envío = Fecha entrega planeada  

[!INCLUDE[d365fin](includes/d365fin_md.md)] A continuación,  comprueba si la fecha de entrega calculada es realista calculando hacia atrás en el tiempo para determinar cuándo debe estar disponible el producto para cumplir la fecha acordada. Esto se logra con las siguientes formulas:  

- Fecha entrega planeada - Hora envío = Fecha envío planeada  
- Fecha envío planeada - Manip. almacén salida = Fecha envío  

La fecha de envío se utiliza para realizar la comprobación de disponibilidad. Si el producto está disponible esta fecha, [!INCLUDE[d365fin](includes/d365fin_md.md)] confirma que la entrega solicitada/acordada se puede cumplir estableciendo la fecha de entrega prevista en la misma fecha de entrega solicitada/acordada. Si el producto no está disponible, devolverá una fecha en blanco y el procesador de pedidos podrá utilizar la funcionalidad de CTP.  

Basándose en las nuevas fechas y horas, todas las fechas relacionadas se calculan según las fórmulas enumeradas anteriormente en esta sección. El cálculo de CTP tarda más en realizarse pero proporciona una fecha exacta en la que el cliente puede esperar que el producto se entregue. Las fechas que se calculan de CTP se muestran en los campos **Fecha entrega planificada** y **Primera fecha envío** en la ventana **Líneas compromiso entrega pedido**.  

El procesador de pedidos termina el proceso de CTP validando las fechas. Esto significa que se crean una línea de planificación y un movimiento de reserva para el producto antes de las fechas calculadas para garantizar que el pedido se cumple.  

Además del compromiso de entrega externo que puede realizar en la ventana **Líneas compromiso entrega pedido**, también puede comprometerse con fechas de entrega internas o externas para los productos de la lista de materiales. Para obtener más información, consulte [Consultar la disponibilidad de los productos](inventory-how-availability-overview.md).

## <a name="to-set-up-order-promising"></a>Para configurar compromisos de pedidos  
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Config. compr. entrega ped.** y, a continuación, seleccione el vínculo relacionado.  
2. Introduzca un número y una unidad de tiempo en el campo **Desfase (tiempo)**. Seleccione uno de los siguientes códigos.  

    |Código|Descripción|  
    |----------|-----------------|  
    |**d**|Día del calendario|  
    |**t**|Semana|  
    |**m**|Mes|  
    |**t**|Trimestre|  
    |**a**|Año|  

    Por ejemplo, "3w" indica que el tiempo de desfase son tres semanas. Para indicar el periodo corriente, utilice "c" como prefijo en cualquiera de estos códigos. Por ejemplo, si desea que el tiempo de desfase sea el mes corriente, introduzca **cm**.  
3. Introduzca una serie numérica en el campo **Nº serie compr. entreg. ped.** al seleccionar una línea de la lista en la ventana **Nº serie**.  
4. Introduzca una plantilla de compromiso de entrega de pedido en el campo **Plantilla compr. entrega ped.** al seleccionar una línea de la lista en la ventana **Lista libros hojas demanda**.  
5. Introduzca una hoja de demanda en el campo **Hoja compr. entrega ped.** al seleccionar una línea de la lista en la ventana **Nombres hojas demanda**.

### <a name="to-enter-inbound-warehouse-handling-time-in-the-inventory-setup-window"></a>Para especificar un tiempo de manipulación en almacén de entrada en la ventana de configuración de existencias  
Si desea incluir un tiempo de manipulación en almacén en el cálculo del compromiso de entrega del pedido en la línea de compra, configúrelo como valor predeterminado para las existencias y para el almacén.    
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Configuración de inventario** y, a continuación, seleccione el vínculo relacionado.  
2. En la ficha desplegable **General**, en el campo **Tiempo manip. almacén entrada**, introduzca el número de días que desea incluir en el cálculo del compromiso de entrega.  

> [!NOTE]  
>  Si ha especificado un valor en el campo **Tiempo manip. almacén entrada** de la **Ficha almacén** para el almacén, este campo se utiliza como el tiempo de manipulación en el almacén de entrada predeterminado.  

### <a name="to-enter-inbound-warehouse-handling-time-on-location-cards"></a>Para especificar un tiempo de manipulación en almacén de entrada en las fichas de almacén  
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Almacén** y, a continuación, seleccione el vínculo relacionado.  
2.  Abra la ficha de almacén correspondiente.  
3.  En la ficha desplegable **Almacén**, en el campo **Tiempo manip. almacén entrada**, introduzca el número de días que desea que se incluya en el cálculo del compromiso de entrega.  

> [!NOTE]  
>  Si deja en blanco el campo **Tiempo manipulación almacén entrada**, el cálculo usa el valor de la ventana **Config. existencias**.

### <a name="to-enter-outbound-warehouse-handling-time-in-the-inventory-setup-window"></a>Para especificar un tiempo de manipulación en almacén de salida en la ventana de configuración de existencias  
Si desea configurar un tiempo de manipulación en almacén de salida para incluirlo en el cálculo del compromiso de entrega del pedido en la línea de venta, configúrelo como un valor predeterminado para las existencias.

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Configuración de inventario** y, a continuación, seleccione el vínculo relacionado.  
2. En la ficha desplegable **General**, en el campo **Tiempo manip. almacén salida**, introduzca el número de días que desea incluir en el cálculo del compromiso de entrega.  

> [!NOTE]  
>  Si ha especificado un valor en el campo **Tiempo manip. almacén salida** de la ficha Almacén, este campo se utiliza como el tiempo de manipulación en almacén de salida predeterminado.  

### <a name="to-enter-outbound-warehouse-handling-time-on-location-cards"></a>Para especificar un tiempo de manipulación en almacén de salida en las fichas almacén  
1.  Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Almacenes** y, a continuación, seleccione el vínculo relacionado.  
2.  Abra la ficha de almacén correspondiente.  
3.  En la ficha desplegable **Almacén**, en el campo **Tiempo manip. almacén salida**, introduzca el número de días que desea incluir en el cálculo del compromiso de entrega.  

> [!NOTE]  
>  Si deja en blanco el campo **Tiempo manipulación almacén salida**, el cálculo usa el valor de la ventana **Config. existencias**.

## <a name="to-make-an-item-critical"></a>Para identificar un producto como crítico  
Para que un producto se pueda incluir en el cálculo del compromiso de entrega, debe marcarse como crítico. Esta configuración garantiza que los elementos no críticos no causen cálculos de compromiso de entrega de pedidos irrelevantes.   
1.  Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Productos** y, a continuación, seleccione el vínculo relacionado.  
2.  Abra la ficha de producto que corresponda.  
3.  En la ficha desplegable **Planificación**, seleccione el campo **Crítico**.  

## <a name="to-calculate-an-order-promising-date"></a>Para calcular una fecha de compromiso de entrega de pedido  
1.  Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Pedido de venta** y, a continuación, seleccione el vínculo relacionado.  
2.  Abra el pedido de venta pertinente y seleccione las líneas del pedido de venta que desea calcular.  
3.  Seleccione la acción **Comprom. entreg.** y, a continuación elija **Líneas compromiso entrega pedido**.  
4.  Seleccione una línea y, a continuación, una de las siguientes opciones:  

    - Seleccione **Neto no comprometido** si desea calcular la fecha más temprana en que el producto estará disponible en función de las existencias, las recepciones programadas y los requerimientos brutos.  
    - Seleccione **Capaz de comprometer** si sabe que el producto está actualmente fuera de stock y desea calcular la fecha más temprana en que podría estar disponible emitiendo nuevas órdenes de reposición.  
5.  Elija el botón **Aceptar** para aceptar la fecha de envío más próxima disponible.  

## <a name="see-also"></a>Consulte también  
[Ccial](sales-manage-sales.md)  
[Cálculo de la fecha de compras](purchasing-date-calculation-for-purchases.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

