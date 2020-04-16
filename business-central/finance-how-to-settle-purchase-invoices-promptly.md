---
title: Liquidación de facturas de compra inmediatamente | Documentos de Microsoft
description: Si necesita pagar al proveedor en efectivo o con cheque, puede hacer que se realice el registro correspondiente cuando se registra la factura.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: bholtorf
ms.openlocfilehash: ec5723088553141c1f6df55ba8bac3303ee4e2bd
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/01/2020
ms.locfileid: "3183265"
---
# <a name="settle-purchase-invoices-promptly"></a>Liquidar facturas de compra inmediatamente
Si necesita pagar al proveedor en efectivo o con cheque, puede registrar el pago cuando registra la factura.  

### <a name="to-settle-purchase-invoices-promptly"></a>Para liquidar facturas de compra inmediatamente  
1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Facturas de compra** y luego elija el enlace relacionado.  
2. Seleccione la acción **Nuevo**.  
3.  Para pagar en efectivo o mediante transferencia bancaria, introduzca el número de cuenta de caja o de banco en el campo **Cuenta contrapartida**.  

> [!IMPORTANT]  
>  Los campos **Tipo contrapartida** y **Cuenta contrapartida** no forman parte del formato estándar de la cabecera de factura. Para registrar el pago de una factura, primero deberá insertarlos con las utilidades de diseño. Para obtener más información, consulte [Personalizar el área de trabajo](ui-personalization-user.md). 

> [!NOTE]  
>  Si paga a menudo facturas de compra en efectivo, se recomienda que configure una forma de pago específica con una cuenta de contrapartida e introduzca la forma en el campo **Forma de pago** de la ficha de proveedor. Se inserta automáticamente el número de cuenta de contrapartida en la cabecera de la factura cada vez que se crea una factura nueva.  

## <a name="see-also"></a>Consulte también  
[Administrar pagos](payables-manage-payables.md)  
[Compras](purchasing-manage-purchasing.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
