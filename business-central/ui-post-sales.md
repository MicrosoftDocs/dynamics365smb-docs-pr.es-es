---
title: "Descripción de cómo registrar documentos de venta | Documentos de Microsoft"
description: "Obtenga información sobre las diversas funciones de registro para registrar documentos de venta."
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/01/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 04807ffbb2d009ae309c499f62e48fa93437b8b5
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="posting-sales"></a>Registrar ventas
En **Grupo contable** en un documento de ventas, puede elegir entre las funciones de registro siguientes:

* **Registrar**
* **Informe de prueba**
* **Registrar y enviar**
* **Registrar e imprimir**
* **Registrar y enviar por correo electrónico**
* **Registrar por lotes**
* **Vista previa de registro**

Una vez completadas todas las líneas e introducida toda la información en el pedido de venta, puede registrarlo. Esto crea un envío y una factura.

Cuando se registra un pedido de venta, se actualiza la cuenta del cliente, la contabilidad y los movimientos de producto.

Para cada pedido de venta, se crea un movimiento de venta en la tabla **Mov. contabilidad**. Se crea también un movimiento en la cuenta de cliente de la tabla **Mov. cliente** y un movimiento de contabilidad en la cuenta de cliente correspondiente. Además, el registro del pedido puede dar como resultado un movimiento de IVA y uno de contabilidad para el importe de descuento. El registro de un movimiento para el descuento depende del contenido del campo **Registro dto.** de la ventana **Conf. ventas y cobros**.

Por cada línea de pedido de venta, se creará un movimiento de producto en la tabla **Mov. producto** (si las líneas de venta contienen números de producto) o un movimiento de contabilidad en la tabla **Mov. contabilidad** (si las líneas de venta contienen una cuenta de contabilidad). Además, los pedidos de venta siempre se registran en las tablas **Histórico cab. albarán venta** y **Histórico cab. factura venta**.

> [!IMPORTANT]  
>   Cuando registre un pedido, puede crear un albarán de venta y una factura. Esto se puede realizar al mismo tiempo o de manera independiente. También puede crear un envío y una factura parciales completando los campos **Cantidad a enviar** y **Cantidad a facturar** en las líneas individuales del pedido de venta antes de registrar. Tenga en cuenta que no se puede crear una factura de algo que no se ha enviado. Es decir, para poder facturar, debe haber registrado un envío, o bien debe elegir enviar y facturar al mismo tiempo.

Una vez completado el registro, las líneas de venta registradas se quitan del pedido. Al terminar el registro aparece un mensaje de aviso. Después de esto, podrá ver los movimientos registrados en las diferentes ventanas que los contienen, como **Movs. cliente**, **Movs. contabilidad**, **Movs. producto**, **Histórico albaranes ventas** y **Histórico facturas venta**.

## <a name="see-also"></a>Consulte también
[Ventas](sales-manage-sales.md)  
[Enviar documentos por correo electrónico](ui-how-send-documents-email.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)


