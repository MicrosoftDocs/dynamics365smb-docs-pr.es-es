---
title: "Cómo crear facturas de prepago | Documentos de Microsoft"
description: Conocer el modo de gestionar las situaciones en las que requiere prepago, o lo requiere el proveedor.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 50b77f4c6e333f3024f2261eb0c6df42b3e535d0
ms.contentlocale: es-es
ms.lasthandoff: 09/28/2018

---
# <a name="create-prepayment-invoices"></a>Crear facturas de prepagos
Si desea que sus clientes realicen el pago antes de enviarles un pedido o su proveedor le requiere que efectúe el pago antes de enviarle un pedido, puede utilizar la funcionalidad de prepago.  

Después de crear un pedido de venta o de compra, puede crear una factura de prepago. Para ello, puede utilizar los porcentajes predeterminados de cada línea de venta o de compra o bien ajustar el importe según sea necesario. Por ejemplo, puede especificar un importe total para todo el pedido.  

El procedimiento siguiente describe cómo facturar un prepago del pedido. Los pasos son parecidos para pedidos de compra.  

## <a name="to-create-a-prepayment-invoice"></a>Para crear una factura de prepago  
1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Pedidos de venta** y luego elija el enlace relacionado.  
2. Crear un nuevo pedido de venta. Para obtener más información, vea [Vender productos](sales-how-sell-products.md).  

    En la ficha desplegable **Prepago**, el campo **% prepago** de la cabecera se rellenará automáticamente si existe un porcentaje de prepago predeterminado en la ficha del cliente. Puede cambiar el contenido del campo. El porcentaje de prepago sólo se copia desde la cabecera en las líneas que no copian dicho porcentaje predeterminado del producto.  

    Si el campo **Compresión prepago** está seleccionado, las líneas se agruparán en la factura si:  
    - Tienen la misma cuenta para los prepagos, tal y como lo haya determinado en la configuración de grupos contables.  
    - Tienen las mismas dimensiones.  

    Deje el campo en blanco si desea especificar una factura de prepago con una línea para cada línea de pedido de venta que tenga un porcentaje de prepago.  

3. Rellene las líneas de venta.  

    Si se han definido porcentajes de prepago para los productos, se copian automáticamente en el campo **% de prepago** de la línea. De lo contrario, el porcentaje de prepago se copia de la cabecera. Puede cambiar el contenido del campo **% de prepago** en la línea.  
4. Si desea aplicar un porcentaje de prepago a todo el pedido, modifique el campo **% de prepago** en la cabecera después de rellenar las líneas.  
5. Para ver el importe de prepago total, elija la acción **Estadísticas**.

    Si desea ajustar el importe de prepago total para el pedido, puede cambiar los contenidos del campo **Importe prepago** en la ventana **Estad. pedido ventas**.  

    Si se selecciona el campo **Precios IVA incluido**, el campo **Cantidad prepago incl. IVA** se puede modificar.  

    Si cambia el contenido del campo **Cantidad prepago**, la cantidad se distribuirá proporcionalmente entre todas las líneas, excepto aquellas cuyo valor es **0** en el campo **% de prepago**.  
6. Para imprimir un test antes de registrar la factura de prepago, elija las acciones **Prepago** e **Informe test prepago**.  
7. Para registrar una factura de prepago, elija las acciones **Prepago** y **Registrar factura prepago**.  

    Para registrar e imprimir la factura de prepago, seleccione la acción **Registrar e imprimir factura prepago**.  

Puede emitir facturas de prepago adicionales para el pedido. Para ello, aumente la cantidad de prepago de una o varias líneas, ajuste la fecha del documento si es necesario y registre la factura de prepago. Se creará una nueva factura con la diferencia entre las cantidades de prepago facturadas hasta el momento y la nueva cantidad de prepago.  

> [!NOTE]  
>  Si se encuentra en América del Norte, no puede cambiar el porcentaje de prepago después de que se haya contabilizado la factura de prepago. Esto se evita en la versión americana de [!INCLUDE[d365fin](includes/d365fin_md.md)] porque el cálculo del impuesto sobre las ventas, de otra manera, sería incorrecto.  

 Cuando esté listo para registrar el resto de la factura, hágalo del mismo modo que lo haría con cualquier otra factura; la cantidad de prepago se descontará automáticamente del importe vencido.  

## <a name="see-also"></a>Consulte también  
[Facturación de prepagos](finance-invoice-prepayments.md)  
[Tutorial: Configuración y facturación de prepagos de ventas](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[Finanzas](finance.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

