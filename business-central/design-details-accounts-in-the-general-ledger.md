---
title: 'Detalles de diseño: cuentas de contabilidad | Documentos de Microsoft'
description: Para conciliar los movimientos de inventario y de capacidad con la contabilidad, los movimientos de valoración relacionas se registran en cuentas distintas en la contabilidad.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/08/2021
ms.author: edupont
ms.openlocfilehash: 41b94d44ba374ecbcad64a2b1da100fcf3e1a2ab
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/09/2021
ms.locfileid: "6215583"
---
# <a name="design-details-accounts-in-the-general-ledger"></a>Detalles de diseño: cuentas de contabilidad
Para conciliar los movimientos de inventario y de capacidad con la contabilidad, los movimientos de valoración relacionas se registran en cuentas distintas en la contabilidad. Para obtener más información, consulte [Detalles de diseño: Conciliación con contabilidad](design-details-reconciliation-with-the-general-ledger.md).  

## <a name="from-the-inventory-ledger"></a>Desde los movimientos de inventario  
En la tabla siguiente se muestra la relación entre diferentes tipos de movimientos de valoración de inventario así como las cuentas y las cuentas de contrapartida en contabilidad.  

|**Tipo mov. producto**|**Tipo movimiento valor**|**Tipo desviación**|**Coste previsto**|**Cuenta**|**Cuenta de contrapartida**|  
|--------------------------------|--------------------------|-----------------------|-----------------------|-----------------|---------------------------|  
|Compra|Coste directo||Sí|Inventario (provisional)|Cta. ajuste invent. (Provis.)|  
|Compra|Coste directo||N.º|Grupos contables inventario|Coste directo aplic.|  
|Compra|Coste indirecto||N.º|Grupos contables inventario|Cost. gen. liqd.|  
|Compra|Desviación|Compra|N.º|Grupos contables inventario|Desviación compras|  
|Compra|Reevaluación||N.º|Grupos contables inventario|Ajuste inventario|  
|Compra|Redondeo||N.º|Grupos contables inventario|Ajuste inventario|  
|Venta|Coste directo||Sí|Inventario (provisional)|Coste ventas (provisional)|  
|Venta|Coste directo||N.º|Grupos contables inventario|CV|  
|Venta|Reevaluación||N.º|Grupos contables inventario|Ajuste inventario|  
|Venta|Redondeo||N.º|Grupos contables inventario|Ajuste inventario|  
|Ajuste positivo, Ajuste negativo, Transferencia|Coste directo||N.º|Grupos contables inventario|Ajuste inventario|  
|Ajuste positivo, Ajuste negativo, Transferencia|Reevaluación||N.º|Grupos contables inventario|Ajuste inventario|  
|Ajuste positivo, Ajuste negativo, Transferencia|Redondeo||N.º|Grupos contables inventario|Ajuste inventario|  
|(Producción) Consumo|Coste directo||N.º|Grupos contables inventario|WIP|  
|(Producción) Consumo|Reevaluación||N.º|Grupos contables inventario|Ajuste inventario|  
|(Producción) Consumo|Redondeo||N.º|Grupos contables inventario|Ajuste inventario|  
|Consumo de ensamblado|Coste directo||N.º|Grupos contables inventario|Ajuste inventario|  
|Consumo de ensamblado|Coste directo||N.º|Coste directo aplic.|Ajuste inventario|  
|Consumo de ensamblado|Coste indirecto||N.º|Cost. gen. liqd.|Ajuste inventario|  
|(Producción) Salida|Coste directo||Sí|Inventario (provisional)|WIP|  
|(Producción) Salida|Coste directo||N.º|Grupos contables inventario|WIP|  
|(Producción) Salida|Coste indirecto||N.º|Grupos contables inventario|Cost. gen. liqd.|  
|(Producción) Salida|Desviación|Material|N.º|Grupos contables inventario|Desviac. material|  
|(Producción) Salida|Desviación|Capacidad|N.º|Grupos contables inventario|Desviac. capacidad|  
|(Producción) Salida|Desviación|Subcontratados|N.º|Grupos contables inventario|Desviac. subcontratada|  
|(Producción) Salida|Desviación|Cost. gen. capdad.|N.º|Grupos contables inventario|Desv. coste gen. cap|  
|(Producción) Salida|Desviación|Cost. gen. fabricación|N.º|Grupos contables inventario|Desv. coste gen. fab.|  
|(Producción) Salida|Reevaluación||N.º|Grupos contables inventario|Ajuste inventario|  
|(Producción) Salida|Redondeo||N.º|Grupos contables inventario|Ajuste inventario|  
|Salida de ensamblado|Coste directo||N.º|Grupos contables inventario|Ajuste inventario|  
|Salida de ensamblado|Reevaluación||N.º|Grupos contables inventario|Ajuste inventario|  
|Salida de ensamblado|Coste indirecto||N.º|Grupos contables inventario|Cost. gen. liqd.|  
|Salida de ensamblado|Desviación|Material|N.º|Grupos contables inventario|Desviac. material|  
|Salida de ensamblado|Desviación|Capacidad|N.º|Grupos contables inventario|Desviac. capacidad|  
|Salida de ensamblado|Desviación|Cost. gen. capdad.|N.º|Grupos contables inventario|Desv. coste gen. cap|  
|Salida de ensamblado|Desviación|Cost. gen. fabricación|N.º|Grupos contables inventario|Desv. coste gen. fab.|  
|Salida de ensamblado|Redondeo||N.º|Grupos contables inventario|Ajuste inventario|  

## <a name="from-the-capacity-ledger"></a>Desde los movimientos de capacidad  
 En la tabla siguiente se muestra la relación entre diferentes tipos de movimientos de valoración de capacidad así como las cuentas y las cuentas de contrapartida en contabilidad. Los movimientos de capacidad representan el tiempo de trabajo consumido en trabajos de ensamblado o de producción.  

|**Tipo trabajo**|**Tipo de movimiento de capacidad**|**Tipo mov. valor**|**Cuenta**|**Cuenta de contrapartida**|  
|-------------------|------------------------------------|--------------------------|-----------------|---------------------------|  
|Ensamblado|Recurso|Coste directo|Coste directo aplic.|Ajuste inventario|  
|Ensamblado|Recurso|Coste indirecto|Cost. gen. liqd.|Ajuste inventario|  
|Producción|Centro máquina/Centro trabajo|Coste directo|Cuenta WIP|Coste directo aplic.|  
|Producción|Centro máquina/Centro trabajo|Coste indirecto|Cuenta WIP|Cost. gen. liqd.|  

## <a name="assembly-costs-are-always-actual"></a>Los costes de ensamblado son siempre reales  
 Como se muestra en de la tabla anterior, los registros de ensamblado no aparecen representados en las cuentas provisionales. Esto se debe a que el concepto de trabajo en curso no se aplica al registro de la salida de ensamblado, a diferencia del registro de la salida de producción. Los costes de ensamblado se registran solo como coste real, nunca como coste previsto.  

 Para obtener más información, consulte [Detalles de diseño: Registro de pedidos de ensamblado](design-details-assembly-order-posting.md).  

## <a name="calculating-the-amount-to-post-to-the-general-ledger"></a>Cálculo del importe que registrar en la contabilidad  
 Los campos siguientes de la tabla **Movimiento valor** se usan para calcular el importe de coste previsto que se registra en contabilidad:  

-   Importe coste (real)  
-   Coste regis. en contab.  
-   Importe coste (Esperado)  
-   Coste esperado reg. en cont.  

En la tabla siguiente se muestra cómo se calculan los importes para registrar en contabilidad para los dos tipos de coste distintos.  

|Tipo coste|Cálculo|  
|---------------|-----------------|  
|Coste real|Importe coste (Real) - Imp. registrado contabilidad|  
|Coste previsto|Importe coste (previsto) – Coste esperado reg. en contabilidad|  

## <a name="see-also"></a>Consulte también  
 [Detalles de diseño: Coste de inventario](design-details-inventory-costing.md)   
 [Detalles de diseño: Registro de inventario](design-details-inventory-posting.md)   
 [Detalles de diseño: Registro de coste previsto](design-details-expected-cost-posting.md)  
 [Gestión de costes de inventario](finance-manage-inventory-costs.md)  
 [Finanzas](finance.md)  
 [Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]