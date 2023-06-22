---
title: Registro de documentos de ventas
description: Obtenga información sobre las diferentes funciones de registro para registrar documentos de ventas y cómo puede actualizar los documentos registrados.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.search.form: '130, 142, 1350'
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="posting-sales" />Registrar ventas

En el menú **Registro** en un documento de venta, puede elegir entre las funciones de registro siguientes:

* **Registrar**
* **Registrar y nuevo**
* **Registrar y enviar**
* **Vista previa de registro**
* **Registrar por lotes**
* **Informe de prueba**

> [!NOTE]
> Para pedidos de cliente, también puede ver opciones relacionadas con la funcionalidad de prepagos. Para obtener más información, consulte [Facturar prepagos](finance-invoice-prepayments.md).

Una vez completadas todas las líneas e introducida toda la información en el pedido de venta, puede registrarlo. Esto crea un envío y una factura.

Cuando se registra un pedido de venta, se actualiza la cuenta del cliente, la contabilidad y los movimientos de producto.

Para cada pedido de venta, se crea un movimiento de venta en la tabla **Mov. contabilidad**. Se crea también un movimiento en la cuenta de cliente de la tabla **Mov. cliente** y un movimiento de contabilidad en la cuenta de cliente correspondiente. Además, el registro del pedido puede dar como resultado un movimiento de IVA y uno de contabilidad para el importe de descuento. El registro de un movimiento para el descuento depende del contenido del campo **Registro dto.** de la página **Conf. ventas y cobros**.

Por cada línea de pedido de venta, se creará un movimiento de producto en la tabla **Mov. producto** (si las líneas de venta contienen números de producto) o un movimiento de contabilidad en la tabla **Mov. contabilidad** (si las líneas de venta contienen una cuenta de contabilidad). Además, los pedidos de venta siempre se registran en las tablas **Histórico cab. albarán venta** y **Histórico cab. factura venta**.

[!INCLUDE [order-ship-invoice](includes/order-ship-invoice.md)]

Puede registrar o registrar y enviar. Si elige registrar y enviar, se genera un archivo PDF que luego podrá enviar. También puede elegir la función **Registrar por lotes**, que permite registrar varios pedidos a la vez. Para obtener más información, consulte [Registrar varios documentos al mismo tiempo](ui-batch-posting.md).

## <a name="viewing-ledger-entries" />Ver movimientos

Una vez completado el registro, las líneas de venta registradas se quitan del pedido. Al terminar el registro aparece un mensaje de aviso. Después de esto, podrá ver los movimientos registrados en las diferentes páginas que los contienen, como **Movs. cliente**, **Movs. contabilidad**, **Movs. producto**, **Histórico albaranes ventas** y **Histórico facturas venta**.  

En la mayoría de los casos, puede abrir movimientos desde la tarjeta o documento afectado. Por ejemplo, en la página **Ficha cliente**, seleccione la acción **Movimientos**.

## <a name="editing-ledger-entries" />Editar movimientos

Puede editar determinados campos en documentos de compra registrados, como **Nº seguimiento bulto**. . Para obtener más información, vea [Editar documentos registrados](across-edit-posted-document.md). Para campos más críticos que afectan el registro de auditoría, debe revertir o deshacer la publicación. Para obtener más información, vea [Revertir los registros de diario y deshacer los recibos/envíos](finance-how-reverse-journal-posting.md).

## <a name="see-related-microsoft-trainingtrainingmodulesship-invoice-items-dynamics--business-centralindex" />Consultar la [formación de Microsoft](/training/modules/ship-invoice-items-dynamics-365-business-central/index) relacionada

## <a name="see-also" />Consulte también

[Ccial](sales-manage-sales.md)  
[Registrar varios documentos al mismo tiempo](ui-batch-posting.md)  
[Editar documentos registrados](across-edit-posted-document.md)  
[Enviar documentos por correo electrónico](ui-how-send-documents-email.md)  
[Corregir o cancelar facturas de venta sin abonar](sales-how-correct-cancel-sales-invoice.md)  
[Búsqueda de páginas e información con Dígame](ui-search.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]  
