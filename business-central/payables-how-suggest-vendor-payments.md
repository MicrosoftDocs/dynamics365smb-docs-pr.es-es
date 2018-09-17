---
title: Usar el proceso Proponer pagos a proveedores | Documentos de Microsoft
description: "Puede especificar la configuración de pago al proveedor para obtener sugerencias o propuestas de pagos que están a punto de vencer o en los que hay un descuento."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: vendor payment, creditor, debt, balance due, AP
ms.date: 05/15/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: ad1b888d475c0523c5a905e804a3f89ab4531b28
ms.openlocfilehash: 02f063daf5afeea85832c8a322183b3db120d8d2
ms.contentlocale: es-es
ms.lasthandoff: 05/17/2018

---
# <a name="suggest-vendor-payments"></a>Proponer pagos a proveedores
En la ventana **Diario de pagos** puede usar el proceso **Proponer pagos a proveedores** para sugerir líneas de pago. Las líneas como pagos que están a punto de vencer, o de pagos en los que hay disponible un descuento por pronto pago, se sugieren según la configuración.

Para obtener ventaja completa de las sugerencias de pago, primero debe asignar prioridades a los proveedores. Para obtener más información, consulte [Dar prioridad a proveedores](purchasing-how-prioritize-vendors.md).  

> [!NOTE]  
> Los movimientos de proveedor que están **En espera** no se incluyen en el trabajo por lotes.  

> [!IMPORTANT]  
>   Si desea aprovechar los descuentos por pronto pago y ha introducido un importe disponible, el importe se utilizará para:  
    * Movimientos de proveedor vencidos con prioridad, primero en orden de prioridad.   
    * Movimientos de proveedor vencidos que no tienen prioridad.  
    * Movimientos de proveedor pendientes que cumplen los requisitos para descuentos por pronto pago, organizados por número del proveedor.  

## <a name="to-use-the-suggest-vendor-payments-function"></a>Para usar la función Proponer pagos a proveedores
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Diarios de pagos** y, a continuación, seleccione el vínculo relacionado.  
2. Abra el diario pertinente y, a continuación, elija la acción **Proponer pagos a proveedor**.  
3. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. Elija el botón **Aceptar**.  

## <a name="to-insert-the-due-date-as-posting-date-on-payment-journal-lines"></a>Para insertar la fecha de vencimiento como fecha de registro en líneas de diario de pagos
Cuando use el proceso **Proponer pagos a proveedores** para crear las líneas de pago para los proveedores, puede rellenar dos campos especiales para asegurarse de que las líneas de planificación usan la fecha de vencimiento para calcular la fecha de registro. Estos campos son **Calcular fecha de registro a partir de fecha de vencimiento de documento de aplicación** y **Desfase fecha de vencimiento de documento de aplicación**.  

> [!IMPORTANT]  
>   No puede usar el campo **Calcular fecha de registro a partir de fecha de vencimiento de documento de aplicación** junto con el campo **Buscar dtos. P.P.** o el campo **Una línea por proveedor**. Si la fecha de registro se basa en la fecha de vencimiento, es posible que no se puedan calcular correctamente los descuentos por pronto pago, porque la fecha de registro es posterior a la fecha del descuento por pronto pago.  

Además, si la fecha de registro calculada está en el pasado, la fecha de registro se adelanta a la fecha de trabajo y aparece una advertencia.  

De forma alternativa, puede crear manualmente las líneas de pago con la fecha de vencimiento a fin de calcular la fecha de registro. Después de aplicar los movimientos de proveedor, puede utilizar la acción **Calcular fecha de registro** para actualizar la fecha de registro de la línea del diario con la fecha de vencimiento de la factura de compra relacionada. Para obtener más información, consulte [Liquidar transacciones de compra manualmente](payables-how-apply-purchase-transactions-manually.md).  

> [!NOTE]  
>   Si la factura de compra tiene fecha vencida, la fecha de registro se establece en la fecha de trabajo, y la fuente de la línea cambia a color rojo.  

## <a name="see-also"></a>Consulte también
[Administrar pagos](payables-manage-payables.md)  
[Creación de pagos](payables-make-payments.md)  
[Trabajar con diarios generales](ui-work-general-journals.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

