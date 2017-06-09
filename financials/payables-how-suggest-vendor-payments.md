---
title: Sugerir pagos de proveedor | Documentos de Microsoft
description: Propuesta de pagos a proveedores
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: vendor payment, creditor, debt, balance due, AP
ms.date: 03/28/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 4b85fc783cdebb7c1d2e048315e48aee02a189fa
ms.contentlocale: es-es
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-suggest-vendor-payments"></a>Propuesta de pagos a proveedores
En la ventana **Diario de pagos** puede usar el proceso **Proponer pagos a proveedores** para sugerir líneas de pago. Las líneas de elementos como pagos que están a punto de vencer, o de pagos en los que hay disponible un descuento por pronto pago, se sugieren según la configuración.

Para obtener ventaja completa de las líneas sugeridas, primero debe asignar prioridades a los proveedores. Para obtener más información, consulte [Procedimiento: Dar prioridad a proveedores](purchasing-how-prioritize-vendors.md).  

No se incluyen los movimientos de proveedor no son del tipo **Esperar**.  

**Importante:** Si desea aprovechar los descuentos por pronto pago y ha introducido un importe disponible, el importe se utilizará para:  

* Movimientos de proveedor vencidos con prioridad, primero en orden de prioridad.  
* Movimientos de proveedor vencidos que no tienen prioridad.  
* Movimientos de proveedor pendientes que cumplen los requisitos para descuentos por pronto pago, organizados por número del proveedor.  

## <a name="to-use-the-suggest-vendor-payments-function"></a>Para usar la función Proponer pagos a proveedores
1. En la esquina superior derecha, seleccione el icono **Buscar página o informe** ![Buscar página o informe](media/ui-search/search_small.png "Icono Buscar página o informe"), especifique **Diarios de pagos** y elija el vínculo relacionado.  
2. Abra el diario pertinente y, a continuación, elija la acción **Proponer pagos a proveedor**.  
3. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. Elija el botón **Aceptar**.  

## <a name="to-insert-the-due-date-as-posting-date-on-payment-journal-lines"></a>Para insertar la fecha de vencimiento como fecha de registro en líneas de diario de pagos
Cuando use el proceso **Proponer pagos a proveedores** para crear las líneas de pago para los proveedores, puede rellenar dos campos especiales para asegurarse de que las líneas de planificación usan la fecha de vencimiento para calcular la fecha de registro. Estos campos son **Calcular fecha de registro a partir de fecha de vencimiento de documento de aplicación** y **Desfase fecha de vencimiento de documento de aplicación**.  

**Importante:** No puede usar el campo **Calcular fecha de registro a partir de fecha de vencimiento de documento de aplicación** junto con el campo **Buscar dtos. P.P.** o el campo **Una línea por proveedor**. Si la fecha de registro se basa en la fecha de vencimiento, es posible que no se puedan calcular correctamente los descuentos por pronto pago, porque la fecha de registro es posterior a la fecha del descuento por pronto pago.  

Además, si la fecha de registro calculada está en el pasado, la fecha de registro se adelanta a la fecha de trabajo y aparece una advertencia.  

De forma alternativa, puede crear manualmente las líneas de pago con la fecha de vencimiento a fin de calcular la fecha de registro. Después de aplicar los movimientos de proveedor, puede utilizar la acción **Calcular fecha de registro** para actualizar la fecha de registro de la línea del diario con la fecha de vencimiento de la factura de compra relacionada. Para obtener más información, consulte [Procedimiento: Liquidar transacciones de compra manualmente](payables-how-apply-purchase-transactions-manually.md).  

**Nota:** Si la factura de compra tiene fecha vencida, la fecha de registro se establece en la fecha de trabajo, y la fuente de la línea cambia a color rojo.  

## <a name="see-also"></a>Consulte también
[Administrar pagos](payables-manage-payables.md)  
[Realizar pagos](payables-make-payments.md)  
[Trabajar con diarios generales](ui-work-general-journals.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)](ui-work-product.md)  

