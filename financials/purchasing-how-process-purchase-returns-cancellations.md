---
title: Proceso de devoluciones o cancelaciones de compras | Documentos de Microsoft
description: Procesamiento de devoluciones de compra o cancelaciones
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cancel, undo, correct
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: f87b51ac746c6586e4ebb3b09aaa8d5ee7ac391d
ms.contentlocale: es-es
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-process-purchase-returns-or-cancellations"></a>Procesamiento de devoluciones de compra o cancelaciones
Si desea devolver productos al proveedor o cancelar servicios comprados, puede crear y registrar un abono de compra que especifique el cambio solicitado en relación a la factura de compra original. Para incluir la información correcta de la factura de compra, puede crear el abono de compra de la factura de compra registrada o usar una función de copia.

**Nota**: Si una factura de compra registrada aún no se ha pagado, puede usar las funciones **Corregir** o **Cancelar** en la factura de compra registrada para revertir automáticamente las transacciones correspondientes. Estas funciones solo funcionan para las facturas sin pagar y no admiten devoluciones o cancelaciones parciales. Para obtener más información, vea [Procedimiento: Corregir o cancelar las facturas de compra sin abonar](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)

Normalmente, se crea un abono de compra como resultado de un abono enviado por un proveedor. El abono de compra funciona como la documentación interna del proceso de abono para fines contables.

El cambio puede relacionarse con todos los productos en la factura de compra original o solo algunos de los productos. Por consiguiente, puede devolver productos parcialmente recibidos o exigir un reembolso parcial de los servicios recibidos. En ese caso, debe modificar la información copiada de la factura de compra.

Además de la original factura de compra registrada, puede liquidar el abono de compra a otros documentos de compra, por ejemplo otra factura de compra registrada, porque usted también devuelve los productos entregados con dicha factura.

## <a name="to-create-a-purchase-credit-memo-from-a-posted-purchase-invoice"></a>Para crear un nuevo abono de compra desde una factura de compra registrada.
1. En la esquina superior derecha, seleccione el icono **Buscar página o informe** ![Buscar página o informe](media/ui-search/search_small.png "Icono Buscar página o informe"), especifique **Abonos de compra** y elija el vínculo relacionado.  
2. En la ventana **Facturas de compra registradas**, seleccione la factura de compra que desea revertir y, a continuación, seleccione la acción **Crear abono correctivo**.

    La mayoría de los campos de la cabecera de abono de compra se rellenan con la información de la factura de compra registrada. Puede modificar todos los campos, por ejemplo, mediante la nueva información que indica el contrato de devolución.
3. Edite la información de las líneas según el contrato, como por ejemplo el número de productos devueltos o el importe que se reembolsará.
4. Seleccione la acción **Liquidar movs.**.
5. En la ventana **Liquidar movimientos proveedor**, seleccione la línea con el documento de compra registrado al que desee liquidar el abono de compras y, a continuación, seleccione la acción **Liq. por id.**. El número del abono de compras se inserta en el campo **Liq. por id**.
6. En la línea del campo **Importe a liquidar**, introduzca el importe que desea liquidar si es menor que el importe original.

    En la parte inferior de la ventana **Liq. movs. proveedor**, puede observar el importe total a liquidar para revertir todos los movimientos correspondientes, concretamente cuando el valor en el campo **Balanza** es cero.
7. Elija el botón **Aceptar**. Cuando registra el abono de compra, este se aplicará a los documentos de compra registrados especificados.

    Cuando ha creado o editado las líneas de abono de compra necesarias y se han especificado una o varias aplicaciones, puede empezar a registrar el abono de compra.
8. Seleccione la acción **Registrar**.

Las facturas de compra registradas a las que se aplica el abono ahora están revertidas. Si ya ha pagado la factura original, el proveedor ahora deberá reembolsarle el pago a usted. Si el abono es solo para parte del producto en la factura original, puede pagar solo el importe pendiente en la factura de compra original para cerrarla.

El abono de compra se ha eliminado y remplazado por un nuevo documento de la lista de abonos de compra registrados.

## <a name="to-create-a-purchase-credit-memo-from-scratch"></a>Para crear un abono de compras desde cero
1. En la esquina superior derecha, seleccione el icono **Buscar página o informe** ![Buscar página o informe](media/ui-search/search_small.png "Icono Buscar página o informe"), especifique **Histórico facturas compra** y elija el vínculo relacionado.
2. Seleccione la acción **Nuevo** para abrir un abono de compras vacío.
3. En el campo **Proveedor**, escriba el nombre de un proveedor existente.
4. Elija la acción **Copiar documento**.
5. En la ventana **Copiar documento de compra**, en el campo **Tipo de documento**, seleccione el campo **Factura registrada**
6. Seleccione el **N.º documento**. para abrir la ventana **Facturas de compra registradas** y, a continuación, seleccione la factura de compra registrada que contiene las líneas que desea revertir.
7. Seleccione la casilla **Recalcular líneas** si desea que las líneas de factura de compra registradas copiadas se actualicen con los cambios en el precio y el coste unitario del producto desde que la factura fue registrada.
8. Elija el botón **Aceptar**. Las líneas de factura copiadas se insertarán en el abono de compra.
9. Complete el abono de compra como se explica en la sección "Para crear un abono de compra de una factura de compras registrada" en este tema.

## <a name="see-also"></a>Consulte también
[Compras](purchasing-manage-purchasing.md)  
[Registro de compras](purchasing-how-record-purchases.md)  
[Corregir o cancelar las facturas de compra sin abonar](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)](ui-work-product.md)

