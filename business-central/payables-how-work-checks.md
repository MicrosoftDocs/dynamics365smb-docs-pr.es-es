---
title: Emitir, imprimir, cancelar y anular cheques
description: Describe cómo emitir cheques con el diario de pagos, imprimir cheques y anular o ver movimientos de cheques en Business Central.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment journal, print check, vendor payment, creditor, debt, balance due, AP
ms.search.form: 256, 404,
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 24e12472ea02f91ff3a0a8d23295865ca2855ca5
ms.sourcegitcommit: e008b3d7003c256475d6c606e5f7c9866a6bbb72
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/10/2022
ms.locfileid: "7953008"
---
# <a name="make-check-payments"></a>Realizar pagos por cheque

Puede emitir cheques electrónicos y manuales en [!INCLUDE[prod_short](includes/prod_short.md)]. Ambos métodos utilizan el diario de pagos para emitir los cheques a proveedores. También puede anular cheques y ver movimientos de cheques.

El siguiente procedimiento muestra cómo pagar a un proveedor con cheques por ordenador, mediante la liquidación del pago a la factura del proveedor relevante, la impresión del cheque y la contabilización del pago como pagado. Esto da como resultado entradas positivas en la contabilidad del proveedor, aplicadas a las entradas negativas y a los cheques físicos para el procesamiento en el banco.

Puede pagar con dos tipos de cheques. Para ambos tipos, el campo **Tipo contrapartida** o **Tipo de cuenta** debe contener **Cuenta bancaria**.

- **Cheque automático**: Seleccione esta opción si desea imprimir un cheque por el importe de la línea del diario de pagos. Debe imprimir los cheques antes de que pueda registrar las líneas del diario.
- **Cheque manual**: Seleccione esta opción si ha creado manualmente un cheque y desea crear el movimiento de cheque correspondiente a ese importe. Usando esta opción no puede imprimir el cheque.

> [!NOTE]  
> Para asegurarse de que su banco solo compensa cheques e importes validados, puede enviarles un archivo que contenga la información de proveedor, cheque y pago. Para obtener más información, vea [Exportar un archivo de Positive Pay](finance-how-positive-pay.md).

> [!IMPORTANT]
> Su impresora tiene que haber configurado correctamente los documentos y usted deberá definir qué plantilla de cheques va a usar. Para obtener más información , vea [Seleccionar una plantilla de cheques](finance-how-define-check-layouts.md). Alternativamente, puede enviar el cheque como un archivo PDF, por ejemplo.  

Puede imprimir hasta 10 facturas en una página para una matriz de cheque. Si un cheque se aplica a más de 10 facturas, cuando imprima el talón anularemos el cheque en la primera página e imprimiremos la palabra ANULADO en el cheque. A continuación, imprimimos el resto de las facturas y el importe total del cheque en la segunda página.

## <a name="to-pay-a-vendor-invoice-with-a-computer-check"></a>Para pagar una factura de proveedor con un cheque automático
A continuación se describe cómo pagar a un proveedor mediante un cheque. Los pasos son similares al reembolso de un cheque.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Diarios de pagos** y luego elija el enlace relacionado.
2. Rellene las líneas del diario de pagos. Para obtener más información, vea [Registre pagos y reembolsos](payables-how-post-payments-refunds.md).
3. En el campo **Cód. forma pago**, seleccione **Cheque**.
4. En el campo **Tipo pago por banco**, seleccione **Cheque automático**.
5. Seleccione la acción **Imprimir cheque**.
6. En la página **Cheque**, rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
7. Si su impresora está configurada para imprimir cheques, elija el botón **Imprimir**. De lo contrario, seleccione el botón **Enviar a**, seleccione la opción **Documento PDF** y, a continuación, el botón **Aceptar** y después imprima el documento PDF.

    Los cheques físicos ahora se pueden enviar a los proveedores para que los procesen. Proceda a publicar el pago tal como se le aplica al proveedor y, por lo tanto, pagado en el sistema.
8. Seleccione la acción **Registrar**.

Se crean los movimientos de contabilidad de proveedores y de cuenta bancaria totalmente aplicados.

> [!NOTE]  
> Si quiere imprimir y pagar cheques en varias divisas de cuentas bancarias distintas, deberá ejecutar el proceso **Imprimir cheque** por separado para cada divisa y especificar la cuenta bancaria correspondiente.

## <a name="to-cancel-printed-checks-that-are-not-posted"></a>Para anular los cheques imprimidos que no han sido registrados
Puede anular los cheques no registrados después de que hayan sido imprimidos usando la acción **Anular cheque** de la página **Diario de pagos**.

1. En la página **Diario de pagos**, seleccione **Anular cheque** y, a continuación, seleccione qué cheques desea cancelar.

## <a name="to-void-checks"></a>Para anular cheques

Cuando se ha registrado el pago del cheque, solo puede cancelar (anular) cheques en los movimientos resultantes del banco.

> [!IMPORTANT]
> Si el cheque se aplica a una factura, anule la aplicación del cheque primero para que la factura se pueda pagar y luego anule el cheque. Si el cheque se imprimió y no pagó una factura, elija **Solo cheque nulo** como se describe en esta sección.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Cuentas bancarias** y luego elija el enlace relacionado.
2. Seleccione la cuenta bancaria correspondiente, seleccione la acción **Editar** y, a continuación, seleccione la acción **Movs. cheques**.
3. En la página **Movs. cheques**, seleccione la acción **Anular cheque**.
4. Seleccione la casilla **Anular cheque solo**.
5. Elija el botón **Aceptar**.

## <a name="to-view-a-summary-of-posted-checks"></a>Para ver un resumen de los cheques registrados
Si desea revisar los cheques registrados, por ejemplo, para verificar los cheques múltiples pagados a un proveedor, puede usar el informe **Bancos - Desglose cheques**.
1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Banco - Desglose cheques** y luego elija el enlace relacionado.
2. Establezca los filtros como relevantes y luego elija el botón **Vista previa**.

## <a name="see-also"></a>Consulte también
[Creación de pagos](payables-make-payments.md)  
[Administrar pagos](payables-manage-payables.md)  
[Configurar banca](bank-setup-banking.md)  
[Exportar un archivo de Positive Pay](finance-how-positive-pay.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]