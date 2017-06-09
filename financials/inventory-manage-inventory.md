---
title: Inventario | Documentos de Microsoft
description: "Describe el modo de administrar los productos físicos."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, stock
ms.date: 03/28/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: b53cae82cfa532fb0620cc9e1f305216c2321785
ms.contentlocale: es-es
ms.lasthandoff: 05/04/2017

---

# <a name="inventory"></a>Grupos contables inventario
Por cada producto físico que se comercialice, debe crear una ficha de producto del tipo **Inventario**. Los productos que ofrece a los clientes pero que no mantiene en el inventario, puede registrarlos como productos sin stock, y puede convertirlos a productos de inventario cuando sea necesario. Puede aumentar o reducir la cantidad de un producto en el inventario registrándolo directamente desde los movimientos de producto, por ejemplo, después de un recuento físico o si no registra compras.

Los aumentos y las disminuciones de inventario también se registran cuando registra documentos de compra y de ventas respectivamente. Para obtener más información, vea [Procedimiento: Registrar](purchasing-how-record-purchases.md), [Procedimiento: Vender productos](sales-how-sell-products.md) y [Procedimiento: Facturar ventas](sales-how-invoice-sales.md). Las transferencias entre almacenes cambian las cantidades de inventario en los almacenes de la empresa.   

Para aumentar la información general de los productos y ayudarle a encontrarlos, puede clasificar los productos y darles atributos para que los pueda ordenar y buscar.

Debe asegurarse de que los costes de los productos se dirigen a la transacción de venta de salida relacionada, especialmente en aquellas situaciones en las que vende bienes antes de facturar compra de dichos productos. A esto se le conoce como ajuste de coste, que puede realizar manualmente o configurar automáticamente cuando se registra una transacción de producto.

Los cambios en el valor de inventario de las operaciones comerciales se concilian automáticamente con los libros financieros cuando se registran transacciones de producto.

|Para |Vea |
|---|----|
|Crear fichas de los productos de inventario que comercialice.|[Registro de productos nuevos](inventory-how-register-new-items.md)|
|Estructure los productos principales que vende como kits que constan de los componentes del principal o que ensamble para pedido o para stock.|[Trabajar con listas de materiales](inventory-how-work-BOMs.md)|
|Mantener una visión general de los productos y ayudarle a buscarlos y clasificarlos al organizarlos en categorías.|[Clasificar productos](inventory-how-categorize-items.md)|
|Asignar atributos de producto de distintos tipos de valor a sus productos le ayudará a ordenarlos y encontrarlos.|[Trabajar con atributos de producto](inventory-how-work-item-attributes.md)|
|Crear fichas especiales para los productos que desea ofrecer a los clientes, pero que no desea mantener en el inventario.|[Trabajar con productos sin stock](inventory-how-work-nonstock-items.md)|
|Aumento o disminución de la cantidad de inventario de un producto, como después de un recuento físico o como simple forma de registrar albaranes de compra.|[Ajuste de inventario](inventory-how-adjust-inventory.md)|
|Ver la disponibilidad de productos por almacén, por periodo, por evento de venta o de compra, o por su uso en las L.M. de ensamblado.|[Obtener un resumen de disponibilidad](inventory-how-availability-overview.md)|
|Transferir productos de inventario entre almacenes con pedidos de transferencia, para administrar las actividades de almacén o con el diario de reclasificación de productos.|[Transferir el inventario entre almacenes](inventory-how-transfer-between-locations.md)|
|Apreciar o amortizar el valor de uno o más productos del inventario registrando el valor calculado actual.|[Revaluación de inventario](inventory-how-revalue-inventory.md)|
|Ajuste los costes de productos, automática o manualmente, para desviar los cambios de coste de los movimientos de entrada a sus movimientos de salida relacionados.|[Ajustar precios de productos](inventory-how-adjust-item-costs.md)|
|Obtenga información acerca de cómo los cambios en el valor de inventario de las operaciones comerciales se concilian con los libros financieros.|[Avanzado: Conciliación de inventario](advanced-inventory-reconciliation.md)|

## <a name="see-also"></a>Consulte también  
[Compras](purchasing-manage-purchasing.md)  
[Ventas](sales-manage-sales.md)    
[Cadena de suministro](madeira-supply-chain.md)  
[Trabajar con [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)](ui-work-product.md)  
[Funciones empresariales generales](ui-across-business-areas.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]
