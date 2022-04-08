---
title: 'Detalles de diseño: Desviación | Documentos de Microsoft'
description: La desviación se define como la diferencia entre el coste real y el coste estándar, tal como se describe en la fórmula siguiente.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/08/2021
ms.author: edupont
ms.openlocfilehash: db015f330a89a164b7636b4f44a265f528e9cc3f
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2022
ms.locfileid: "8513049"
---
# <a name="design-details-variance"></a>Detalles de diseño: Desviación
La desviación se define como la diferencia entre el coste real y el coste estándar, tal como se describe en la fórmula siguiente.  

 coste real – coste estándar = desviación  

 Si el coste real cambia, por ejemplo, porque se registra un cargo de producto en una fecha posterior, la desviación se actualizará según corresponda.  

> [!NOTE]  
>  La revalorización no afecta al cálculo de desviación, porque la revalorización solo modifica el valor de inventario.  

## <a name="example"></a>Ejemplo  
 En el ejemplo siguiente se ilustra cómo se calcula la desviación de los productos comprados. Se basa en el siguiente caso:  

1.  El usuario compra un producto por DL 90,00, pero el coste estándar es de 100,00 DL. Por consiguiente, la desviación de compra es 10,00 DL.  
2.  Se cargan 10,00 DL en la cuenta de la desviación de compras.  
3.  El usuario registra un cargo de producto de 20,00 DL. Por consiguiente, el coste real se aumenta a 110,00 DL, y el valor de desviación de compra se convierte en 10,00 DL.  
4.  Se adeudan 20,00 DL en la cuenta de la desviación de compras. Por consiguiente, la desviación neta de compra se convierte en 10,00 DL.  
5.  El usuario revaloriza el producto de 100,00 DL a DL 70,00. No afecta al cálculo de desviación, solo al valor de inventario.  

 En la tabla siguiente se muestran los movimientos de valoración resultantes.  

 ![Cálculo de desviación de compras.](media/design_details_inventory_costing_11_purchase_variance.png "Cálculo de desviación de compras")  

## <a name="determining-the-standard-cost"></a>Determinación del coste estándar  
 El coste estándar se usa al calcular la desviación y el importe para capitalizar. Como el coste estándar puede cambiarse con el tiempo debido al cálculo de actualización manual, para el cálculo de desviación necesita un punto en el tiempo en el que el coste estándar sea fijo. Este momento se produce cuando se factura la entrada de existencias. En el caso de productos fabricados o ensamblados, el punto en el que se determina el coste estándar es cuando se ajusta el coste.  

 En la tabla siguiente se muestra cómo se calculan diferentes partes de coste para productos fabricados y ensamblados al usar la función Calcular coste estándar.  

|Parte coste|Producto comprado|Producto fabricado/ensamblado|  
|----------------|--------------------|------------------------------|  
|**Coste estándar**||Coste material a un nivel + Coste capacidad a un nivel + Coste subcontrat. a un nivel + Costes gen. cap. a un nivel + Coste gen. fab. a un nivel|  
|**Coste material a un nivel**|Coste unitario|![Ecuación 1.](media/design_details_inventory_costing_11_equation_1.png "Ecuación 1")|  
|**Coste capacidad a un nivel**|No aplicable|![Ecuación 2.](media/design_details_inventory_costing_11_equation_2.png "Ecuación 2")|  
|**Coste subcontrat. a un nivel**|No aplicable|![Ecuación 3.](media/design_details_inventory_costing_11_equation_3.png "Ecuación 3")|  
|**Costes gen. cap. a un nivel**|No aplicable|![Ecuación 4.](media/design_details_inventory_costing_11_equation_4.png "Ecuación 4")|  
|**Coste gen. fab. a un nivel**|No aplicable|(Coste de material de un nivel + Coste de capacidad de un nivel + Coste subcontr. de un nivel) * Coste indirecto % /100 + Tasa costes generales|  
|**Coste material distribuido**|Coste unitario|![Ecuación 5.](media/design_details_inventory_costing_11_equation_5.png "Ecuación 5")|  
|**Coste capacidad distribuida**|No aplicable|![Ecuación 6.](media/design_details_inventory_costing_11_equation_6.png "Ecuación 6")|  
|**Coste subcontratado distrib.**|No aplicable|![Ecuación 7.](media/design_details_inventory_costing_11_equation_7.png "Ecuación 7")|  
|**Coste gen. capacidad distribuida**|No aplicable|![Ecuación 8.](media/design_details_inventory_costing_11_equation_8.png "Ecuación 8")|  
|**Costes gen. fabr. distrib.**|No aplicable|![Ecuación 9.](media/design_details_inventory_costing_11_equation_9.png "Ecuación 9")|  

## <a name="see-also"></a>Consulte también  
 [Detalles de diseño: Coste de inventario](design-details-inventory-costing.md)   
 [Detalles de diseño: métodos de coste](design-details-costing-methods.md) [Gestión de costes de inventario](finance-manage-inventory-costs.md)  
 [Finanzas](finance.md)  
 [Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]