---
title: Registro de documentos de ventas
description: Obtenga información sobre las diferentes funciones de registro para registrar documentos de ventas y cómo puede actualizar los documentos registrados.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: e59c48c31e897d235c7920f4231313a2332fdf06
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2021
ms.locfileid: "5783264"
---
# <a name="posting-sales"></a>Registrar ventas

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

> [!IMPORTANT]  
> Cuando registre un pedido, puede crear un albarán de venta y una factura. Esto se puede realizar al mismo tiempo o de manera independiente. También puede crear un envío y una factura parciales completando los campos **Cantidad a enviar** y **Cantidad a facturar** en las líneas individuales del pedido de venta antes de registrar. Tenga en cuenta que no se puede crear una factura de algo que no se ha enviado. Es decir, para poder facturar, debe haber registrado un envío, o bien debe elegir enviar y facturar al mismo tiempo.

Puede registrar o registrar y enviar. Si elige registrar y enviar, se genera un archivo PDF que luego podrá enviar. También puede elegir la función **Registrar por lotes**, que permite registrar varios pedidos a la vez. Para obtener más información, consulte [Registrar varios documentos al mismo tiempo](ui-batch-posting.md).

## <a name="viewing-ledger-entries"></a>Ver movimientos

Una vez completado el registro, las líneas de venta registradas se quitan del pedido. Al terminar el registro aparece un mensaje de aviso. Después de esto, podrá ver los movimientos registrados en las diferentes páginas que los contienen, como **Movs. cliente**, **Movs. contabilidad**, **Movs. producto**, **Histórico albaranes ventas** y **Histórico facturas venta**.  

En la mayoría de los casos, puede abrir movimientos desde la tarjeta o documento afectado. Por ejemplo, en la página **Ficha cliente**, seleccione la acción **Movimientos**.

## <a name="editing-ledger-entries"></a>Editar movimientos

Puede editar determinados campos en documentos de compra registrados, como **Nº seguimiento bulto**. . Para obtener más información, vea [Editar documentos registrados](across-edit-posted-document.md). Para campos más críticos que afectan el registro de auditoría, debe revertir o deshacer la publicación. Para obtener más información, vea [Revertir los registros de diario y deshacer los recibos/envíos](finance-how-reverse-journal-posting.md).

## <a name="see-related-training-at-microsoft-learn"></a>Consulte Formación relacionada en [Microsoft Learn](/learn/modules/ship-invoice-items-dynamics-365-business-central/index)

## <a name="see-also"></a>Consulte también

[Ccial](sales-manage-sales.md)  
[Registrar varios documentos al mismo tiempo](ui-batch-posting.md)  
[Editar documentos registrados](across-edit-posted-document.md)  
[Enviar documentos por correo electrónico](ui-how-send-documents-email.md)  
[Corregir o cancelar facturas de venta sin abonar](sales-how-correct-cancel-sales-invoice.md)  
[Búsqueda de páginas e información con Dígame](ui-search.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]  
