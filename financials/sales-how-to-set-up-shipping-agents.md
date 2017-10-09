---
title: Configurar transportistas | Documentos de Microsoft
description: "Configure un código para cada uno de sus transportistas e introduzca información acerca de ellos."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/23/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 84a5d9eb8757dc82834c17327ffbb510cd15fa1a
ms.contentlocale: es-es
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-shipping-agents"></a>Cómo configurar transportistas
Configure un código para cada uno de sus transportistas e introduzca información acerca de ellos.  

Si introduce una dirección de Internet para el transportista, y éste ofrece servicios de seguimiento de paquetes a través de Internet, utilice la función de seguimiento automático de paquetes. Para obtener más información, vea [Procedimiento: realizar seguimiento de paquetes](sales-how-track-packages.md).

Cuando configura transportistas en los pedidos de venta, también puede especificar los servicios que cada uno ofrece.  
Puede configurar un número ilimitado de servicios para cada transportista y especificar un tiempo de envío para cada servicio.  

Una vez asignado un servicio de transportista a una línea de pedido de venta, el tiempo de envío del servicio se incluirá en el cálculo del compromiso de entrega de dicha línea. Para obtener más información, consulte [Procedimiento: cálculo de las fechas de compromiso de entrega de pedido](sales-how-to-calculate-order-promising-dates.md).

## <a name="to-set-up-a-shipping-agent"></a>Para configurar un transportista  
1.  Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Transportistas** y, a continuación, seleccione el vínculo relacionado.  
2.  Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].  
3.  Elija la acción **Servicios transportista**.
4. En **Servicios transportista**, rellene los campos según sea necesario.

> [!NOTE]  
>  Si elimina el transportista de la línea de pedido, también se eliminará el código de servicio de transportista. Se volverá a calcular el contenido de los campos basados en parte en el servicio de transportista.  

## <a name="see-also"></a>Consulte también
[Cómo hacer el seguimiento de los paquetes](sales-how-track-packages.md)    
[Gestión almacén](warehouse-manage-warehouse.md)  
[Grupos contables inventario](inventory-manage-inventory.md)  
[Configuración de la gestión del almacén](warehouse-setup-warehouse.md)     
[Gestión de ensamblaje](assembly-assemble-items.md)    
[Detalles de diseño: Gestión de almacén](design-details-warehouse-management.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

