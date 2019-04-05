---
title: Liquidación de facturas de compra inmediatamente | Documentos de Microsoft
description: Si necesita pagar al proveedor en efectivo o con cheque, puede hacer que se realice el registro correspondiente cuando se registra la factura.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: bholtorf
ms.openlocfilehash: 402632f7ce6e721310c3fc3ccfb93e58eae641e5
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/08/2019
ms.locfileid: "806012"
---
# <a name="settle-purchase-invoices-promptly"></a>Liquidar facturas de compra inmediatamente
Si necesita pagar al proveedor en efectivo o con cheque, puede registrar el pago cuando registra la factura.  
  
### <a name="to-settle-purchase-invoices-promptly"></a>Para liquidar facturas de compra inmediatamente  
1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Facturas compra** y luego elija el enlace relacionado.  
2. En la pestaña **Inicio**, elija **Nuevo**.  
3.  Para pagar en efectivo o mediante transferencia bancaria, introduzca el número de cuenta de caja o de banco en el campo **Cuenta contrapartida**.  
  
> [!IMPORTANT]  
>  Los campos **Tipo contrapartida** y **Cuenta contrapartida** no forman parte del formato estándar de la cabecera de factura. Para registrar el pago de una factura, primero deberá insertarlos con las utilidades de diseño.  
  
> [!NOTE]  
>  Si paga a menudo facturas de compra en efectivo, se recomienda que configure una forma de pago específica con una cuenta de contrapartida e introduzca la forma en el campo **Forma de pago** de la ficha de proveedor. Se inserta automáticamente el número de cuenta de contrapartida en la cabecera de la factura cada vez que se crea una factura nueva.  
  
## <a name="see-also"></a>Consulte también  
[Administrar pagos](payables-manage-payables.md)  
[Compras](purchasing-manage-purchasing.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)