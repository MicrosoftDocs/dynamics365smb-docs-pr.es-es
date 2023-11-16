---
title: Trabajo por lotes de Propuesta de pagos a proveedores
description: Puede especificar la configuración de pago del proveedor para obtener sugerencias de pagos.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: conceptual
ms.search.keywords: 'vendor payment, creditor, debt, balance due, AP'
ms.search.form: '256,'
ms.date: 09/07/2023
ms.custom: bap-template
---
# <a name="suggest-vendor-payments"></a>Proponer pagos a proveedores

En la página **Diario de pagos** puede usar el proceso **Proponer pagos a proveedores** para sugerir líneas de pago. Según su configuración, [!INCLUDE [prod_short](includes/prod_short.md)] sugiere líneas de pagos:

* Pagos que vencen pronto
* Pagos donde hay un descuento de pago disponible

Para obtener ventaja completa de las sugerencias de pago, primero debe asignar prioridades a los proveedores. Para obtener más información sobre cómo priorizar proveedores, vaya a [Priorizar proveedores](purchasing-how-prioritize-vendors.md).  

> [!NOTE]  
> El trabajo por lotes excluye los asientos del libro mayor de proveedores que están **En espera** o que ya están aplicados y tienen un valor en el campo **Se aplica a la identificación**.  

> [!IMPORTANT]  
> Si desea aprovechar los descuentos por pronto pago y ha introducido un importe disponible, el importe se utilizará para:  
>
> * Movimientos de proveedor vencidos con prioridad, primero en orden de prioridad.
> * Movimientos de proveedor vencidos que no tienen prioridad.  
> * Movimientos de proveedor pendientes que cumplen los requisitos para descuentos por pronto pago. Las entradas están ordenadas por número de proveedor.  

## <a name="to-use-the-suggest-vendor-payments-function"></a>Para usar la función Proponer pagos a proveedores

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Diarios de pagos** y luego elija el enlace relacionado.  
2. Abra el diario y, a continuación, elija la acción **Proponer pagos a proveedor**.  
3. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. Elija el botón **Aceptar**.  

## <a name="to-insert-the-due-date-as-posting-date-on-payment-journal-lines"></a>Para insertar la fecha de vencimiento como fecha de registro en líneas de diario de pagos

Cuando use el proceso **Proponer pagos a proveedores** para crear las líneas de pago para los proveedores, puede rellenar dos campos especiales para asegurarse de que las líneas de planificación usan la fecha de vencimiento para calcular la fecha de registro. Estos campos son **Calcular fecha de registro a partir de fecha de vencimiento de documento de aplicación** y **Desfase fecha de vencimiento de documento de aplicación**.  

> [!IMPORTANT]  
> No puede usar el campo **Calcular fecha de registro a partir de fecha de vencimiento de documento de aplicación** junto con el campo **Buscar dtos. P.P.** o el campo **Una línea por proveedor**. Si la fecha de registro se basa en la fecha de vencimiento, es posible que no se podrían calcular correctamente los descuentos por pronto pago, porque la fecha de registro es posterior a la fecha del descuento por pronto pago.  

Además, si la fecha de registro calculada está en el pasado, la fecha de registro se adelanta a la fecha de trabajo y aparece una advertencia.  

También puede crear manualmente las líneas de pago con la fecha de vencimiento a fin de calcular la fecha de registro. Después de aplicar los movimientos de proveedor, puede utilizar la acción **Calcular fecha de registro** para actualizar la fecha de registro de la línea del diario con la fecha de vencimiento de la factura de compra relacionada. Para obtener más información sobre este proceso manual, vaya a [Aplicar transacciones de compra manualmente](payables-how-apply-purchase-transactions-manually.md).  

> [!NOTE]  
> Si la factura de compra tiene fecha vencida, la fecha de registro se establece en la fecha de trabajo, y la fuente de la línea cambia a color rojo.  

## <a name="see-also"></a>Consulte también .

[Administrar pagos](payables-manage-payables.md)  
[Creación de pagos](payables-make-payments.md)  
[Trabajar con diarios generales](ui-work-general-journals.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
