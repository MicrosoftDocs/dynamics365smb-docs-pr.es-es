---
title: Configurar códigos para servicios estándar | Documentos de Microsoft
description: Aprenda a configurar códigos para las actividades de servicio que realiza a menudo.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: service, service item, service order, repairs, maintenance
ms.date: 06/22/2020
ms.author: edupont
ms.openlocfilehash: 32699c3c509a9d3516d43d9fb76948460b75d41f
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "3784639"
---
# <a name="set-up-standard-service-codes"></a>Configurar códigos de servicio estándar

Cuando se realiza un servicio habitual, a menudo es necesario crear documentos de servicio que utilicen líneas de servicio que contengan información similar. Para facilitar la creación de estas líneas, puede configurar códigos de servicio estándar que tengan un conjunto predefinido de líneas de servicio. Cuando elige el código en un documento de servicio, las líneas se introducen automáticamente. Puede configurar números de códigos de servicio estándar, y cada código puede tener un número ilimitado de líneas de servicio de diferentes tipos, incluidas artículo, recurso, coste o texto estándar. Cree líneas de servicio de cada código de servicio estándar en la ficha **Ficha código servicio estándar**. Puede asignar códigos de servicio estándar a los grupos de producto de servicio en la página **Códs. grupo prod. serv. est.** Más adelante, cuando cree un documento de servicio, podrá ejecutar la función **Obtener cód. servicio estánd.** para añadir líneas de servicio.  
  
> [!Tip]
> Puede utilizar el mismo concepto para crear líneas de ventas y documentos de compra. Para obtener más información, vea [Crear líneas de ventas y de compras periódicas](sales-how-work-standard-lines.md).  
  
## <a name="to-set-up-a-standard-service-code"></a>Para configurar un código de servicio estándar

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Códigos servicio estándar** y luego elija el enlace relacionado.  
2. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Rellene las líneas de servicio vinculadas a este código de servicio.  

## <a name="to-assign-a-standard-service-code-to-a-service-item-group"></a>Para asignar un código de servicio estándar a un grupo de productos de servicio

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Grupos productos servicio** y luego elija el enlace relacionado.  
2. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Rellene las líneas de servicio vinculadas a este código de servicio.  

## <a name="see-also"></a>Consulte también

[Gestión de servicios](service-service.md)