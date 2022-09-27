---
title: Corregir prepagos
description: Puede realizar una corrección en un pedido después de haber registrado una factura de prepago para el pedido y agregar nuevas líneas a un pedido después de emitir un prepago.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 44, 48, 42, 50, 52, 9305, 9307
ms.date: 06/16/2021
ms.author: edupont
ms.openlocfilehash: 45bc013c983e4c58d2c4b54dfa074c2170165652
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/19/2022
ms.locfileid: "9529682"
---
# <a name="correct-prepayments"></a>Corregir prepagos

Puede corregir un pedido después de haber registrado una factura de prepago para el mismo. Puede agregar nuevas líneas a un pedido después de emitir un prepago y, a continuación, registrar otra factura de prepago, pero no puede eliminar una línea de un pedido una vez que se haya facturado un prepago para la línea.  

> [!TIP]
> Si ha publicado una factura de prepago para una factura de ventas que luego corrige o cancela, también debe corregir o cancelar el prepago.

## <a name="to-correct-a-prepayment"></a>Para corregir un prepago

El procedimiento siguiente muestra cómo emitir una abono de prepago para cancelar todos los pagos adelantados facturados para un pedido de venta.  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Pedidos de venta** y, a continuación, elija el vínculo relacionado.  
2. Abra el pedido de venta correspondiente.
3. Elija la acción **Prepago** y **Registrar abono prepago** o **Registrar e imprimir abono prepago**.  
4. En la página **Abono venta**, corrija los movimientos correspondientes, en función de cualquier abono de venta. Para obtener más información, vea [Procesar devoluciones de ventas o cancelaciones](sales-how-process-sales-returns-cancellations.md).  

    > [!NOTE]  
    > Para reducir la cantidad del campo **Importe de línea**, antes debe aumentar el porcentaje de prepago de la línea, para que el valor del campo **Importe línea prepago** no se reduzca por debajo del valor del campo **Importe prepago facturado**.

5. Para crear una factura prepago para las nuevas líneas en el abono de ventas, elija las acciones **Prepago** y **Registrar factura prepago** o **Registrar e imprimir factura prepago**.  
6. Para emitir una factura de prepago adicional, aumente la cantidad de prepago de una o varias líneas y registre la factura de prepago. Se creará una nueva factura con la diferencia entre las cantidades de prepago facturadas y las nuevas cantidades de prepago.  

## <a name="see-related-microsoft-training"></a>Consultar la [formación de Microsoft](/training/modules/prepayment-invoices-dynamics-365-business-central/) relacionada

## <a name="see-also"></a>Consulte también .

[Facturación de prepagos](finance-invoice-prepayments.md)  
[Tutorial: configuración y facturación de prepagos de ventas](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[Finanzas](finance.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
