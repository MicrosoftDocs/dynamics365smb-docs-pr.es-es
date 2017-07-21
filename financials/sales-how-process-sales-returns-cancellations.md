---
title: Usar un abono de venta para procesar devoluciones o cancelaciones de ventas | Documentos de Microsoft
description: "Describe cómo crear un abono de ventas para procesar una devolución, una cancelación o un reembolso de productos o servicios de los que ha recibido el pago."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: undo, credit memo, return
ms.date: 06/21/2016
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: f08526054e99f742cedfefe036d8903304e54a56
ms.contentlocale: es-es
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-process-sales-returns-or-cancellations"></a>Procesamiento de devoluciones de ventas o cancelaciones
Si un cliente desea devolver u obtener un reembolso de algún producto o servicio que usted ha vendido y que le han pagado, debe crear y registrar una abono de ventas que especifique el cambio requerido. Para incluir la información correcta de la factura de venta, puede crear el abono de venta de la factura de venta registrada o usar una función de copia.  

> [!NOTE]  
>   Si una factura de venta registrada aún no se ha pagado, puede usar las funciones **Corregir** o **Cancelar** en la factura de venta registrada para revertir las transacciones. Estas funciones solo funcionan para las facturas sin pagar y no admiten devoluciones o cancelaciones parciales. Para obtener más información, vea [Procedimiento: Corregir o cancelar las facturas de venta sin abonar](sales-how-correct-cancel-sales-invoice.md)

Además de la original factura de venta registrada, puede liquidar el abono de venta a otros documentos de venta, por ejemplo otra factura de venta registrada, porque el cliente también devuelve los productos entregados con dicha factura.

Una devolución o reembolso se puede relacionar con solo algunos de los productos o servicios de la factura de venta original. En ese caso, debe editar la información de las líneas del abono de venta. Cuando se registra el abono de venta, se revierten los documentos de venta que se ven afectados por el cambio y se puede crear un pago de devolución para el cliente.  

Puede enviar el abono de venta registrado al cliente para confirmar la devolución o cancelación y comunicar que el valor relacionado se reembolsará, por ejemplo, cuando se devuelven los productos.

El registro del abono también revertirá cualquier coste de producto que se hubiera asignado al documento registrado, de forma que los movimientos de valor del producto son los mismos de antes que se asignara el cargo de producto.

## <a name="to-create-a-sales-credit-memo-from-a-posted-sales-invoice"></a>Para crear un nuevo abono de venta desde una factura de venta registrada.
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Facturas de ventas registradas** y, a continuación, elija el vínculo relacionado.  
2. En la ventana **Facturas de venta registradas**, seleccione la factura de ventas que desea revertir y, a continuación, seleccione la acción **Crear abono correctivo**.

    La cabecera del abono de venta contiene información de la factura de venta registrada. Puede modificarla, por ejemplo, mediante la nueva información que indica el contrato de devolución.  
3. Edite la información de las líneas según el contrato, como por ejemplo el número de productos devueltos o el importe que se reembolsará.
4. Seleccione la acción **Liquidar movs.**.
5. En la ventana **Liquidar movimientos cliente**, seleccione la línea con el documento de ventas registrado al que desee liquidar el abono de ventas y, a continuación, seleccione la acción **Liq. por id.**.

    El identificador del abono de ventas se muestra en el campo **Liq. por id**.
6. En la línea del campo **Importe a liquidar**, introduzca el importe que desea liquidar si es menor que el importe original.  

    En la parte inferior de la ventana **Liq. movs. cliente**, puede observar el importe total a liquidar para revertir todos los movimientos correspondientes, concretamente cuando el valor en el campo **Balanza** es cero.
7. Elija el botón **Aceptar**. Cuando registra el abono de venta, este se aplica a los documentos de venta registrados.

    Después de crear o editar las líneas de abono de venta y especificar una o varias aplicaciones, puede registrar el abono de venta.   
8. Seleccione la acción **Registrar y enviar**.  

El cuadro de diálogo de **Registrar y enviar confirmación** se abre para mostrar el método de envío preferido para el cliente. Puede cambiar el método de envío seleccionando el botón de búsqueda en el campo **Enviar documento a**. Para obtener más información, vea [Procedimiento: Configurar los perfiles de envío de documentos](sales-how-setup-document-send-profiles.md).  

Los documentos de venta registrados a los que ha aplicado el abono están invertidas y se puede crear un pago del reembolso para el cliente. El abono de venta se ha eliminado y remplazado por un nuevo documento de la lista de abonos de venta registrados.

## <a name="to-create-a-sales-credit-memo-from-scratch"></a>Para crear un abono de ventas desde cero
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Abonos de venta** y, a continuación, seleccione el vínculo relacionado.
2. Seleccione la acción **Nuevo** para abrir un abono de ventas vacío.
3. En el campo **Cliente**, escriba el nombre de un cliente existente.
4. Elija la acción **Copiar documento**.
5. En la ventana **Copiar documento de ventas**, en el campo **Tipo de documento**, seleccione el campo **Factura registrada**
6. Seleccione el **N.º documento**. para abrir la ventana **Facturas de venta registradas** y, a continuación, seleccione la factura de ventas registrada que contiene las líneas que desea revertir.
7. Seleccione la casilla **Recalcular líneas** si desea que las líneas de factura de venta registradas copiadas se actualicen con los cambios en el precio y el coste unitario del producto desde que la factura fue registrada.
8. Elija el botón **Aceptar**. Las líneas de factura copiadas se insertarán en el abono de venta.
9. Complete el abono de venta como se explica en la sección "Para crear un abono de ventas de una factura de ventas registrada" en este tema.

## <a name="see-also"></a>Consulte también
[Ventas](sales-manage-sales.md)  
[Configuración de ventas](sales-setup-sales.md)  
[Enviar documentos por correo electrónico.](ui-how-send-documents-email.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

