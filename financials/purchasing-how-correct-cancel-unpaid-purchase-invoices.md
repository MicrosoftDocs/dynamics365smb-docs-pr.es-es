---
title: Modificar o cancelar facturas de compra sin abonar | Documentos de Microsoft
description: "Explica cómo corregir, cancelar o deshacer una factura de compra registrada y crear automáticamente un abono de compra."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: undo, credit memo, return
ms.date: 08/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 53800a9fe42934807c551e81098eda768f4f1542
ms.contentlocale: es-es
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-correct-or-cancel-unpaid-purchase-invoices"></a>Corrección o cancelación de facturas de compra sin abonar
Puede corregir o cancelar una factura de compra registrada. Esto es útil si se desea corregir un error de escritura o si desea cambiar la compra de forma anticipada en el proceso de pedido.

Si ya ha pagado productos en la factura de compra registrada, no puede corregirla o cancelarla desde la factura de compra registrada en sí. En su lugar, debe crear manualmente un abono de compra para revertir la compra, opcionalmente administrada con una orden de devolución de compra. Para obtener más información, vea [Procedimiento: Procesar devoluciones de compra o cancelaciones](purchasing-how-process-purchase-returns-cancellations.md).

En la ventana **Factura de compra registrada**, puede elegir el botón **Corregir** o **Cancelar**. Al corregir o cancelar una factura de compra registrada, el abono de compra de corrección se aplica a todos los movimientos contables y del inventario que se crearon cuando se registró la factura de compra inicial. De esta forma se invierte la factura de compra registrada en los registros financieros deja el abono de compra registrado de corrección para el seguimiento de auditoria. A continuación se describe el uso de **Corregir** y **Cancelar**.

## <a name="to-correct-a-posted-purchase-invoice"></a>Para corregir una factura de compra registrada
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Histórico facturas compra** y, a continuación, seleccione el vínculo relacionado.  
2. Seleccione la factura de compra registrada que desea corregir.  

    > [!NOTE]  
>   Si se selecciona la casilla **Cancelado**, no puede corregir la factura de compra registrada porque ya se ha corregido o cancelado.
3. En la ventana **Factura de compra registrada**, elija **Corregir**.

    Una nueva factura de compra con la misma información se crea donde puede realizar la corrección. Para obtener más información, consulte [Procedimiento: Registrar compras](purchasing-how-record-purchases.md). El campo **Cancelado** en la factura de compra registrada inicial se cambia a **Sí**.

    Un abono de compra se crea y se registra automáticamente para anular la factura de compra registrada inicialmente.
4. Elija **Mostrar abono correctivo** para ver el histórico de abonos de compra que anula la factura de compra registrada inicial.

## <a name="to-cancel-a-posted-purchase-invoice"></a>Para cancelar una factura de compra registrada
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Histórico facturas compra** y, a continuación, seleccione el vínculo relacionado.  
2. Seleccione la factura de compra registrada que desea cancelar.

    > [!NOTE]  
>   Si se selecciona la casilla **Cancelado**, no puede cancelar la factura de compra registrada porque ya se ha cancelado o corregido.
3. En la ventana **Factura de compra registrada**, elija **Cancelar**.

    Un abono de compra se crea y se registra automáticamente para anular la factura de compra registrada inicialmente. El campo **Cancelado** en la factura de compra registrada inicial se cambia a **Sí**.
4. Elija **Mostrar abono correctivo** para ver el histórico de abonos de compra que anula la factura de compra registrada inicial.

## <a name="see-also"></a>Consulte también
[Compras](purchasing-manage-purchasing.md)  
[Registro de compras](purchasing-how-record-purchases.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

