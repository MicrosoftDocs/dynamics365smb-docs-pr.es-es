---
title: "Cómo combinar albaranes | Documentos de Microsoft"
description: "Si desea facturar varios albaranes de compra a la vez, puede utilizar la función Combinar albaranes."
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
ms.openlocfilehash: 2176baf2947a08785fdf6327b2ebebf35686d04a
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="combine-receipts-on-a-single-invoice"></a>Agrupar albaranes en una factura única
Si desea facturar varios albaranes de compra a la vez, puede utilizar la función **Combinar albaranes**.  

Para poder crear un albarán de compra combinado, es necesario haber registrado primero más de un albarán del mismo proveedor y en la misma divisa. En otras palabras, debe haber rellenado dos o más pedidos de compra, así como haberlos registrado como recibidos, pero no facturado.  

Cuando se combinan varios albaranes de compra en una factura y se registran, se crea una factura de compra registrada para las líneas facturadas. El campo **Cantidad facturada** del pedido de compra de origen, o del pedido abierto de compra, se actualiza en función de la cantidad facturada. Sin embargo, este documento de compra original no se elimina, aunque se haya recibido y facturado por completo, por lo que debe eliminar el documento de compra.  

## <a name="to-combine-receipts"></a>Para combinar albaranes  
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Facturas compra** y, a continuación, seleccione el vínculo relacionado.  
2. Seleccione la acción **Nuevo**. Para obtener más información, consulte [Registrar compras](purchasing-how-record-purchases.md).  
3. En la ficha desplegable Líneas, haga clic en **Acciones**, y elija la acción **Traer líns. recep**.  
4. Seleccione las distintas líneas de albarán que desee incluir en la factura.  

    Si se ha seleccionado una línea de albarán incorrecta o desea comenzar desde el principio, simplemente elimine las líneas de la factura de compra y vuelva a usar la función **Traer líns. recep**.  
5. Para registrar la factura, elija la acción **Registrar**.  

## <a name="to-remove-open-purchase-orders-after-combined-receipt-posting"></a>Procedimiento para eliminar pedidos de compra abiertos después del registro de recepción combinada  
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Eliminar peds. compra. factdos...** y, a continuación, seleccione el vínculo relacionado.  
2. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].
3. Elija el botón **Aceptar**.  

También puede eliminar los pedidos individuales manualmente.

Repita las tareas 1 a 3 para cualquier otro documento asignado, como pedidos abiertos de compra.

## <a name="see-also"></a>Consulte también  
[Compras](purchasing-manage-purchasing.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

