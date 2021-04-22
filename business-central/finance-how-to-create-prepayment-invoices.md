---
title: Cómo crear facturas de prepago | Documentos de Microsoft
description: Conocer el modo de gestionar las situaciones en las que requiere prepago, o lo requiere el proveedor.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 72a073fcde9ddf20df7c138ab544afb6719b93ce
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2021
ms.locfileid: "5782168"
---
# <a name="create-prepayment-invoices"></a>Crear facturas de prepagos

Si requiere que sus clientes envíen el pago antes de enviarles un pedido, puede usar la funcionalidad de prepago. Lo mismo se aplica si su proveedor requiere que envíe el pago antes de enviarle un pedido.  

Puede iniciar el proceso de prepago cuando cree un pedido de venta o de compra. Si tiene un porcentaje de prepago predeterminado para este cliente o proveedor, se incluirá automáticamente en la factura de prepago resultante. También puede especificar un porcentaje de prepago para todo el documento.

Después de crear un pedido de venta o de compra, puede crear una factura de prepago. Para ello, puede utilizar los porcentajes predeterminados de cada línea de venta o de compra o bien ajustar el importe según sea necesario. Por ejemplo, puede especificar un importe total para todo el pedido.  

El procedimiento siguiente describe cómo facturar un prepago del pedido de venta. Los pasos son parecidos para pedidos de compra.  

## <a name="to-create-a-prepayment-invoice"></a>Para crear una factura de prepago

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Pedidos de venta** y luego elija el enlace relacionado.  
2. Cree un pedido de venta nuevo para un cliente relevante. Para obtener más información, vea [Vender productos](sales-how-sell-products.md).  

    En la ficha desplegable **Prepago**, el campo **% de prepago** especifica el porcentaje que se utilizará para calcular el importe de prepago. Si existe un porcentaje de prepago predeterminado en la ficha del cliente, el campo se rellenará automáticamente. Puede cambiar el porcentaje. <!--This percentage is applied to lines where the item on that line does not already specify a prepayment percentage. The prepayment percentage is only copied from the header to lines that do not copy the default prepayment percentage from the item.-->  

    Elija el campo **Compreión prepago** si desea crear líneas en la factura de prepago que combinen líneas del pedido de cliente si:  

    - Tienen la misma cuenta para los prepagos, tal y como lo haya determinado en la configuración de grupos contables.  
    - Tienen las mismas dimensiones.  

    Si desea especificar una factura de prepago con una línea para cada línea de pedido de venta que tenga un porcentaje de prepago, después, no elija el campo **Compresión prepago**.  

    La fecha de vencimiento del prepago se calcula automáticamente en función del valor de **Código términos prepago**.

3. Rellene las líneas de venta.  

    Si ha especificado un porcentaje de prepago predeterminado para el cliente o en la ficha desplegalbe **Prepago** en este documento, este valor se copia en cada línea. Puede cambiar el contenido del campo **% de prepago** en la línea.  

4. Para ver el importe de prepago total, elija la acción **Estadísticas**.

    Si desea ajustar el importe de prepago total para el pedido, puede cambiar los contenidos del campo **Importe prepago** en la página **Estad. pedido ventas**.  

    Si se selecciona el campo **Precios IVA incluido**, el campo **Cantidad prepago incl. IVA** se puede modificar.  

    Si cambia el contenido del campo **Cantidad prepago**, la cantidad se distribuirá proporcionalmente entre todas las líneas, excepto aquellas cuyo valor es **0** en el campo **% de prepago**.  

5. Para imprimir un test antes de registrar la factura de prepago, elija las acciones **Prepago** e **Informe test prepago**.  
6. Para registrar una factura de prepago, elija las acciones **Prepago** y **Registrar factura prepago**.  

    Para registrar e imprimir la factura de prepago, seleccione la acción **Registrar e imprimir factura prepago**.  

Puede emitir facturas de prepago adicionales para el pedido. Para ello, aumente la cantidad de prepago de una o varias líneas, ajuste la fecha del documento si es necesario y registre la factura de prepago. Se creará una nueva factura con la diferencia entre las cantidades de prepago facturadas hasta el momento y la nueva cantidad de prepago.  

> [!NOTE]  
> Si se encuentra en América del Norte, no puede cambiar el porcentaje de prepago después de que se haya contabilizado la factura de prepago. Esto se evita en la versión americana de [!INCLUDE[prod_short](includes/prod_short.md)] porque el cálculo del impuesto sobre las ventas, de otra manera, sería incorrecto.  

 Cuando esté listo para registrar el resto de la factura, hágalo del mismo modo que lo haría con cualquier otra factura; la cantidad de prepago se descontará automáticamente del importe vencido.  

## <a name="see-also"></a>Consulte también

[Facturación de prepagos](finance-invoice-prepayments.md)  
[Tutorial: Configuración y facturación de prepagos de ventas](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[Finanzas](finance.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]