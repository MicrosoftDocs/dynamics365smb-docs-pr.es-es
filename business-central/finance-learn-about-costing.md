---
title: Acerca de inventario y valoración | Documentos de Microsoft
description: Administrar inventario y valoración se refiere al registro y la creación de informes sobre los costes de explotación de la empresa. Incluye la creación de informes de los costes de stock y fabricación, es decir, el valor de los productos.
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
ms.openlocfilehash: 9706e072261d89a68527a0801a57f78296bb2cc1
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/29/2019
ms.locfileid: "1238215"
---
# <a name="about-inventory-costing"></a>Acerca del contabilidad de valoración
Administrar inventario y valoración se refiere al registro y la creación de informes sobre los costes de explotación de la empresa. Incluye la creación de informes de los costes de stock y fabricación, es decir, el valor de los productos.  

 Es preciso entender los principios básicos, es decir, que los métodos de valoración definen cómo se valoran los productos cuando salen del inventario, que el ajuste de costes actualiza el coste de las mercancías vendidas con los costes de compra asociados registrados tras su venta y que los valores de inventario deben registrarse en cuentas contables exclusivas periódicamente.  

 En la tabla siguiente se indican una serie de tareas con vínculos a los temas que las describen.   

|**Para**|**Vea**|  
|------------|-------------|  
|Distinguir los cinco métodos diferentes de valoración de existencias y su efecto en los flujos de coste.|[Detalles de diseño: Métodos de coste](design-details-costing-methods.md)|  
|Conocer cómo los movimientos de liquidación de productos vinculan dinámicamente las reducciones de existencias con aumentos para mantener un control de los flujos de costes.|[Detalles de diseño: Liquidación de productos](design-details-item-application.md)|  
|Conocer cómo se actualiza continuamente el coste unitario de un producto con el coste de su última transacción según la valoración de existencias del producto.|[Detalles de diseño: Ajuste de coste](design-details-cost-adjustment.md)|  
|Aprender cómo se calcula dinámicamente el coste medio de un producto según el periodo de coste medio seleccionado.|[Detalles de diseño: Coste medio](design-details-average-cost.md)|  
|Distinguir el coste previsto (aún no facturado) del coste real y conocer cómo se administra en la contabilidad.|[Detalles de diseño: Registro de coste previsto](design-details-expected-cost-posting.md)|  
|Conocer el mecanismo de ajuste de coste, que asegura que los costes se presentan aunque las transacciones de existencias tengan lugar de manera aleatoria.|[Detalles de diseño: Ajuste de coste](design-details-cost-adjustment.md)|  
|Leer por qué los costes estándar los suelen utilizar las empresas de fabricación como base de valoración para los componentes y productos finales.|[Acerca del cálculo de coste estándar](finance-about-calculating-standard-cost.md)|  
|Conocer cómo se refleja el valor de existencias en la contabilidad.|[Creación de informes de costes y conciliación con la contabilidad](finance-report-costs-and-reconcile-with-the-general-ledger.md)|  
|Aprender cómo los cargos de los productos, como flete y seguro, pueden asignar componentes de coste adicionales al coste unitario de un producto.|[Usar los cargos de producto a cuenta para los costes comerciales adicionales](payables-how-assign-item-charges.md)|  
|Leer cómo los periodos de inventario ayudan a las empresas a controlar el valor de las existencias con el tiempo definiendo periodos más cortos que se pueden cerrar para registrar según avanza el año fiscal.|[Trabajar con periodos de inventario](finance-how-to-work-with-inventory-periods.md)|  
|Comprender todos los mecanismos del motor de cálculo de costos, incluyendo lo que sucede cuando se registran las transacciones de montaje y producción.|[Detalles de diseño: Coste de inventario](design-details-inventory-costing.md)|

## <a name="see-also"></a>Consulte también
[Gestión de costes de inventario](finance-manage-inventory-costs.md)    
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
