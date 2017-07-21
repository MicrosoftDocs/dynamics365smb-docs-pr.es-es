---
title: Ajustar manualmente los costes de producto | Documentos de Microsoft
description: "Puede ajustar la valoración de inventario de un producto utilizando los métodos de costes FIFO o Promedio, por ejemplo, cuando los costes de producto cambien por motivos distintos de las transacciones."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cost adjustment, cost forwarding, costing method, inventory valuation, costing
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: a1f682b60b7b9ae402c27093f13aa3db2368ed5b
ms.contentlocale: es-es
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-adjust-item-costs-manually"></a>Ajustar los costes de producto manualmente
El precio de un producto (valor de inventario) que compre y más tarde venda puede cambiar durante su vida útil, por ejemplo, debido a que se agregue un coste de flete a su precio de compra después de que haya vendido el producto. El ajuste de coste es muy relevante en aquellas situaciones en las que se venden bienes antes de generar la factura de compra para dichos bienes. Para conocer siempre el valor de inventario correcto, los costes de productos se deben ajustar con frecuencia. Esto garantiza que las estadísticas relativas a ventas y beneficios estén actualizadas y que los KPI financieros sean correctos.

En [!INCLUDE[d365fin](includes/d365fin_md.md)], los costes de producto se actualizan automáticamente cada vez que aparece una transacción de inventario, como al registrar una factura de compra para un producto.

También puede usar una función para ajustar manualmente los costes de uno o varios productos. Esto resulta útil, por ejemplo, si sabe que los costes de producto han cambiado por motivos distintos a las transacciones de producto.

Los costes de producto ajustan por el método FIFO o Promedio, según la selección en la configuración asistida **Configurar mi empresa**. Para obtener más información, vea [Preparación para hacer negocios](ui-get-ready-business.md).  

Si utiliza el método de costes FIFO, el coste unitario de un producto es el valor real de cualquier recepción del producto. El inventario se valora con el supuesto de que los primeros productos colocados en el inventario se venden primero.

Si utiliza el método de costes Promedio, el coste unitario de un producto se calcula como el coste unitario medio en cada momento después de una compra. El inventario se valora con el supuesto de que todos los inventarios se venden simultáneamente.

La función de ajuste de precios solo procesa los movimientos de valores que aún no se hayan ajustado. Si la función encuentra una situación en que es necesario transferir los precios de entrada cambiados a movimientos de salida asociados, se crean nuevos movimientos de valor de ajuste, que se basan en la información de los movimientos de valor de ajuste, pero contienen el importe de ajuste. La función de ajuste de precios usa la fecha de registro del movimiento de valor original en el movimiento de ajuste, a menos que dicha fecha se encuentre dentro de un periodo del inventario que esté cerrado. En ese caso, el programa utilizará la fecha de inicio como el siguiente periodo del inventario abierto. Si no se usan periodos de inventario, la fecha del campo **Permitir registro desde** de la ventana **Configuración contabilidad** definirá cuándo se registra el movimiento de ajuste.

Los cambios en el valor de inventario de las operaciones comerciales se concilian automáticamente con los libros financieros cuando se registran transacciones de producto. Para obtener más información, consulte la sección "Conciliación de inventario" en [Inventario](inventory-manage-inventory.md).

## <a name="to-adjust-item-costs-manually"></a>Para ajustar manualmente precios de productos
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Valorar stock - movs. producto** y, a continuación, seleccione el vínculo relacionado.
2. En la ventana **Valorar stock - movs. producto**, especifique los productos cuyos costes ajustará.
3. Elija el botón **Aceptar**.

## <a name="see-also"></a>Consulte también
[Inventario](inventory-manage-inventory.md)  
[Ventas](sales-manage-sales.md)  
[Compras](purchasing-manage-purchasing.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

