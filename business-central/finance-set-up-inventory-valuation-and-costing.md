---
title: Configuración de valoración de existencias
description: 'Para asegurarse de que los costes de inventario se registran correctamente, debe configurar varios campos y páginas antes de comenzar a realizar transacciones de elementos.'
author: brentholtorf
ms.topic: conceptual
ms.search.keywords: null
ms.date: 06/16/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Configuración de valoración de existencias

Para asegurarse de que los costes de inventario se registran correctamente, debe configurar varios campos y páginas antes de comenzar a realizar transacciones de elementos. Por lo general, las empresas eligen una valoración de existencias específica y la aplican a los productos del inventario, por ejemplo, para ayudarles a seguir el valor de los productos en stock.  

> [!TIP]
> Para una introducción al cálculo de costos en [!INCLUDE [prod_short](includes/prod_short.md)], consulte [Acerca de la variación de existencias](finance-learn-about-costing.md).

En la tabla siguiente se indican una serie de tareas con vínculos a los temas que las describen.

|**Para**|**Vea**|  
|------------|-------------|
|Especifique una valoración de existencias predeterminada para la empresa y así regir cómo se utilizan sus costes entrantes para evaluar el valor de inventario y el coste de las mercancías vendidas.|[Configurar información de inventario general](inventory-how-setup-general.md)|  
|Especifique una valoración de existencias de productos individuales si requieren un método de valoración de existencias diferente.|[Registro de productos nuevos](inventory-how-register-new-items.md)|  
|Asegurar que el coste se registra automáticamente en la contabilidad cada vez que se registra una transacción de inventario.|Campo **Registro de costes automático** de la página **Configuración de inventario**.|  
|Asegurar que los costes esperados se registran en la contabilidad para ver a partir de las cuentas provisionales una estimación de los importes vencidos y el coste de los productos comercializados antes de que se facturen realmente.|**Registro de coste previsto en contabilidad** de la ventana **Configuración de inventario**.|  
|Configurar el sistema para ajustar los cambios de coste automáticamente cada vez que se registran transacciones de inventario.|[Modificar costes de productos](inventory-how-adjust-item-costs.md)|  
|Defina si el coste medio debe calcularse por producto solamente o por producto para cada unidad de almacenamiento y para cada variante del producto.|Campo **Tipo cálculo coste medio** en la página **Configuración de inventario**|  
|Seleccionar el periodo de tiempo que desea que utilice la aplicación para calcular el coste medio ponderado de los productos que utilizan la valoración de existencias media.|Campo **Periodo coste medio** en la página **Configuración de inventario**|  
|Definir periodos de inventario para controlar el valor del inventario con el tiempo no permitiendo el registro de transacciones en periodos de inventario cerrados.|[Trabajar con periodos de inventario](finance-how-to-work-with-inventory-periods.md)|  
|Asegurar que las devoluciones de ventas se liquidan con la transacción de salida original para conservar el valor del inventario.|Campo **Coste exacto reversión obligatoria** en la página **Ventas y cobros**|  
|Asegurar que las devoluciones de compras se liquidan con la transacción de entrada original para conservar el valor del inventario.|Campo **Reversión de coste exacto obligatoria** en la página **Compras y pagos**|
|Configurar las reglas de redondeo que hay que aplicar al ajustar o sugerir precios de productos y al ajustar o sugerir costes estándar.|Página **Método de redondeo**|  

## Consulte también

[Gestión de costes de inventario](finance-manage-inventory-costs.md)  
[Configurar información de inventario general](inventory-how-setup-general.md)  
[Conciliar costes de inventario con la contabilidad general](finance-how-to-post-inventory-costs-to-the-general-ledger.md)  
[Procedimientos recomendados de configuración: valoración de existencias](setup-best-practices-costing-method.md)  
[Detalles de diseño: Coste de inventario](design-details-inventory-costing.md)  
[Detalles de diseño: cambiar la valoración de existencias para productos](design-details-changing-costing-methods.md)  
[Trabajar con Business Central](ui-work-product.md)  
[Finanzas](finance.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]