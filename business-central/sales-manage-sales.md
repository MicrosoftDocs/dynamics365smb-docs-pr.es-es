---
title: Resumen de tareas para administrar las ventas | Documentos de Microsoft
description: "Describe cómo gestionar las actividades de ventas."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade, sell
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 6c8c3f39d782a33896e531c4bfdf95b589458f99
ms.contentlocale: es-es
ms.lasthandoff: 09/28/2018

---
# <a name="sales"></a>Ccial
Puede crear una factura o un pedido de ventas para registrar el contrato con un cliente para vender determinados productos según términos de entrega y pago determinados.

Debe usar pedidos de venta si el proceso de venta requiere que pueda enviar parte de una cantidad del pedido, por ejemplo, porque la cantidad total no está disponible a la vez. Si vende productos que se entregan directamente desde el proveedor al cliente, como envío directo, deberá usar también pedidos de ventas. En todos los demás aspectos, los pedidos de venta funcionan de la misma forma que las facturas de venta. Con los pedidos de venta, puede utilizar la función compromiso de pedido para comunicar determinadas fechas de entrega a sus clientes.  

Puede negociar con el cliente creando primero creando una oferta de venta, que puede convertir en una factura de venta o pedido de venta cuando acuerde la venta. Después de que el cliente haya confirmado el contrato, puede enviar confirmación de pedido para registrar su obligación de entregar los productos según se ha acordado.

Puede corregir o cancelar fácilmente una factura de venta registrada antes de que se pague. Esto es útil si se desea corregir un error de escritura o si el cliente solicita un cambio temprano en el proceso de pedido. Si la factura de venta registrada se ha pagado, deberá crear un abono de venta o un pedido de devolución de venta para revertir la venta.

Las buenas prácticas de ventas y marketing consisten en tomar las mejores decisiones en los momentos adecuados. La funcionalidad de marketing de [!INCLUDE[d365fin](includes/d365fin_md.md)] proporciona un resumen preciso y puntual sobre la información de contacto para que pueda servir a sus clientes potenciales con más eficacia y aumentar la satisfacción de sus clientes. Para obtener más información, vea [Gestión de relaciones](marketing-relationship-management.md).

En entornos de negocio donde el cliente debe pagar antes de que los productos se entreguen, por ejemplo en la venta minorista, debe esperar la recepción del pago antes de entregar los productos. En la mayoría de casos, puede procesar los pagos entrantes algunas semanas después de la salida liquidando los pagos a las facturas relacionadas, registradas como facturas de ventas no pagadas . Para obtener más información, vea [Conciliar pagos con liquidación automática](receivables-how-reconcile-payments-auto-application.md).

Los documentos de ventas se pueden enviar como archivos PDF adjuntos al correo electrónico. El cuerpo del correo electrónico contendrá un extracto del documento de ventas, como los productos, el importe total y un vínculo al sitio web de PayPal. Para obtener más información, vea [Enviar documentos por correo electrónico](ui-how-send-documents-email.md).

Para todos los procesos de ventas, puede introducir un flujo de trabajo de aprobación, por ejemplo, para requerir que el administrador de contabilidad apruebe las compras grandes para ciertos clientes. Para obtener más información, consulte [Uso de flujos de trabajo](across-use-workflows.md).

En la tabla siguiente se indican una serie de tareas con vínculos a los temas que las describen.

| Para | Vea |
| --- | --- |
|Cree una ficha de cliente para cada cliente al que vende.|[Permite registrar nuevos clientes](sales-how-register-new-customers.md)|
| Crea una oferta de venta donde ofrece los productos según términos negociables antes de convertir la oferta en una factura de venta. |[Crear ofertas de ventas](sales-how-make-offers.md) |
| Crea una factura de venta para registrar el contrato con un cliente para vender productos según términos de entrega y pago determinados. |[Facturar ventas](sales-how-invoice-sales.md) |
| Procesar un pedido de ventas que requiera un envío parcial o directo. |[Vender productos](sales-how-sell-products.md) |
|Configurar líneas de ventas o compras estándar que puede insertar rápidamente en documentos, por ejemplo, para las órdenes de reposición periódicas.|[Crear líneas de ventas y de compras periódicas](sales-how-work-standard-lines.md)|  
| Vincular un pedido de ventas a una orden de compra para vender un producto de envío directo que se entregará directamente desde el proveedor al cliente. |[Realizar envíos directos](sales-how-drop-shipment.md) |
|Crear un producto del catálogo enviado desde un proveedor a su almacén para poder enviar el producto a su cliente.|[Crear pedidos especiales](sales-how-to-create-special-orders.md)|
| Realice una acción en una factura de venta registrada sin abonar para crear automáticamente un abono y para cancelar la factura de venta o regenerarla para poder hacer correcciones. |[Corregir o cancelar facturas de venta sin abonar](sales-how-correct-cancel-sales-invoice.md) |
| Crea un abono de venta para revertir una factura de venta registrada específica para reflejar qué productos devuelve el cliente y qué importe de pago se reembolsará. |[Procesamiento de devoluciones de ventas o cancelaciones](sales-how-process-sales-returns-cancellations.md) |
|Administrar el compromiso de su cliente para comprar grandes cantidades entregadas en varios envíos a lo largo del tiempo.|[Trabajar con pedidos de venta abiertos](sales-how-to-create-blanket-sales-orders.md)|
|Vender elementos de ensamblaje que no están disponibles actualmente mediante una orden de ensamblado vinculada para suministrar la cantidad total o parcial de la orden de venta.|[Venta de artículos ensamblados para pedido](assembly-how-to-sell-items-assembled-to-order.md)|
|Facturar a un cliente una vez por varios envíos, combinándolos en una única factura.|[Agrupar envíos en una factura única](sales-how-to-combine-shipments-on-a-single-invoice.md)|
|Informar a los clientes las fechas de entrega de los pedidos, mediante el cálculo de la fecha fecha capaz de comprometer o la fecha del neto no comprometido.|[Calcular fechas de compromiso de entrega de pedido](sales-how-to-calculate-order-promising-dates.md)|

## <a name="see-also"></a>Consulte también
[Configuración de ventas](sales-setup-sales.md)  
[Permite registrar nuevos clientes](sales-how-register-new-customers.md)  
[Administrar cobros](receivables-manage-receivables.md)  
[Administrar pagos](payables-manage-payables.md)  
[Administración de proyectos](projects-manage-projects.md)    
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Funciones empresariales generales](ui-across-business-areas.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  

