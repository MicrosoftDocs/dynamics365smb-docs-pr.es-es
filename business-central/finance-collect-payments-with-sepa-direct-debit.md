---
title: Adeudo directo SEPA en Business Central | Documentos de Microsoft
description: "Puede cobrar los pagos directamente al banco del cliente según el formato SEPA."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 557d6411540cc778a8f6810e747d4113fccd8f4c
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="collecting-payments-with-sepa-direct-debit"></a>Cobro de pagos mediante adeudo directo SEPA
Con el consentimiento de sus clientes, puede cobrar los pagos directamente al banco del cliente según el formato SEPA.  

 En primer lugar, configure el formato de exportación del archivo de banco que indica a su banco que debe realizar un adeudo directo. A continuación, configure la forma de pago del cliente. Por último, establezca la orden de domiciliación de adeudo directo que refleja el acuerdo con el cliente para cobrar sus pagos en un período de acuerdo determinado.  

 Para indicar al banco que transfiera el importe de pago desde el banco del cliente al banco de su empresa, debe crear un movimiento de cobro por adeudo directo que contiene información acerca de los bancos, las facturas de venta afectadas y la orden de domiciliación de adeudo directo. Luego exporta un archivo XML que se basa en el movimiento de cobro y que se envía al banco para su procesamiento. Los pagos que el banco no pudo procesar los comunicará el usuario al banco y el usuario deberá rechazar manualmente los movimientos de pago por adeudo directo en cuestión.  

 Puede establecer códigos de venta estándar del cliente con la información de forma de pago y orden de domiciliación de adeudo directo. Puede utilizar el trabajo por lotes **Crear facturas clientes estándar** para generar varias facturas de venta con la información de domiciliación rellenada previamente. Esto puede realizarse manual o automáticamente, según la fecha de vencimiento del pago.  

 Cuando los pagos se procesan correctamente, según lo ha comunicado el banco, puede registrar los recibos de pago directamente desde la ventana **Movimientos de cobros por adeudo directo** o mover las líneas de pago en el diario en el que contabiliza los recibos de pago, como la ventana **Diario de recibos de efectivo**. Como alternativa, en función del proceso de administración de efectivo, puede esperar y simplemente aplicar los pagos como parte de la conciliación bancaria.  

> [!NOTE]  
>  Para cobrar los pagos mediante adeudo directo SEPA, la divisa de la factura de venta debe ser EURO.  

 En la tabla siguiente se indican una serie de tareas con vínculos a los temas que las describen.   

|**Para**|**Vea**|  
|------------|-------------|  
|Prepare los formatos de banco, las formas de pago y los acuerdos de cliente para el adeudo directo SEPA.|[Configuración de domiciliaciones de adeudo directo SEPA](finance-how-to-set-up-sepa-direct-debit.md)|  
|Indique a su banco para que transfiera los importes de pago de los bancos de los clientes a la cuenta de su empresa según la configuración de adeudo directo SEPA.|[Crear movimientos de domiciliación de adeudo directo SEPA y exportación a un archivo bancario](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md)|  
|Configure códigos de ventas estándar de cliente para las facturas de domiciliación y generar facturas de venta con información de domiciliación cuando las facturas que están pendientes de pago.|[Crear líneas de ventas y de compras periódicas](sales-how-work-standard-lines.md)|  
|Registre los pagos efectuados como adeudos directos SEPA.|[Registro de recibos de pagos de domiciliación de adeudo directo SEPA](finance-how-to-post-sepa-direct-debit-payment-receipts.md)|  

## <a name="see-also"></a>Consulte también  
[Administrar cobros](receivables-manage-receivables.md)

