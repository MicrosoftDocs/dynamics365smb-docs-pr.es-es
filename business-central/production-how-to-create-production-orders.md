---
title: Como crear una cabecera de orden de producción | Documentos de Microsoft
description: Puede crear una orden de producción manualmente y el primer paso es crear la cabecera.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 683631572b7898ede3b7f1418f68a7ce95743ff8
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5380906"
---
# <a name="create-production-order-headers"></a>Crear cabeceras de orden de producción
Puede crear una orden de producción manualmente y el primer paso es crear la cabecera.

Las órdenes de producción normalmente se crean automáticamente por algunas tareas de planificación para cubrir una demanda conocida. Para obtener más información, consulte [Planificación](production-planning.md).   

En el siguiente procedimiento, se crea una orden de producción planificada en firme. Puede también crear órdenes de producción con estados distintos.  

## <a name="to-create-a-production-order-header"></a>Para crear la cabecera de una orden de producción  
1.  Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **O.P. Planificadas en firme** y luego elija el enlace relacionado.  
2.  Seleccione la acción **Nuevo**.  
3.  En el campo **N.º**, inserte el número siguiente de la serie.  
4.  En el campo **Tipo procedencia mov.**, seleccione la procedencia del movimiento de la orden de producción.

    Aquí puede seleccionar producir para una familia de productos. Para obtener más información, consulte [Trabajar con familias de producción](production-how-work-family.md).
5.  En el campo **Cód. procedencia mov.**, seleccione el código de producto, familia o cabecera de venta para el cual se va a generar la orden de producción.  
6.  Rellene los campos **Cantidad** y **Fecha vencimiento** según sus especificaciones.  

Cuando cambian las necesidades de producción, como componentes u operaciones, puede replantear rápidamente la orden de producción. Para obtener más información, vea [Actualizar o replanificar las órdenes de producción directamente](production-how-to-replan-refresh-production-orders.md). 

## <a name="see-also"></a>Consulte también  
[Fabricación](production-manage-manufacturing.md)    
[Configuración de fabricación](production-configure-production-processes.md)  
[Planificación](production-planning.md)      
[Inventario](inventory-manage-inventory.md)  
[Compras](purchasing-manage-purchasing.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]