---
title: Campo de estado en los documentos
description: 'Obtenga información sobre los estados ''Abierto'' y ''Liberado'' en documentos de oferta, pedido o nota de abono.'
author: brentholtorf
ms.service: dynamics-365-business-central
ms.topic: conceptual
ms.search.keywords: 'document, status, quote, order, credit memo, released, open, pending approval, pending prepayment,'
ms.search.form: null
ms.date: 09/19/2022
ms.author: bholtorf
---
# <a name="status-field-on-documents"></a>Campo de estado en los documentos

Al crear una oferta, un pedido o un abono, el campo **Estado** de la cabecera del documento contiene el estado **Pendiente** de forma predeterminada.

Una vez rellenado el documento, láncelo y [!INCLUDE[prod_short](includes/prod_short.md)] modificará el valor del campo **Estado** a **Lanzado**. Este estado indica que el pedido está listo para pasar a la siguiente etapa del proceso antes de ser registrado.

| Status | Descripción |
| ------ | ----------- |
| Abierta   | Puede realizar cambios en el documento. |
| Lanzada | El documento ha sido lanzado a la siguiente etapa del proceso, por lo que no se podrán realizar cambios en las líneas del tipo *Producto* y *Activo fijo*.<br /><br />Para realizar cambios en el contenido del documento lanzado, puede volver a abrirlo. Para pasar el documento modificado a la etapa siguiente de procesamiento, deberá volver a lanzarlo. |
| Aprobación pendiente   | El documento está en espera de aprobación. |
| Prepago pendiente | Se ha registrado una factura de prepago para el documento. |

## <a name="release-process"></a>Proceso de versión

El proceso de lanzamiento se puede utilizar de varias formas distintas para facilitar el flujo de trabajo habitual, por ejemplo, para seguir los procedimientos de la empresa respecto de autorizaciones o para iniciar actividades de almacén.

### <a name="approval-procedures"></a>Procedimientos de aprobación

Utilice el procedimiento de lanzamiento en su empresa para indicar que otro usuario ha autorizado el documento, o que un contacto externo puede cumplir las especificaciones del documento, como se muestra en los siguientes ejemplos:

* El pedido de compra sólo se puede lanzar cuando el proveedor ha indicado que ya puede atender el pedido.
* Cree un pedido para que lo autorice un segundo usuario, por motivos de seguridad probablemente, antes de que pueda lanzarlo.
* El abono que creó debe ser lanzado por el director responsable de autorizar todos los reembolsos.

Obtenga más información sobre los flujos de trabajo de aprobación en [Usar flujos de trabajo](across-use-workflows.md).

### <a name="warehouse-activities"></a>Actividades de almacén

Si el estado del pedido es **Pendiente**, el almacén no iniciará los preparativos del envío ni esperará recibir los productos de un pedido de compra. Cuando lance el pedido, indique que está completo y que el almacén puede incluirlo en sus actividades.

## <a name="reopen-a-released-order"></a>Reapertura de un pedido lanzado

Para modificar un pedido lanzado, debe abrirlo de nuevo. Pero, sólo podrá incrementar la cantidad de las líneas ya procesadas por el almacén.

Una vez haga los cambios y lanzado el pedido de nuevo, [!INCLUDE [prod_short](includes/prod_short.md)] vuelve a calcular el impuesto sobre el valor añadido (IVA) y el descuento en factura.

Si modifica un pedido lanzado, debe notificar dichos cambios al almacén.

> [!NOTE]
> Si desea registrar un solo abono o pedido pendiente sin lanzarlo previamente, [!INCLUDE [prod_short](includes/prod_short.md)] lanzará el documento automáticamente cuando lo registre. Si registra los pedidos o abonos con la función **Registrar por lotes**, si lo desea puede registrar únicamente los pedidos o abonos que ha lanzado.

## <a name="see-also"></a>Consulte también .

[Vender productos con un pedido de venta de cliente](sales-how-sell-products.md)  
[Registrar compras con facturas de compra](purchasing-how-record-purchases.md)  
[Enviar productos](warehouse-how-ship-items.md)  
[Recibir productos](warehouse-how-receive-items.md)  
[Usar flujos de trabajo de aprobación del producto](across-how-use-approval-workflows.md)  
[Ordenar, buscar y filtrar listas](ui-enter-criteria-filters.md)  
[Archivar documentos](across-how-to-archive-documents.md)  
[Funciones empresariales generales](ui-across-business-areas.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
