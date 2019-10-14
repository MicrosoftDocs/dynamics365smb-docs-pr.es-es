---
title: Administrar cuentas por pagar | Documentos de Microsoft
description: Resumen de cómo administra las cuentas por pagar (AP), incluidos los pagos de proveedor, acreedores, deuda y saldo vencido.
services: project-madeira
documentationcenter: ''
author: bholtorf
manager: edupont
editor: ''
ms.service: dynamics365-business-central
ms.workload: na
ms.tgt_pltfrm: na
ms.devlang: na
ms.topic: article
ms.search.keywords: vendor payment, creditor, debt, balance due, AP
ms.date: 10/01/2019
ms.author: bholtorf
redirect_url: finance-set-up-cost-accounting
ms.openlocfilehash: 36da19dbe011f3e26dc166955fb9c5f0decd3b94
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2019
ms.locfileid: "2305769"
---
# <a name="managing-payables"></a>Administración de pagos
[!INCLUDE[d365fin](includes/d365fin_md.md)] tiene lo que necesita para administrar eficazmente las cuentas de pagos.  

## <a name="payments"></a>Pagos
Resulta fácil asignar prioridades a los pagos, tener en cuenta las penalizaciones por pagos atrasados y controlar por pronto pago.

Puede registrar pagos en un diario general e imprimir cheques antes de que se registre el diario de pagos.

Puede liquidar pagos para cerrar facturas cuando registre el pago o después de registrar el pago. El **Método liquidación** especificado para el proveedor (en la **Ficha del proveedor**) determina si debe liquidar el pago manual o automáticamente. Siempre puede liquidar las transacciones manualmente. Sin embargo, si el método de liquidación para el proveedor es **Por antigüedad** y no especifica un documento que liquide el pago, este liquida el movimiento abierto más antiguo para el proveedor.

## <a name="suggest-vendor-payments"></a>Proponer pagos a proveedores
[!INCLUDE[d365fin](includes/d365fin_md.md)] puede sugerir distintos pagos a proveedores, como pagos que vencerán pronto o pagos en donde hay un descuento disponible. La propuesta de pago puede considerar un importe que se especifique como fondos disponibles para el pago y si se pueden aplicar descuentos por pronto pago.

## <a name="issue-checks"></a>Problemas con los cheques
[!INCLUDE[d365fin](includes/d365fin_md.md)] le permite emitir los cheques a los proveedores manual y electrónicamente. Ambos se realizan en la página **Diarios de pagos**, donde también puede anular cheques y ver movimientos de cheque.

## <a name="export-payments-to-a-bank-file"></a>Exportar pagos a un archivo bancario
Cuando esté listo para pagar a un proveedor desde la página **Diario de pagos**, puede exportar un archivo con la información de pago de las líneas del diario. Después, puede cargar el archivo al banco electrónico para procesar las transferencias de dinero.

Si no desea registrar una línea de diario de pagos para un pago exportado, por ejemplo porque se está esperando que el banco confirme la transacción, puede eliminar solo la línea del diario. Posteriormente, cuando cree una línea de diario de pagos para pagar el importe pendiente en la factura, el campo **Importe total exportado** muestra qué parte del importe del pago se ha exportado ya. También puede encontrar información detallada acerca del total exportado seleccionando el botón **Movimientos de reg. de transferencia de crédito**.

Si espera a registrar los pagos hasta que el banco confirme que ha procesado las transacciones, hay dos formas de evitar la reexportación accidental de pagos de los documentos pendientes:  

* En un diario de pagos con líneas de pago propuestas, puede ordenar tanto **Exportado a archivo de pagos** o **Importe total exportado** y después eliminar las propuestas de pago de las facturas pendientes para las que ya se han realizado los pagos y no desea realizar ninguno más.

    **Nota** Es posible que tenga que agregar dichas columnas a la lista. Para obtener más información, consulte [Personalizar el área de trabajo](ui-personalization-user.md).  
* En el proceso **Proponer pagos a proveedores**, donde se pueden especificar los pagos que se incluirán en el diario de pagos, también puede especificar que no se inserten las líneas de diario para pagos que ya se hayan exportado eligiendo la casilla **Omitir pagos exportados**.

## <a name="see-also"></a>Consulte también
[Formas de pago](finance-payment-methods.md)  
[Finanzas](finance.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
