---
title: Emitir, imprimir, cancelar y anular cheques | Documentos de Microsoft
description: "Describe cómo emitir cheques con el diario de pagos, imprimir cheques y anular o ver movimientos de cheques en Dynamics 365."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment journal, print check, vendor payment, creditor, debt, balance due, AP
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: 85e5cd61571ec6e571a44e39f397bd370112dd5c
ms.contentlocale: es-es
ms.lasthandoff: 11/10/2017

---
# <a name="how-to-work-with-checks"></a>Procedimiento: Trabajar con cheques
Puede emitir cheques electrónicos y manuales en [!INCLUDE[d365fin](includes/d365fin_md.md)]. Ambos métodos utilizan el diario de pagos para emitir los cheques a proveedores. También puede anular cheques y ver movimientos de cheques.

El proceso de emisión de cheques propone pagos, crea movimientos e imprime los cheques automáticos.

> [!NOTE]  
>   Para asegurarse de que su banco solo compensa cheques e importes validados, puede enviarles un archivo que contenga la información de proveedor, cheque y pago. Para obtener más información, vea [Exportar un archivo de Positive Pay](finance-how-positive-pay.md).

Su impresora tiene que haber configurado correctamente los documentos y usted deberá definir qué plantilla de cheques va a usar. Para obtener más información , vea [Procedimiento: Definir plantillas de cheques](finance-how-define-check-layouts.md)

## <a name="to-issue-checks"></a>Para emitir cheques
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Diarios de pagos** y, a continuación, seleccione el vínculo relacionado.
2. Rellene el diario con los pagos relevantes, por ejemplo, mediante la función Proponer pagos a proveedores. Para obtener más información, vea [Procedimiento: Proponer pagos a proveedores](payables-how-suggest-vendor-payments.md).
3. En el campo **Tipo de pago bancario** en las líneas de diario para el pago que desea realizar mediante cheques, seleccione una de las opciones siguientes:

   * **Cheque automático**: Seleccione esta opción si desea imprimir un cheque por el importe de la línea del diario de pagos. Debe imprimir los cheques antes de que pueda registrar las líneas del diario. solo puede seleccionar **Cheque automático** si el valor de **Tipo contrapartida** o el de **Tipo mov.** es **Cuenta banco**.
   * **Cheque manual**: Seleccione esta opción si ha creado manualmente un cheque y desea crear el movimiento de cheque correspondiente a ese importe. Usando esta opción no puede imprimir cheques de [!INCLUDE[d365fin](includes/d365fin_md.md)]. solo puede seleccionar **Cheque manual** si el valor de **Tipo contrapartida** o el de **Tipo mov.** es **Cuenta banco**.

     > [!NOTE]  
>   Debe imprimir los cheques automáticos antes de registrar las líneas del diario relacionadas.
4. En el caso de los cheques automáticos, seleccione **Imprimir cheque**.
5. En la ventana **Cheque**, rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
6. Elija el botón **Imprimir**.

> [!NOTE]  
>   Si desea imprimir cheques en varias divisas de distintas cuentas bancarias, deberá ejecutar el trabajo por lotes **Imprimir cheque** por separado para cada divisa y especificar la cuenta bancaria correspondiente.

## <a name="to-cancel-printed-checks-that-are-not-posted"></a>Para anular los cheques imprimidos que no han sido registrados
Puede anular los cheques no registrados después de que hayan sido imprimidos usando la acción **Anular cheque** de la ventana **Diario de pagos**.

1. En la ventana **Diario de pagos**, seleccione **Anular cheque** y, a continuación, seleccione que cheques desea cancelar.

## <a name="to-void-checks"></a>Para anular cheques
Cuando se ha registrado el pago del cheque, solo puede cancelar (anular) cheques en los movimientos resultantes del banco.

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Cuentas bancarias** y, a continuación, seleccione el vínculo relacionado.
2. Seleccione la cuenta bancaria correspondiente, seleccione la acción **Editar** y, a continuación, seleccione la acción **Movs. cheques**.
3. En la ventana **Movs. cheques**, seleccione la acción **Anular cheque**.
4. Seleccione la casilla **Anular cheque solo**.
5. Elija el botón **Aceptar**.

## <a name="see-also"></a>Consulte también
[Administrar pagos](payables-manage-payables.md)  
[Configurar banca](bank-setup-banking.md)  
[Exportar un archivo de Positive Pay](finance-how-positive-pay.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

