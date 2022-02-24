---
title: Configurar transportistas | Documentos de Microsoft
description: Configure un código para cada uno de sus transportistas e introduzca información acerca de ellos.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: d6a4bac4d540a65cc164029b23b063c8c9dbc1fb
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/01/2020
ms.locfileid: "3192664"
---
# <a name="set-up-shipping-agents"></a>Configurar transportistas
Configure un código para cada uno de sus transportistas e introduzca información acerca de ellos.  

Si introduce una dirección de Internet para el transportista, y éste ofrece servicios de seguimiento de paquetes a través de Internet, utilice la función de seguimiento automático de paquetes. Para obtener más información, vea [Realizar seguimiento de paquetes](sales-how-track-packages.md).

Cuando configura transportistas en los pedidos de venta, también puede especificar los servicios que cada uno ofrece.  
Puede configurar un número ilimitado de servicios para cada transportista y especificar un tiempo de envío para cada servicio.  

Una vez asignado un servicio de transportista a una línea de pedido de venta, el tiempo de envío del servicio se incluirá en el cálculo del compromiso de entrega de dicha línea. Para obtener más información, consulte [Calcular las fechas de compromiso de entrega de pedido](sales-how-to-calculate-order-promising-dates.md).

## <a name="to-set-up-a-shipping-agent"></a>Para configurar un transportista  
1.  Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Transportistas** y luego elija el enlace relacionado.  
2.  Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].  
3.  Elija la acción **Servicios transportista**.
4. En **Servicios transportista**, rellene los campos según sea necesario.

> [!NOTE]  
>  Si elimina el transportista de la línea de pedido, también se eliminará el código de servicio de transportista. Se volverá a calcular el contenido de los campos basados en parte en el servicio de transportista.  

## <a name="see-also"></a>Consulte también
[Configuración de métodos de envío](sales-how-set-up-shipment-methods.md)  
[Hacer un seguimiento de los paquetes](sales-how-track-packages.md)    
[Gestión de almacenes](warehouse-manage-warehouse.md)  
[Inventario](inventory-manage-inventory.md)  
[Configuración de la gestión del almacén](warehouse-setup-warehouse.md)     
[Gestión de ensamblaje](assembly-assemble-items.md)    
[Detalles de diseño: Gestión de almacén](design-details-warehouse-management.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
