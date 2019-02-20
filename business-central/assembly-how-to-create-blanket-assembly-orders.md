---
title: "Cómo crear pedido de ensamblado abierto | Documentos de Microsoft"
description: "Si el campo **Sistema reposición** en la ficha del artículo contiene **Montaje**, el método predeterminado para suministrar el artículo será ensamblarlo desde los componentes definidos y potencialmente por un recurso definido."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: kit, kitting
ms.date: 12/20/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 5801fcc1284edfe1b8578518c084455c336d5a40
ms.openlocfilehash: 8796ccf6ce73ded327fad35573a2268e249fb7a7
ms.contentlocale: es-es
ms.lasthandoff: 12/27/2018

---
# <a name="create-blanket-assembly-orders"></a>Crear pedidos abiertos ensamblados
Puede utilizar la administración de ensamblados para personalizar un artículo del ensamblado a la solicitud de un cliente durante el proceso de venta. Para obtener más información, consulte [Venta de artículos ensamblados para pedido](assembly-how-to-sell-items-assembled-to-order.md).  

 Como para cualquier otro tipo de artículo, también puede crear pedidos abiertos de venta para los artículos de ensamblado personalizados antes de realizar el pedido de ventas real según el acuerdo del pedido abierto. Este proceso implica varios pasos adicionales cuando se compara con la creación de pedidos de ventas abiertos periódicos y utiliza una variación del pedido de ensamblado vinculado, que es un pedido de ensamblado abierto.

> [!NOTE]  
>  Al igual que todos los pedidos abiertos, las cantidades de los pedidos abiertos de ensamblado solo son previsiones y no están operativas hasta que se convierten en pedidos de ensamblado reales. Por tanto, la funcionalidad del pedido, como el cálculo de disponibilidad, la reserva y el seguimiento de artículos no están activos en los pedidos de ensamblado abiertos.  

## <a name="to-create-a-blanket-assembly-order-for-an-assemble-to-order-item"></a>Crear un pedido de ensamblado abierto para un artículo de ensamblado para pedido  
1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Pedidos de venta abiertos** y luego elija el enlace relacionado.  
2. Cree un nuevo pedido de ventas abierto con una línea para un artículo de ensamblado. Consulte [Crear pedidos abiertos de venta](sales-how-to-create-blanket-sales-orders.md) para obtener más información.  
3. En el campo **Cantidad a ensamblar para pedido** en la línea del pedido de ensamblado abierto, escriba la cantidad total.

    > [!NOTE]  
    >  No debe crear los acuerdos de pedido abierto para una cantidad parcial. Por tanto, deberá especificar la misma cantidad que haya especificado en el campo **Cantidad** de la línea de pedido de ventas abierto.  

4. Elija la acción **Ensamblar para pedido** y, a continuación, **Ensamblar para líneas de pedido**. También puede elegir el campo **Cdad. al ensamblar para pedido** en la línea.  
5. En la página **Líneas de ensamblado para pedido**, revise o modifique las líneas de pedido de ensamblado de acuerdo con el acuerdo de pedido abierto que haya suscrito con el cliente. Si desea ver más información, seleccione la acción **Mostrar documento** para abrir el pedido de ensamblado abierto completo. No puede modificar el contenido de la mayoría de los campos, y no puede realizar ningún registro.  
6. Cuando se hayan ajustado las líneas del pedido de ensamblado según el acuerdo de pedido abierto, cierre la página **Líneas de ensamblado para pedido** para volver a la página **Pedido abierto de ventas**.  
7. Cuando el cliente solicita crear un pedido de venta basado en el pedido de ventas abierto acordado, crea un pedido de venta para los artículos de ensamblado acordados. Consulte [Crear pedidos abiertos de venta](sales-how-to-create-blanket-sales-orders.md) para obtener más información.

El pedido de ensamblado abierto vinculado y las personalizaciones se vinculan a ese nuevo pedido de ventas para preparar el ensamblado de los artículos que se van a vender.  

## <a name="see-also"></a>Consulte también
[Crear pedidos abiertos de ventas](sales-how-to-create-blanket-sales-orders.md)  
[Gestión de ensamblaje](assembly-assemble-items.md)  
[Trabajar con listas de materiales](inventory-how-work-BOMs.md)  
[Grupos contables inventario](inventory-manage-inventory.md)  
[Detalles de diseño: Gestión de almacén](design-details-warehouse-management.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

