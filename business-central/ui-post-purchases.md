---
title: Descripción de cómo registrar documentos de compra | Documentos de Microsoft
description: Obtenga información sobre las diferentes funciones de registro para registrar documentos de compra y cómo puede actualizar los documentos registrados.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 78657265e45aa9eb01d56a65aab8366c24b3d39a
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "4756747"
---
# <a name="posting-purchases"></a>Registrar compras
En un documento de compra, puede elegir entre las acciones de registro siguientes:

* **Registrar**
* **Vista previa de registro**
* **Registrar e imprimir**
* **Informe de prueba**
* **Registrar por lotes**

Cuando se registra un documento de compra, se actualiza la cuenta del proveedor, la contabilidad, los movimientos de producto y los movimientos de recursos.

Por cada documento de compra, se crea un movimiento de compra en la tabla **Mov. contabilidad**. Se crea también un movimiento en la cuenta de proveedor de la tabla **Mov. proveedor** y un movimiento de contabilidad en la correspondiente cuenta de pagos. Además, el registro de la compra puede dar como resultado un movimiento de IVA y uno de contabilidad para el importe de descuento. El que se registre un movimiento para el descuento depende del contenido del campo **Registro dto.** de la página **Conf. compras y pagos**.

Para cada línea de compra, se crearán las siguientes entradas:
- Una entrada en la tabla **Mov. producto** si la línea de compra es de tipo **Producto**.
- Una entrada en la tabla **Mov. contabilidad** si las líneas de compra son de tipo **Cuenta**.
- Una entrada en la tabla **Movimiento de recurso** si la línea de compra es de tipo **Recurso**.

Además, los documentos de compra siempre se registran en las tablas **Histórico cab. albarán compra** e **Histórico cab. factura compra**.

Antes de comenzar a registrar, podrá imprimir un informe que contenga toda la información del pedido de compra y que indique cualquier error que pueda existir allí. Para imprimir este informe, elija **Registro** y, a continuación, **Informe de prueba**.

> [!IMPORTANT]  
>   Cuando registre un pedido de compra para productos, podrá crear tanto un albarán de compra como una factura. Esto se puede hacer simultánea o independientemente. También puede crear una recepción y una factura parciales completando los campos **Cantidad a recibir** o **Cantidad a facturar** en las líneas individuales del pedido de compra antes de registrar. Tenga en cuenta que no puede crear una factura de algo no se ha recibido. Es decir, antes de poder facturar debe haber registrado un albarán de compra o haber elegido recibir y facturar al mismo tiempo.

Puede registrar o registrar e imprimir. Si elije registrar e imprimir, un informe se imprime cuando se registre el pedido. También puede elegir la función **Registrar por lotes**, que permite registrar varios pedidos a la vez. Para obtener más información, consulte [Registrar varios documentos al mismo tiempo](ui-batch-posting.md).

## <a name="viewing-ledger-entries"></a>Ver movimientos
Una vez finalizado el registro, las líneas de compra registradas se quitan del pedido. Al terminar el registro aparece un mensaje de aviso. Después de esto, podrá ver los movimientos registrados en las diferentes páginas que los contienen, como **Movs. proveedores**, **Movs, contabilidad**, **Movs. productos**, **Movimientos de recursos**, **Albaranes compra** e **Histórico facturas compra**.

En la mayoría de los casos, puede abrir movimientos desde la tarjeta o documento afectado. Por ejemplo, en la página **Ficha proveedor**, seleccione la acción **Entradas**.

## <a name="editing-ledger-entries"></a>Editar movimientos
Puede editar determinados campos en documentos de compra registrados, como el campo **Referencia pago**. Para obtener más información, vea [Editar documentos registrados](across-edit-posted-document.md). Para campos más críticos que afectan el registro de auditoría, debe revertir o deshacer la publicación. Para obtener más información, vea [Revertir los registros de diario y deshacer los recibos/envíos](finance-how-reverse-journal-posting.md).

## <a name="see-related-training-at-microsoft-learn"></a>Consulte Formación relacionada en [Microsoft Learn](/learn/modules/receive-invoice-dynamics-d365-business-central/index)

## <a name="see-also"></a>Consulte también
[Editar documentos registrados](across-edit-posted-document.md)  
[Registrar varios documentos al mismo tiempo](ui-batch-posting.md)  
[Compras](purchasing-manage-purchasing.md)  
[Registrar documentos y diarios](ui-post-documents-journals.md)  
[Corregir o cancelar facturas de compra sin abonar](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
[Búsqueda de páginas e información con Dígame](ui-search.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]