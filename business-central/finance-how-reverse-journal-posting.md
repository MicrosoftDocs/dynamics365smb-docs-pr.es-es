---
title: Deshacer un registro registrando el movimiento de reversión | Documentos de Microsoft
description: Si ha realizado un registro erróneo en el diario general, puede utilizar la función Revertir transacción para deshacer el registro con un seguimiento de auditoria correcto.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reimbursement
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: cdbf4b682b4ad99524ea0aace9a123283668fb43
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2021
ms.locfileid: "5779102"
---
# <a name="reverse-journal-postings-and-undo-receiptsshipments"></a>Revertir los registros de diario y deshacer los recibos/envíos
Para deshacer un registro erróneo del diario, seleccione un movimiento y cree un movimiento de reversión (movimientos idénticos al original, pero con el signo contrario en el campo de importe) con el mismo número de documento y la misma fecha de registro que el movimiento original. Después de revertir un movimiento, debe registrar el movimiento correcto.

Solo se pueden revertir los movimientos que están registrados desde una línea del diario general. Un movimiento solo se puede revertir una vez.

Para deshacer un registro de albarán o de envío, antes de que se registre como facturado, puede usar la función **Deshacer** en el documento registrado. Puede deshacer cantidades de tipo **Artículo** y **Recurso**.

Si ha realizado un registro de una cantidad negativa errónea, como un pedido de compra con un número de productos erróneo y lo ha registrado como recibido, pero no facturado, puede deshacer el registro.

Si ha realizado un registro de una cantidad positiva errónea, como un albarán de venta o un envío de devolución de compra con un número de productos erróneo y lo ha registrado como enviado, pero no facturado, puede deshacer el registro.   

## <a name="to-reverse-the-journal-posting-of-a-general-ledger-entry"></a>Para revertir el registro de diario de un movimiento de contabilidad
Se pueden revertir movimientos desde todas las páginas **Movimientos**. El siguiente procedimiento se basa en la página **Movs. contabilidad**.
1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), introduzca **Movs. contabilidad** y luego elija el enlace relacionado.
2. Seleccione el movimiento que desea revertir y, después, seleccione **Revertir transacción**. Tenga en cuenta que debe proceder de un registro de diario.
3. En la página **Revertir movs. trans.**, elija la acción **Revertir**.
4. Elija el botón **Sí** en el mensaje de confirmación.

> [!NOTE]
> No pueden revertir los movimientos que se han registrado con información de un trabajo, o que han obtenido ganancias y pérdidas dentro de la misma transacción.

## <a name="to-post-a-negative-entry"></a>Para registrar un movimiento negativo  
Puede utilizar el campo **Corrección** para enviar un adeudo negativo en lugar de un abono, o registrar un crédito negativo en vez de un débito en una cuenta. Para cumplir los requisitos legales, este campo estará visible de forma predeterminada en todos los diarios. Los campos **Importe debe** e **Importe haber** incluyen tanto el movimiento original como el corregido. Estos campos no influyen en el saldo de la cuenta.  

1.  Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), introduzca **Diarios generales** y luego elija el enlace relacionado  
2.  En el campo **Nombre sección**, seleccione el nombre de sección requerido.  
3.  Escriba información en los campos relevantes.  
4.  En la línea del diario que desea activar para los movimientos negativos, seleccione la casilla de activación **Corrección**.  
5.  Para registrar el diario, elija la acción **Registrar** y el botón **Sí**.

## <a name="to-undo-a-quantity-posting-on-a-posted-purchase-receipt"></a>Para deshacer la cantidad registrada en un albarán de compra registrado  
A continuación se describe cómo deshacer un albarán registrado de artículos o recursos. Los pasos son parecidos para los envíos registrados.

1.  Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), introduzca **Albaranes de compra registrados** y luego elija el enlace relacionado.  
2.  Abra la recepción registrada que desea deshacer.  
3.  Selecciones las líneas del diario que desea deshacer.  
4.  Seleccione la acción **Deshacer albarán**.

Una línea correctiva se inserta bajo la línea de recepción seleccionada. Si se recibe la cantidad en un albarán de almacén, entonces se inserta una línea de corrección en la recepción de almacén registrado.  

Los campos de **Cantidad recibida** y de **Cdad. Rec. no facturada** en el pedido de compra relacionado se establecerán a cero.

## <a name="to-undo-and-then-redo-a-quantity-posting-on-a-posted-return-shipment"></a>Deshacer y rehacer una cantidad registrada en un envío devuelto registrado
A continuación se describe cómo deshacer un envío de devolución de artículos o recursos registrado y luego volver a registrar la devolución de la compra con una nueva cantidad. Los pasos son parecidos para las recepciones de devolución registradas.

1.  Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), introduzca **Registro de envíos de devolución** y luego elija el enlace relacionado.  
2.  Abra el envío devolución registrado que desea deshacer.
3. Selecciones las líneas del diario que desea deshacer.  

4.  Elija la acción **Deshacer envío dev.**.  

    Se insertará una línea de corrección en el documento registrado y los campos **Cantidad dev. enviada** y **Dev. enviadas no facturadas** del pedido de devolución se establecerán en cero.  

    Ahora vuelva al pedido de devolución de compra para volver a realizar el registro.  

5.  En la página **Histórico envío devolución**, tome una nota del número en el campo **Nº devolución** .  
6.  Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), introduzca **Devolución de pedidos** y luego elija el enlace relacionado.  
7.  Abra el pedido de devolución en cuestión y, a continuación, elija la acción **Volver a abrir**.  
8.  Corrija el movimiento en el campo **Cantidad** y vuelva a publicar la orden de devolución de la compra.  

## <a name="see-also"></a>Consulte también
[Deshacer registro de ensamblado](assembly-how-to-undo-assembly-posting.md)  
[Registrar transacciones directamente en la contabilidad](finance-how-post-transactions-directly.md)  
[Trabajar con diarios generales](ui-work-general-journals.md)  
[Finanzas](finance.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]