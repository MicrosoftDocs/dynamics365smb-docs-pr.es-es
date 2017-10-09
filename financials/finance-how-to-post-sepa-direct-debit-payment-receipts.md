---
title: Registrar pagos de adeudo directo SEPA | Documentos de Microsoft
description: "Cuando el banco procesa correctamente un cobro por adeudo directo, puede proceder con el registro de la recepción del pago para las facturas de venta implicadas."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 5beb5f6795bd7f4943a6ed9d8b691c05fc5ecb63
ms.contentlocale: es-es
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-post-sepa-direct-debit-payment-receipts"></a>Registro de recibos de pagos de domiciliación de adeudo directo SEPA
Cuando el banco procesa correctamente un cobro por adeudo directo, puede proceder con el registro de la recepción del pago para las facturas de venta implicadas. Para obtener más información, consulte [Creación de movimientos de domiciliación de adeudo directo SEPA y exportación a un archivo bancario](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md).  

Puede registrar el recibo de pago directamente desde la ventana **Cobros por adeudo directo** o la ventana **Movimientos de cobros por adeudo directo**. Como alternativa, puede delegar el trabajo a otro usuario mediante la preparación de las líneas de diario relacionadas.  

## <a name="to-post-a-direct-debit-payment-receipt-from-the-direct-debit-collections-window"></a>Registro de un recibo de pago de domiciliación desde la ventana Cobros por adeudo directo  
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Cobros por adeudo directo** y, a continuación, seleccione el vínculo relacionado.  
2. Seleccione una línea para un cobro por adeudo directo que se ha exportado a un archivo de banco y procesado correctamente por el banco. Para obtener más información, consulte [Creación de movimientos de domiciliación de adeudo directo SEPA y exportación a un archivo bancario](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md).  
3. Seleccione la acción **Registrar recibos de pago**.  
4. En la ventana **Registrar cobro por adeudo directo**, rellene los campos tal como se describe en la tabla siguiente.  

    |Campo|Description|  
    |---------------------------------|---------------------------------------|  
    |**Nº cobro por adeudo directo**|Especifique el cobro por adeudo directo para el que desea registrar el albarán de pago.|  
    |**Plantilla de libros diario general**|Especifique la plantilla de diario general que se debe usar para registrar el albarán de pago, tal como la plantilla de recibo de cobro.|  
    |**Nombre sección diario general**|Especifique qué sección del diario general se debe usar para registrar el albarán de pago.|  
    |**Crear solo diario**|Seleccione esta casilla si no desea registrar el recibo de pago al seleccionar el botón **Aceptar**. El recibo de pago se preparará en el diario especificado y no se registrará hasta que alguien registre las líneas de diario en cuestión.|  

5. Elija el botón **Aceptar**.  

## <a name="see-also"></a>Consulte también  
 [Cobrar pagos mediante adeudo directo SEPA](finance-collect-payments-with-sepa-direct-debit.md)   
 [Ccial](sales-manage-sales.md)

