---
title: 'Detalles de diseño: Componentes de coste | Documentos de Microsoft'
description: Los componentes del coste son distintos tipos de costes que conforman el valor de una entrada o una salida de existencias.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 07/01/2017
ms.author: sgroespe
ms.openlocfilehash: 697c040915b5117dc7aa2140a63e57b60090cd20
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/29/2019
ms.locfileid: "1243216"
---
# <a name="design-details-cost-components"></a>Detalles de diseño: Componentes de coste
Los componentes del coste son distintos tipos de costes que conforman el valor de una entrada o una salida de existencias.  

 En la tabla siguiente se muestran los distintos componentes de coste y los componentes de coste subordinados de los que constan.  

|Componentes de coste|Componente de coste subordinado|Description|  
|--------------------|--------------------------------|---------------------------------------|  
|Coste directo|Coste unitario (precio de compra directo)|Coste que puede seguirse hasta un objeto de coste.|  
|Coste directo|Coste de flete (cargo de producto)|Coste que puede seguirse hasta un objeto de coste.|  
|Coste directo|Coste de seguro (cargo de producto)|Coste que puede seguirse hasta un objeto de coste.|  
|Coste indirecto||Coste que no puede seguirse hasta un objeto de coste.|  
|Desviación|Desviación compras|La diferencia entre los costes estándar y real, que solo se registra para productos que utilizan el método de valoración de existencias **Estándar**.|  
|Desviación|Desviac. material|La diferencia entre los costes estándar y real, que solo se registra para productos que utilizan el método de valoración de existencias **Estándar**.|  
|Desviación|Desviac. capacidad|La diferencia entre los costes estándar y real, que solo se registra para productos que utilizan el método de valoración de existencias **Estándar**.|  
|Desviación|Desviac. subcontratada|La diferencia entre los costes estándar y real, que solo se registra para productos que utilizan el método de valoración de existencias **Estándar**.|  
|Desviación|Desviación cost. gen. capdad.|La diferencia entre los costes estándar y real, que solo se registra para productos que utilizan el método de valoración de existencias **Estándar**.|  
|Desviación|Desviación coste gen. fab.|La diferencia entre los costes estándar y real, que solo se registra para productos que utilizan el método de valoración de existencias **Estándar**.|  
|Reevaluación||Una depreciación o apreciación del valor actual de las existencias.|  
|Redondeo||Valores residuales provocados por la forma en que se calcula la valoración de las salidas de existencias.|  

> [!NOTE]  
>  Los costes de flete y de seguro son cargos de producto que se pueden agregar a un coste de producto en cualquier momento. Al ejecutar el proceso **Valorar stock - movs. producto**, el valor de cualquier salida de existencias relacionada se actualiza según corresponda.  

## <a name="see-also"></a>Consulte también  
 [Detalles de diseño: Coste de inventario](design-details-inventory-costing.md)   
 [Detalles de diseño: Desviación](design-details-variance.md) [Gestión de costes de inventario](finance-manage-inventory-costs.md)  
 [Finanzas](finance.md)  
 [Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
