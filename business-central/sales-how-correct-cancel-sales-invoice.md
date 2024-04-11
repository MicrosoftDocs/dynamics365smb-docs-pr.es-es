---
title: Corregir o cancelar una factura de venta registrada
description: 'Este artículo describe cómo corregir, deshacer o cancelar una factura de venta registrada y aplicar un abono de venta.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: ivkoleti
ms.topic: conceptual
ms.search.keywords: 'undo, credit memo, return'
ms.date: 03/05/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="correct-or-cancel-unpaid-sales-invoices"></a>Corregir o cancelar facturas de venta sin abonar

Puede corregir o cancelar una factura de venta registrada impaga, siempre que no se haya enviado por completo. Esto es útil si se comete un error o si el cliente solicita un cambio antes de que se complete el envío. En todos los demás escenarios, le recomendamos que cree directamente una nota de crédito de ventas correctiva. Para más información, vea [Para crear una nota de crédito de ventas a partir de una factura de ventas registrada](sales-how-process-sales-returns-cancellations.md#to-create-a-sales-credit-memo-from-a-posted-sales-invoice).  

> [!NOTE]  
> Una vez que una factura de venta registrada se haya pagado parcial o totalmente, no puede corregirla o cancelarla de la factura de venta registrada en sí. En su lugar, debe crear manualmente un abono de venta para anular la venta y reembolsar al cliente, opcionalmente administrada con una orden de devolución de venta. Para obtener más información, vea [Procesar devoluciones de ventas o cancelaciones](sales-how-process-sales-returns-cancellations.md).

La diferencia entre cancelar o corregir una factura de venta registrada que no se ha pagado o enviado se describe en la siguiente tabla.

| Acción | Descripción |
| --- | --- |
| **Cancelar** |La factura de venta registrada está cancelada. Un abono de venta de corrección se crea y se registra automáticamente para anular la factura de venta registrada inicial. En la factura de venta registrada inicial, están marcadas las casillas **Cancelado** y **Pagado**. |
| **Corregir** |La factura de venta registrada está cancelada. Se crea una nueva factura de venta con la misma información, a menos que la orden de venta registrada se haya registrado desde una orden de venta. En ese caso, le sugerimos que cancele la factura de venta registrada y luego haga la corrección y continúe el proceso de venta desde el pedido de venta original. <br/><br/>La nueva factura de venta tiene un número diferente que la factura de venta inicial. Un abono de venta de corrección se crea y se registra automáticamente para anular la factura de venta registrada inicial. En la factura de venta registrada inicial, están marcadas las casillas **Cancelado** y **Pagado**. |
|**Crear nota de abono correctiva**|Se crea una nueva nota de abono con la misma información. Puede ajustar la nueva nota de crédito de ventas antes de contabilizarla y se aplicará a la factura original cuando la contabilice. |

Al corregir o cancelar una factura de ventas registrada, el abono de venta de corrección se aplica a todos los movimientos contables y del inventario que se crearon cuando se registró la factura de venta inicial. De esta forma se invierte la factura de venta registrada en los registros financieros deja el abono de venta registrado de corrección para el seguimiento de auditoria.  

> [!TIP]
> Si ha publicado una factura de prepago para una factura de ventas que luego corrige o cancela, también debe corregir o cancelar el prepago. Para obtener más información, consulte [Corregir prepagos](finance-how-to-correct-prepayments.md).

## <a name="to-cancel-a-posted-sales-invoice"></a>Cancelar una factura de venta registrada

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Histórico facturas venta** y luego elija el enlace relacionado.  
2. Seleccione la factura de venta registrada que desea cancelar.

    > [!NOTE]  
    > Si se selecciona la casilla **Cancelado**, no puede cancelar la factura de venta registrada porque ya se ha cancelado o corregido.
3. En la página **Factura de ventas registrada**, elija la acción **Cancelar**.

    Un abono de venta se crea y se registra automáticamente para anular la factura de venta registrada inicial. El campo **Cancelado** en la factura de ventas registrada inicial se cambia a **Sí**.
4. Elija la acción **Mostrar abono correctivo** para ver el histórico de abonos de ventas que anula la factura de ventas registrada inicial.

### <a name="partial-invoice-posting-also-supported"></a>También se admite el registro parcial de facturas

Si la cancelación está relacionada con un registro parcial de la factura, la línea de pedido de venta original se actualiza para reflejar la cantidad facturada cancelada. Los campos **Cant. a facturar** y **Cant. facturada** en la línea de pedido de venta relacionada se restablecen a los valores previos del registro parcial.

## <a name="to-correct-a-posted-sales-invoice"></a>Corregir una factura de venta registrada

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Histórico facturas venta** y luego elija el enlace relacionado.  
2. Seleccione la factura de venta registrada que desea corregir.

    > [!NOTE]  
    >   Si se selecciona la casilla **Cancelado**, no puede corregir la factura de venta registrada porque ya se ha corregido o cancelado.
3. En la página **Factura de ventas registrada**, elija la acción **Corregir**.  

    > [!NOTE]
    > Si la factura de venta se registró desde un pedido de venta, le recomendamos que *cancelar* esta factura de venta y luego procese la corrección del pedido de venta original. Si se ha eliminado el pedido de cliente original, por ejemplo, si se ha enviado por completo, puede crear un nuevo pedido de cliente utilizando la acción **Copiar documento**. Para más información, vea [Para crear una nota de crédito de ventas copiando una factura de ventas registrada](sales-how-process-sales-returns-cancellations.md#to-create-a-sales-credit-memo-by-copying-a-posted-sales-invoice).
4. Una nueva factura de venta con la misma información se crea donde puede realizar la corrección. El campo **Cancelado** en la factura de ventas registrada inicial se cambia a **Sí**.

    Un abono de venta se crea y se registra automáticamente para anular la factura de venta registrada inicial.
5. Elija la acción **Mostrar abono correctivo** para ver el histórico de abonos de ventas que anula la factura de ventas registrada inicial.

## <a name="see-also"></a>Consulte también .

[Ventas](sales-manage-sales.md)  
[Configuración de ventas](sales-setup-sales.md)  
[Enviar documentos por correo electrónico](ui-how-send-documents-email.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
