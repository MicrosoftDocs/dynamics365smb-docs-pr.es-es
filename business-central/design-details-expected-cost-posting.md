---
title: 'Detalles de diseño: Advertencia registro coste esperado | Documentos de Microsoft'
description: Los costes previstos representan la estimación, por ejemplo, del coste de un producto comprado registrado antes de recibir la factura de este producto.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 8bb2c0af31fe2ffbac64b1cebd860356c124e881
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2021
ms.locfileid: "5777878"
---
# <a name="design-details-expected-cost-posting"></a>Detalles de diseño: Registro de coste previsto
Los costes previstos representan la estimación, por ejemplo, del coste de un producto comprado registrado antes de recibir la factura de este producto.  

 Puede registrar el coste previsto en el inventario y en la contabilidad. Cuando se registra una cantidad que solo se ha recibido o enviado, pero no se ha facturado, se crea un movimiento de valoración con el coste previsto. Este coste previsto afecta al valor de inventario, pero no se registra en la contabilidad a no ser que se haya configurado el sistema para tal fin.  

> [!NOTE]  
>  Los costes previstos solo se gestionan para transacciones de productos. Los costes previstos no son tipos de transacciones no materiales, como capacidad y cargos de productos.  

 Si solo se ha registrado la parte de la cantidad de una entrada de existencias, el valor de inventario en la contabilidad no cambia, a menos que haya seleccionado la casilla **Regis. cte. previsto en contab.** en la página **Configuración de inventario**. En ese caso, el coste previsto se registra en las cuentas provisionales en el momento de recepción. Tras haber facturado por completo el albarán, las cuentas provisionales se saldan y el coste real se registra en la cuenta de inventario.  

 Para respaldar el trabajo de conciliación y trazabilidad, el movimiento de valoración facturado muestra el importe del coste previsto que se ha registrado para cuadrar las cuentas provisionales.  

## <a name="example"></a>Ejemplo  
 En el ejemplo siguiente se muestra el coste previsto si las casillas **Variación existencias automát.** y **Regis. cte. previsto en contab.** se seleccionan en la página **Configuración de inventario**.  

 Registra un pedido de compra como recibido. El coste previsto es de 95,00 DL.  

 **Valor mov.**  

|Fecha registro|Tipo mov.|Importe coste (Esperado)|Coste esperado reg. en cont.|Coste previsto|Nº mov. producto|Nº mov.|  
|------------------|----------------|------------------------------|----------------------------------|-------------------|---------------------------|---------------|  
|01-01-20|Coste directo|95,00|95,00|Sí|1|1|  

 **Movimientos de relación en C/G: tabla Relación movs. productos**  

|Nº mov. contabilidad|Nº mov. valor|Nº asto. registro|  
|--------------------|---------------------|-----------------------|  
|1|1|1|  
|2|1|1|  

 **Movs. contabilidad**  

|Fecha registro|Cuenta|Nº cuenta (demostración En-US)|Importe|Nº mov.|  
|------------------|------------------|---------------------------------|------------|---------------|  
|01-01-20|Cuenta de ajuste de inventario (provisional)|5530|-95,00|2|  
|01-01-20|Cta. inventario (provisional)|2131|95,00|1|  

 En una fecha posterior, el pedido de compra se puede registrar como facturado. El coste facturado es de 100,00 DL.  

 **Valor mov.**  

|Fecha registro|Importe coste (Real)|Importe coste (Esperado)|Coste regis. en contab.|Coste previsto|Nº mov. producto|Nº mov.|  
|------------------|----------------------------|------------------------------|-------------------------|-------------------|---------------------------|---------------|  
|15-01-20|100.00|-95,00|100.00|No|1|2|  

 **Movimientos de relación en C/G: tabla Relación movs. productos**  

|Nº mov. contabilidad|Nº mov. valor|Nº asto. registro|  
|--------------------|---------------------|-----------------------|  
|3|2|2|  
|4|2|2|  
|5|2|2|  
|6|2|2|  

 **Movs. contabilidad**  

|Fecha registro|Cuenta|Nº cuenta (demostración En-US)|Importe|Nº mov.|  
|------------------|------------------|---------------------------------|------------|---------------|  
|15-01-20|Cuenta de ajuste de inventario (provisional)|5530|95,00|4|  
|15-01-20|Cta. inventario (provisional)|2131|-95,00|3|  
|15-01-20|Cuenta aplic. coste directo|7291|-100|6|  
|15-01-20|Cta. inventario|2130|100|5|  

## <a name="see-also"></a>Consulte también
 [Detalles de diseño: Coste de inventario](design-details-inventory-costing.md)   
 [Detalles de diseño: Ajuste de coste](design-details-cost-adjustment.md)   
 [Detalles de diseño: Conciliación con contabilidad](design-details-reconciliation-with-the-general-ledger.md)   
 [Detalles de diseño: Registro de inventario](design-details-inventory-posting.md)   
 [Detalles de diseño: Desviación](design-details-variance.md)  
 [Gestión de costes de inventario](finance-manage-inventory-costs.md)  
 [Finanzas](finance.md)  
 [Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]