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
ms.date: 01/17/2020
ms.author: sgroespe
ms.openlocfilehash: 2565133adfab4fb5f6febeeccb69c4f3d6f59e71
ms.sourcegitcommit: 877af26e3e4522ee234fbba606615e105ef3e90a
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/28/2020
ms.locfileid: "2991885"
---
# <a name="posting-purchases"></a>Registrar compras
En **Grupo contable** en un documento de compra, puede elegir entre las funciones de registro siguientes:

* **Registrar**
* **Vista previa de registro**
* **Registrar e imprimir**
* **Informe de prueba**
* **Registrar por lotes**

Una vez completadas todas las líneas e introducida la información en el pedido de compra, podrá registrarlo; es decir, crear un albarán de compra y una factura.

Cuando se registra un pedido de compra, se actualiza la cuenta del proveedor, la contabilidad y los movimientos de producto.

Por cada pedido de compra, se crea un movimiento de compra en la tabla **Mov. contabilidad**. Se crea también un movimiento en la cuenta de proveedor de la tabla **Mov. proveedor** y un movimiento de contabilidad en la correspondiente cuenta de pagos. Además, el registro del pedido puede dar como resultado un movimiento de IVA y uno de contabilidad para el importe de descuento. El que se registre un movimiento para el descuento depende del contenido del campo **Registro dto.** de la página **Conf. compras y pagos**.

Por cada línea de pedido de compra, se creará un movimiento de producto en la tabla **Mov. producto** (si las líneas de compra contienen números de producto) o un movimiento de contabilidad en la tabla **Mov. contabilidad** (si las líneas de compra contienen una cuenta de contabilidad). Además, los pedidos de compra siempre se registran en las tablas **Histórico cab. albarán compra** e **Histórico cab. factura compra**.

Antes de comenzar a registrar, podrá imprimir un informe que contenga toda la información del pedido de compra y que indique cualquier error que pueda existir allí. Para imprimir este informe, elija **Registro** y, a continuación, **Informe de prueba**.

> [!IMPORTANT]  
>   Cuando registre un pedido, podrá crear tanto un albarán de compra como una factura. Esto se puede hacer simultánea o independientemente. También puede crear una recepción y una factura parciales completando los campos **Cantidad a recibir** o **Cantidad a facturar** en las líneas individuales del pedido de compra antes de registrar. Tenga en cuenta que no puede crear una factura de algo no se ha recibido. Es decir, antes de poder facturar debe haber registrado un albarán de compra o haber elegido recibir y facturar al mismo tiempo.

Puede registrar o registrar e imprimir. Si elije registrar e imprimir, un informe se imprime cuando se registre el pedido. También puede elegir la función **Registrar por lotes**, que permite registrar varios pedidos a la vez. Para obtener más información, consulte [Registrar varios documentos al mismo tiempo](ui-batch-posting.md).

## <a name="viewing-ledger-entries"></a>Ver movimientos
Una vez finalizado el registro, las líneas de compra registradas se quitan del pedido. Al terminar el registro aparece un mensaje de aviso. Después de esto, podrá ver los movimientos registrados en las diferentes páginas que los contienen, como **Movs. proveedores**, **Movs, contabilidad**, **Movs. productos**, **Albaranes compra** e **Histórico facturas compra**.

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
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
