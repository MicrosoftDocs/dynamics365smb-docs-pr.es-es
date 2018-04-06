---
title: "Cómo actualizar costes estándar | Documentos de Microsoft"
description: "Debe actualizar periódicamente los costes estándar de los componentes y distribuir los nuevos costes al producto principal."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/09/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 53716a78d7538e034c097506205a840b1243c4cf
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="update-standard-costs"></a>Actualizar costes estándar
Debe actualizar periódicamente los costes estándar de los componentes y distribuir los nuevos costes al producto principal. El proceso normalmente consiste en los cuatro pasos siguientes:  

1.  Actualizar los costes en los niveles de componente y de capacidad. Para obtener más información, consulte el proceso **Sugerir coste estándar prod.**.  
2.  Consolide y distribuya los costes de componentes y de capacidad para calcular el coste total de fabricación o ensamblado de los productos.  
3.  Implementar los costes estándar que se introducen al ejecutar los trabajos por lotes anteriores. Los costes estándar no tienen efecto hasta que se implementan. Para obtener más información, consulte Implementar cambios de coste estándar.  
4.  Implementar los cambios para actualizar el campo **Coste unitario** en la ficha del producto y realizar una revalorización de inventario. Para obtener más información, vea [Revaluación de inventario](inventory-how-revalue-inventory.md).  

Para obtener más información, consulte [Acerca de Calcular el coste estándar](finance-about-calculating-standard-cost.md).  
## <a name="to-update-standard-costs"></a>Para actualizar los costes estándar  
1.  Ejecute el proceso **Valorar stock - movs. producto**.  
2.  Ejecute el proceso **Regis. variación existencias**.  
3.  Abra la **Hoja trab. coste estándar** y use una o más de las funciones siguientes:  

    1.  Ejecute el proceso **Sugerir coste estándar prod.**  
    2.  Revise los resultados y realice los cambios que considere necesarios.  
    3.  Ejecute el proceso **Sugerir coste estándar capacidad**.  
    4.  Revise los resultados y realice los cambios que considere necesarios.
    5. Ejecute el proceso **Distribuir coste estándar**.
    6.  Revise los resultados y realice los cambios que considere necesarios.
    7.  Ejecute el proceso **Implementar cambios de coste estándar**.  
4.  Revise y registre la ventana **Diario revalorizac.**, la cual se ha rellenado con entradas provenientes de los pasos anteriores del proceso.  

## <a name="see-also"></a>Consulte también  
 [Acerca del cálculo de coste estándar](finance-about-calculating-standard-cost.md)   
 [Gestión de costes de inventario](finance-manage-inventory-costs.md)   
 [Detalles de diseño: Métodos de coste](design-details-costing-methods.md) [Finanzas](finance.md)  
 [Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

