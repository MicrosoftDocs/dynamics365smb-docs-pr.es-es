---
title: Configuración de valoración de existencias | Documentos de Microsoft
description: En la tabla siguiente se indican una serie de tareas con vínculos a los temas que las describen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 931b0ac2a7ac7e33c69ec10bc3770ceda3b1659f
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/03/2019
ms.locfileid: "2879542"
---
# <a name="setting-up-inventory-valuation-and-costing"></a>Configuración de valoración de existencias
Para asegurarse de que los costes de inventario se registran correctamente, debe configurar varios campos y páginas antes de comenzar a realizar transacciones de elementos.

En la tabla siguiente se indican una serie de tareas con vínculos a los temas que las describen.

|**Para**|**Vea**|  
|------------|-------------|  
|Configurar una valoración de existencias para cada producto que rija cómo se utilizan sus costes entrantes para evaluar el valor de inventario y el coste de las mercancías vendidas.|[Registro de productos nuevos](inventory-how-register-new-items.md)|  
|Asegurar que el coste se registra automáticamente en la contabilidad cada vez que se registra una transacción de inventario.|Campo **Registro de costes automático** de la página **Configuración de inventario**.|  
|Asegurar que los costes esperados se registran en la contabilidad para ver a partir de las cuentas provisionales una estimación de los importes vencidos y el coste de los productos comercializados antes de que se facturen realmente.|**Registro de coste previsto en contabilidad** de la ventana **Configuración de inventario**.|  
|Configurar el sistema para ajustar los cambios de coste automáticamente cada vez que se registran transacciones de inventario.|[Modificar costes de productos](inventory-how-adjust-item-costs.md)|  
|Definir si el coste medio debe calcularse por producto solamente o por producto para cada unidad de almacenamiento y para cada variante del producto.|Campo **Tipo cálculo coste medio** en la página **Configuración de inventario**|  
|Seleccionar el periodo de tiempo que desea que utilice la aplicación para calcular el coste medio ponderado de los productos que utilizan la valoración de existencias media.|Campo **Periodo coste medio** en la página **Configuración de inventario**|  
|Definir periodos de inventario para controlar el valor del inventario con el tiempo no permitiendo el registro de transacciones en periodos de inventario cerrados.|[Trabajar con periodos de inventario](finance-how-to-work-with-inventory-periods.md)|  
|Asegurar que las devoluciones de ventas se liquidan con la transacción de salida original para conservar el valor del inventario.|Campo **Coste exacto reversión obligatoria** en la página **Ventas y cobros**|  
|Asegurar que las devoluciones de compras se liquidan con la transacción de entrada original para conservar el valor del inventario.|Campo **Coste exacto reversión obligatoria** en la página **Compras y pagos**|
|Configurar las reglas de redondeo que hay que aplicar al ajustar o sugerir precios de productos y al ajustar o sugerir costes estándar.|Página **Método de redondeo**|  

## <a name="see-also"></a>Consulte también  
[Gestión de costes de inventario](finance-manage-inventory-costs.md)  
[Trabajar con Business Central](ui-work-product.md)  
[Finanzas](finance.md)  
