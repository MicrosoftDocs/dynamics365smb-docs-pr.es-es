---
title: Registrar varios documentos al mismo tiempo
description: Aprenda a seleccionar varios documentos no publicados en una lista para la publicación por lotes inmediata o programada en Business Central.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: null
ms.reviewer: edupont
ms.date: 06/25/2021
ms.author: edupont
---
# <a name="post-multiple-documents-at-the-same-time"></a><a name="post-multiple-documents-at-the-same-time"></a><a name="post-multiple-documents-at-the-same-time"></a>Registrar varios documentos al mismo tiempo

En lugar de registrar documentos individuales uno por uno, puede seleccionar varios documentos no registrados en una lista para el registro inmediato o para el registro por lotes según una programación, por ejemplo, al final del día. Esto puede ser útil solo si un supervisor puede registrar documentos creados por otros usuarios o para evitar problemas de rendimiento del sistema del registro durante las horas de trabajo.

## <a name="to-post-multiple-purchase-orders-immediately"></a><a name="to-post-multiple-purchase-orders-immediately"></a><a name="to-post-multiple-purchase-orders-immediately"></a>Para registrar varios pedidos de compra inmediatamente

El siguiente procedimiento explica cómo registrar varios pedidos de compra inmediatamente. Los pasos son parecidos a todos los documentos de compra y venta.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Pedidos de compra** y, a continuación, elija el vínculo relacionado.
2. En la página **Pedidos de compra**, seleccione todos los pedidos que se registrarán:
3. En el campo **N.º**, elija los tres puntos verticales para abrir el menú contextual y luego elija la acción **Seleccionar más**.
4. Seleccione la casilla para todas las líneas que representan los pedidos que desea registrar al mismo tiempo.
5. Elija la acción **Registro** y, a continuación, seleccione la acción **Registrar**.
6. Elija el botón **Sí** en el mensaje de confirmación.

## <a name="to-batch-post-multiple-purchase-orders"></a><a name="to-batch-post-multiple-purchase-orders"></a><a name="to-batch-post-multiple-purchase-orders"></a>Para registrar por lotes varios pedidos de compra

El siguiente procedimiento explica cómo registrar por lotes los pedidos de compra. Los pasos son similares para todos los documentos de compra y venta donde la acción **Registro por lotes** está disponible.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Pedidos de compra** y, a continuación, elija el vínculo relacionado.  
2. En la página **Pedidos de compra**, seleccione todos los pedidos que se registrarán:
3. En el campo **N.º**, elija los tres puntos verticales para abrir el menú contextual y luego elija la acción **Seleccionar más**.
4. Seleccione la casilla para todas las líneas que representan los pedidos que desea registrar al mismo tiempo.
5. Elija la acción **Registro** y, a continuación, seleccione la acción **Registrar por lotes**.
6. En la página **Reg. lotes pedidos compra**, rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
7. Elija el botón **Aceptar**.
8. Para ver posibles problemas que han sucedido durante el registro por lotes de documentos, abra la página **Registro de mensajes de error**.

> [!NOTE]
> La publicación de varios documentos puede llevar algún tiempo y bloquear a otros usuarios. Considere habilitar la publicación en segundo plano. Para obtener más información, consulte [Uso de colas de proyectos para programar tareas](admin-job-queues-schedule-tasks.md).

## <a name="to-set-up-background-posting-with-job-queues"></a><a name="to-set-up-background-posting-with-job-queues"></a><a name="to-set-up-background-posting-with-job-queues"></a>Para configurar el registro de fondo con colas de proyecto
Las colas de proyecto son una herramienta eficaz para programar la ejecución de procesos de negocios en segundo plano, como cuando varios usuarios intentan publicar pedidos de ventas, pero solo se puede procesar un pedido a la vez.  

El siguiente procedimiento explica cómo configurar el registro en segundo plano de los pedidos de ventas. Los pasos son parecidos para la compra.  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración de ventas y cobros** y luego elija el enlace relacionado.
2. En la página **Configuración de ventas y cobros**, seleccione la casilla de verificación **Registrar con cola de proyectoss**.
3. Elija el campo **Cód. categoría cola proyectos** y especifique un código **SALESPOST**.

    > [!NOTE]
    > Algunos proyectos cambian los mismos datos y no deberían ejecutarse al mismo tiempo porque pueden causar conflictos. Por ejemplo, los proyectos en segundo plano para documentos de ventas intentarán modificar los mismos datos al mismo tiempo. Las categorías de la cola de proyectos ayudan a prevenir este tipo de conflictos al garantizar que cuando se ejecuta un proyecto, otro proyecto que pertenece a la misma categoría de cola de proyectos no se ejecutará hasta que finalice. Por ejemplo, un proyecto que pertenece a una categoría de cola de proyectos de ventas esperará hasta que se realicen todos los demás proyectos relacionados con las ventas. Usted especifica una categoría de cola de proyectos en la ficha desplegable de **Registro de fondo** en la página **Configuración de ventas y cobros**.
    >
    > [!INCLUDE[prod_short](includes/prod_short.md)] proporciona categorías de cola de proyectos para ventas, compras y contabilidad. Recomendamos que siempre se especifique uno de estos, o uno que cree usted. Si experimenta fallos debido a conflictos, considere configurar una categoría para todas las ventas, compras y publicaciones de contabilidad.

    Si también desea que los documentos de ventas se impriman cuando se registren, seleccione la casilla de verificación **Registrar e imprimir con cola de proyectoss** en la página **Configuración de ventas y cobros**.  
    Si selecciona **PDF** en el campo **Tipo de salida de informe**, los pedidos de compra registrados correctamente estarán disponibles en la parte **Bandeja de entrada de informes** de su área de trabajo.

    > [!IMPORTANT]  
    > Si configura un proyecto que va a registrar e imprimir documentos y la impresora muestra un cuadro de diálogo, como una solicitud de credenciales o una advertencia sobre un nivel bajo de tinta de impresora, el documento se registra pero no se imprime. Finalmente, el tiempo de espera del movimiento de cola de proyectos correspondiente se agota y el campo **Estado** se establece **Error**. Por consiguiente, es recomendable no utilizar una configuración de impresora que requiere la interacción con la pantalla de cuadros de diálogo de la impresora junto con el registro en segundo plano.

    La próxima vez que registre documentos de ventas, [!INCLUDE [prod_short](includes/prod_short.md)]crea automáticamente una entrada en la cola de proyectos para cada documento y ejecuta los trabajos en segundo plano, uno por uno.

4. Para verificar que la cola de proyectos funciona como se esperaba, registre un pedido de venta. Para obtener más información, vea [Vender productos](sales-how-sell-products.md).
    Los pedidos de venta ahora se agregarán a una entrada de cola de proyectos dedicada, que define cuándo se registran los documentos. 

### <a name="to-view-status-from-a-sales-or-purchase-document"></a><a name="to-view-status-from-a-sales-or-purchase-document"></a><a name="to-view-status-from-a-sales-or-purchase-document"></a>Para ver el estado de un documento de compra o de venta
Si la cola de proyectos no puede registrar el pedido de venta, cambie el estado a **Error** y el pedido de venta se agregará a la lista de pedidos de venta que el usuario debe administrar manualmente.
1. Desde el documento que ha intentado registrar con el registro en segundo plano, seleccione el campo **Estado de la cola de proyectos**, que contendrá **Error**.
2. Revise el mensaje de error y corrija el problema.

Alternativamente, puede revisar si el pedido de ventas se publicó correctamente en la página **Movs. registro cola proyecto**. Para obtener más información, consulte la sección [Supervisar la cola de proyectos](#monitor-the-job-queue).

## <a name="to-create-a-job-queue-entry-for-batch-posting-of-sales-orders"></a><a name="to-create-a-job-queue-entry-for-batch-posting-of-sales-orders"></a><a name="to-create-a-job-queue-entry-for-batch-posting-of-sales-orders"></a>Para crear un movimiento de la cola de proyectos para el registro por lotes de pedidos de ventas

Alternativamente, puede posponer los registros para horas en que resulta adecuado para su organización. Por ejemplo, para su empresa puede tener sentido ejecutar ciertas rutinas cuando la mayor parte de la introducción de datos del día ha concluido. Para hacerlo, configure la cola de proyectos para que ejecute varios informes de registro por lotes, como el **Reg. lotes pedidos venta**, el **Reg. lotes facturas ventas** e informes similares. [!INCLUDE[prod_short](includes/prod_short.md)] admite el registro en segundo plano para todos los documentos de ventas, compras y servicios.

El siguiente procedimiento muestra cómo configurar el informe **Reg. lotes pedidos venta** para que se registren automáticamente los pedidos de ventas a las 4:00 en días hábiles.  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Movimientos de cola de proyectos** y luego elija el enlace relacionado.  
2. Seleccione la acción **Nuevo**.  
3. En el campo **Tipo objeto para ejecutar**, seleccione **Informe**.  
4. En el campo **Id. objeto para ejecutar**, seleccione 296, **Reg. lotes pedidos venta**.

   También puede utilizar los siguientes informes:
  
   * 900 **Reg. lotes pedidos ensamblado**
   * 497 **Reg. lotes facturas compra**
   * 496 **Reg. lotes pedidos compra**
   * 498 **Reg. lotes abonos compra**
   * 6665 **Reg. lotes pedidos devolución**
   * 298 **Reg. lotes abonos venta**
   * 297 **Reg. lotes facturas ventas**
   * 296 **Reg. lotes pedidos venta**
   * 6655 **Reg. lotes devoluciones ventas**
   * 6005 **Reg. lotes abonos servicio**
   * 6004 **Reg. lotes facturas servicio**
   * 6001 **Reg. lotes ped. servicio**

5. Seleccione la casilla **Página de solicitud de informe**.
6. En la página de solicitud **Reg. lotes pedidos venta**, defina qué se incluye durante el registro automático de pedidos de ventas y luego elija el botón **Aceptar**.

    > [!IMPORTANT]
    > Recuerde establecer filtros estrictos; de otra manera, [!INCLUDE [prod_short](includes/prod_short.md)] publicará todos los documentos, incluso si no están listos. Considere establecer un filtro en el campo **Estado** para el valor *Publicado* y un filtro en el campo **Fecha de publicación** para el valor *..hoy*. Para obtener más información, consulte [Ordenar, buscar y filtrar](ui-enter-criteria-filters.md).
7. Seleccione todas las casillas de verificación desde **Ejecutar los lunes** hasta **Ejecutar los viernes**.
8. En el campo **Hora de inicio**, introduzca 4:00.
9. Elija la acción **Establecer estado en Preparado**.

Los pedidos de venta que estén en filtros definidos ahora se registrarán cada día de la semana a las 4:00.

## <a name="monitor-the-job-queue"></a><a name="monitor-the-job-queue"></a><a name="monitor-the-job-queue"></a>Supervisar la cola de proyectos

Si configura la publicación en segundo plano con colas de proyectos, conviértalo en una tarea periódica para supervisar la cola de proyectos para detectar cualquier problema. Puede hacer un seguimiento del estado en la página **Movimientos de cola de proyectos**. Para obtener más información, consulte [Uso de colas de proyectos para programar tareas](admin-job-queues-schedule-tasks.md).  

Como administrador, puede utilizar [Application Insights](/azure/azure-monitor/app/app-insights-overview) para recopilar y analizar la telemetría que puede utilizar para identificar problemas. Para obtener más información, consulte [Supervisión y análisis de la telemetría](/dynamics365/business-central/dev-itpro/administration/telemetry-overview) en el contenido de desarrolladores y administración.  

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Consulte también

[Registrar documentos y diarios](ui-post-documents-journals.md)  
[Uso de colas de proyectos para programar tareas](admin-job-queues-schedule-tasks.md)  
[Editar documentos registrados](across-edit-posted-document.md)  
[Corregir o cancelar facturas de compra sin abonar](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
[Búsqueda de páginas e información con Dígame](ui-search.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
