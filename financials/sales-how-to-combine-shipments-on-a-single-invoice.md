---
title: "Procedimiento: agrupamiento de envíos en una factura única | Documentos de Microsoft"
description: "Si desea facturar varios envíos a la vez, utilice la función de agrupación de envíos."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/14/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: c9f2464014f2078f2a86f2e7d8a72873fa4015a8
ms.contentlocale: es-es
ms.lasthandoff: 01/30/2018

---
# <a name="combine-shipments-on-a-single-invoice"></a>Agrupar envíos en una factura única
Si desea facturar varios envíos a la vez, utilice la función de agrupación de envíos.  

 Para crear una agrupación de envíos, primero debe registrar más de un envío de venta para el mismo cliente en la misma divisa. Dicho de otro modo, debe haber rellenado dos o más pedidos de venta y haberlos registrado como enviados pero no facturados. Para agrupar envíos deberá activar la casilla de verificación **Fact. automática** de la ficha desplegable **Envíos** de la ficha del **Cliente**.  

## <a name="to-manually-combine-shipments-on-a-single-invoice"></a>Para agrupar envíos de forma manual en una factura única  
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Facturas venta** y, a continuación, seleccione el vínculo relacionado.  
2. Seleccione la acción **Nuevo**. Para obtener más información, vea [Facturar ventas](sales-how-invoice-sales.md).
3. En el campo **Venta a-N.º cliente**, introduzca el cliente que recibirá la factura de los productos enviados.  
4. En la ficha desplegable **Líneas**, elija la acción **Traer líns. recep**.  
5. Seleccione la línea del envío que desee incluir en la factura:  

    - Para insertar todas las líneas, selecciónelas y haga clic en **Aceptar**.  
    - Para insertar líneas concretas, selecciónelas y haga clic en **Aceptar**. Puede utilizar la tecla Ctrl para seleccionar varias líneas no secuenciales.  

    Si se ha seleccionado una línea de envío incorrecta o desea volver a empezar, sólo tiene que eliminar las líneas de la factura y volver a ejecutar la función **Traer líneas alb. venta**.  
7. Para registrar la factura, elija la acción **Registrar**.  

## <a name="to-automatically-combine-shipments-on-a-single-invoice"></a>Para agrupar envíos de forma automática en una factura única  
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Fact. automática...** y, a continuación, seleccione el vínculo relacionado. Se abre la ventana de solicitud de trabajo por lotes.  
2. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Seleccione la casilla de verificación **Registrar facturas**.  
4.  Elija el botón **Aceptar**.  

> [!NOTE]  
>  Deberá registrar las facturas manualmente si no se ha activado la casilla de verificación **Registrar facturas** en el trabajo por lotes.  

## <a name="to-remove-open-sales-orders-after-combined-shipment-posting"></a>Eliminar pedidos de venta abiertos después del registro de envío combinado 
Cuando se agrupan envíos en una factura y se registran, se crea una factura de venta registrada para las líneas facturadas. El campo **Cantidad facturada** del pedido de venta o pedido abierto de venta de origen se actualiza en función de la cantidad facturada.  

Al facturar envíos de esta forma, los pedidos a partir de los cuales se registraron los envíos siguen existiendo, aunque se hayan enviado y facturado por completo.   

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Eliminar ped. venta fact...** y, a continuación, seleccione el vínculo relacionado.  
2. Especifique en el campo de filtro **Nº.** que pedidos de venta desea eliminar.  
3. Elija el botón **Aceptar**.  

También puede eliminar los pedidos de venta individuales manualmente.  

Repita las tareas 1 a 3 para cualquier otro documento asignado, como pedidos abiertos de ventas.

## <a name="see-also"></a>Consulte también  
[Ccial](sales-manage-sales.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

