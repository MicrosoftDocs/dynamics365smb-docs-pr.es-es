---
title: "Detalles de diseño: Redondeo | Documentos de Microsoft"
description: Los redondeos residuales se pueden producir cuando se valora el coste de una salida de existencias que se mide en una cantidad distinta a la de la entrada de existencias correspondiente. Cuando se ejecuta el proceso **Valorar stock - movs. producto**, se calculan los redondeos residuales para todas las valoraciones de existencias.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 231481ed9b8de81fb565e86e9b89c96434545cbf
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-rounding"></a>Detalles de diseño: Redondeo
Los redondeos residuales se pueden producir cuando se valora el coste de una salida de existencias que se mide en una cantidad distinta a la de la entrada de existencias correspondiente. Cuando se ejecuta el proceso **Valorar stock - movs. producto**, se calculan los redondeos residuales para todas las valoraciones de existencias.  

 Cuando se usa la valoración de existencias media, el redondeo residual se calcula y registra de forma acumulada y movimiento a movimiento.  

 Cuando se usa una valoración de existencias distinta de Media, el redondeo residual se calcula cuando se ha liquidado completamente la entrada de existencias, lo que sucede cuando la cantidad restante de la entrada de existencias es igual a cero. A continuación se crea una entrada independiente para la redondeo residual, y la fecha de registro en esta entrada de redondeo es la fecha de registro de la entrada del último valor facturado de la entrada de existencias.  

## <a name="example"></a>Ejemplo  
 En el ejemplo siguiente se ilustra cómo se tratan diferentes redondeos residuales para la valoración de existencias Media y de otro tipo, respectivamente. En ambos casos, se ha ejecutado el proceso **Valorar stock - movs. producto**.  

 En la tabla siguiente se muestran los movimientos de producto en los que se basa el ejemplo.  

|Fecha registro|Cantidad|Nº mov.|  
|------------------|--------------|---------------|  
|01-01-20|3|1|  
|01-02-20|-1|2|  
|01-03-20|-1|3|  
|01-04-20|-1|4|  

 Para un producto que emplee el método de coste Promedio, dicha residual de redondeo (1/300) se calcula con la primera disminución (movimiento número 2) y se transfiere al movimiento número 3.  Por tanto, el movimiento número 3 se valora en –3,34.  

 En la tabla siguiente se muestran los movimientos de valoración resultantes.  

|Fecha registro|Cantidad|Importe coste (Real)|Nº mov. producto|Nº mov.|  
|------------------|--------------|----------------------------|---------------------------|---------------|  
|01-01-20|3|10|1|1|  
|01-02-20|-1|-3,33|2|2|  
|01-03-20|-1|-3,34|3|3|  
|01-04-20|-1|-3,33|4|4|  

 Para un producto que emplee un método de coste diferente al de Promedio, la residual de redondeo (0,01) se calcula cuando la cantidad pendiente para que la entrada de existencias sea cero. El redondeo residual tiene un movimiento independiente (número 5).  

 En la tabla siguiente se muestran los movimientos de valoración resultantes.  

|Fecha registro|Cantidad|Importe coste (Real)|Nº mov. producto|Nº mov.|  
|------------------|--------------|----------------------------|---------------------------|---------------|  
|01-01-20|3|10|1|1|  
|01-02-20|-1|-3,33|2|2|  
|01-03-20|-1|-3,33|3|3|  
|01-04-20|-1|-3,33|4|4|  
|01-01-20|0|-0,01|1|5|  

## <a name="see-also"></a>Consulte también  
 [Detalles de diseño: Coste de inventario](design-details-inventory-costing.md)   
 [Detalles de diseño: Ajuste de coste](design-details-cost-adjustment.md)   
 [Detalles de diseño: métodos de coste](design-details-costing-methods.md) [Gestión de costes de inventario](finance-manage-inventory-costs.md)  
 [Finanzas](finance.md)  
 [Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

