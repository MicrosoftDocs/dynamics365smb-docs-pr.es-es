---
title: Crear órdenes de producción desde pedidos de venta
description: Conozca las diferentes formas de crear órdenes de producción para productos producidos directamente a partir de órdenes de venta.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/22/2021
ms.author: edupont
ms.openlocfilehash: a432b8f00a24771578716a1b51678904d2e29ec5
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 07/08/2021
ms.locfileid: "6438632"
---
# <a name="create-production-orders-from-sales-orders"></a>Crear órdenes de producción desde pedidos de venta
Puede crear órdenes de producción para artículos producidos directamente desde los pedidos de venta.  

## <a name="to-create-a-production-order-from-a-sales-order"></a>Para crear una orden de producción desde un pedido de venta  

1.  Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Pedidos de venta** y, a continuación, elija el vínculo relacionado.  
2.  Seleccione el pedido de venta para el que desea crear una orden de producción.  
3.  Seleccione la acción **Planificación**. En la página **Planificación pedido venta**, puede consultar la disponibilidad de un producto incluido en un pedido de venta.  
4.  Seleccione la acción **Orden de producción**.  
5.  Seleccione el tipo del estado y orden.  
6.  Seleccione el botón **Sí** para crear una o más órdenes de producción para las líneas que tengan **Ord. prod.** en su campo **Sistema de reposición**.


> [!NOTE]  
> Las líneas de demanda en la orden de producción creada que disponen de **Prod. Pedido** en el campo de **Sistema reposición** representan las órdenes de producción subyacentes. Después de generar estas órdenes de producción, recuerde identificar la demanda de componentes no satisfecha utilizando la página **Planificación de pedidos** o la función **Replanificar** desde las órdenes creadas. 

## <a name="order-type"></a>Tipo orden  
Puede elegir entre dos formas de crear las órdenes de producción, como se describe en la siguiente tabla.

|Opción|Descripción|
|------|-----------|
|Orden producto|Se crea una orden de producción para cada orden de producción necesaria representada por una línea en la ventana **Planificación pedido venta**.|
|Orden proyecto|Se crea una orden de producción para todas las órdenes de producción necesarias representadas por líneas en la ventana **Planificación pedido venta**. |

Cuando utilice órdenes de proyecto, el campo **Tipo de procedencia** de la orden de producción contiene **Cabecera de ventas** y la orden tiene varias líneas, una para cada producto de línea de venta que debe fabricarse.  


## <a name="see-also"></a>Consulte también  
[Configuración de fabricación](production-configure-production-processes.md)  
[Fabricación](production-manage-manufacturing.md)    
[Inventario](inventory-manage-inventory.md)  
[Compras](purchasing-manage-purchasing.md)  
[Detalles de diseño: planificación de aprovisionamiento](design-details-supply-planning.md)   
[Procedimientos recomendados de configuración: planificación de suministros](setup-best-practices-supply-planning.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
