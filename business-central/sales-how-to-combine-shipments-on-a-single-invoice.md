---
title: 'Procedimiento: agrupamiento de envíos en una factura única | Documentos de Microsoft'
description: Si desea facturar varios envíos a la vez, utilice la función de agrupación de envíos.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: f6ce4c0c304fc8255789ec91fb3a00ba78170d6d
ms.sourcegitcommit: 6078bc9b2b571248d779722ce4125f250e7a3922
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/07/2020
ms.locfileid: "3666927"
---
# <a name="combine-shipments-on-a-single-invoice"></a>Agrupar envíos en una factura única
Si desea facturar varios envíos a la vez, utilice la función de agrupación de envíos.  

Para crear una agrupación de envíos, primero debe registrar más de un envío de venta para el mismo cliente en la misma divisa. Dicho de otro modo, debe haber creado dos o más pedidos de venta y haberlos registrado como enviados pero no facturados. 

## <a name="to-manually-combine-shipments-on-a-single-invoice"></a>Para agrupar envíos de forma manual en una factura única  
1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Facturas venta** y luego elija el enlace relacionado.  
2. Seleccione la acción **Nuevo**. Para obtener más información, vea [Facturar ventas](sales-how-invoice-sales.md).
3. En el campo **Venta a-N.º cliente**, introduzca el cliente que recibirá la factura de los productos enviados.  
4. En la ficha desplegable **Líneas**, elija la acción **Traer líns. recep**.  
5. Seleccione la línea del envío que desee incluir en la factura:  

    - Para insertar todas las líneas, selecciónelas y haga clic en **Aceptar**.  
    - Para insertar líneas concretas, selecciónelas y haga clic en **Aceptar**. Puede utilizar la tecla Ctrl para seleccionar varias líneas no secuenciales.  

    Si se ha seleccionado una línea de envío incorrecta o desea volver a empezar, sólo tiene que eliminar las líneas de la factura y volver a ejecutar la función **Traer líneas alb. venta**.  
7. Para registrar la factura, elija la acción **Registrar**.  

## <a name="to-automatically-combine-shipments-on-a-single-invoice"></a>Para agrupar envíos de forma automática en una factura única  
[!INCLUDE[d365fin](includes/d365fin_md.md)] seleccionará solo pedidos de venta donde se elija **Combinar envíos**. 

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Fact. automática** y luego elija el enlace relacionado. Se abre la página de solicitud de trabajo por lotes.  
2. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Elija la casilla de verificación **Registrar facturas**.  
4. Elija el botón **Aceptar**.  

> [!NOTE]  
>  Deberá registrar las facturas manualmente si no se ha activado la casilla de verificación **Registrar facturas** en el trabajo por lotes.  

## <a name="to-remove-open-sales-orders-after-combined-shipment-posting"></a>Eliminar pedidos de venta abiertos después del registro de envío combinado 
Cuando se agrupan envíos en una factura y se registran, se crea una factura de venta registrada para las líneas facturadas. El campo **Cantidad facturada** del pedido de venta o pedido abierto de venta de origen se actualiza en función de la cantidad facturada.  

Al facturar envíos de esta forma, los pedidos a partir de los cuales se registraron los envíos siguen existiendo, aunque se hayan enviado y facturado por completo.   

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Eliminar ped. venta fact.** y luego seleccione el enlace.  
2. Especifique en el campo de filtro **Nº.** que pedidos de venta desea eliminar.  
3. Elija el botón **Aceptar**.  

También puede eliminar los pedidos de venta individuales manualmente.  

Repita las tareas 1 a 3 para cualquier otro documento asignado, como pedidos abiertos de ventas.

## <a name="see-also"></a>Consulte también  
[Ccial](sales-manage-sales.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
