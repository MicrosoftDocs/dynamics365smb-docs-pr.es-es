---
title: Ajustar manualmente los costes de producto | Documentos de Microsoft
description: Puede ajustar la valoración de inventario de un producto utilizando los métodos de costes FIFO o Promedio, por ejemplo, cuando los costes de producto cambien por motivos distintos de las transacciones.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cost adjustment, cost forwarding, costing method, inventory valuation, costing
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: b8d764bcbf1a7f6a2bc97130eddbdc1a644f9f1c
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2020
ms.locfileid: "3914169"
---
# <a name="adjust-item-costs"></a>Modificar costes de productos
El precio de un producto (valor de inventario) que compre y más tarde venda puede cambiar durante su vida útil, por ejemplo, debido a que se agregue un coste de flete a su precio de compra después de que haya vendido el producto. El ajuste de coste es muy relevante en aquellas situaciones en las que se venden bienes antes de generar la factura de compra para dichos bienes. Para conocer siempre el valor de inventario correcto, los costes de productos se deben ajustar con frecuencia. Esto garantiza que las estadísticas relativas a ventas y beneficios estén actualizadas y que los KPI financieros sean correctos. Para obtener más información, consulte [Detalles de diseño: Ajuste de coste](design-details-cost-adjustment.md).

Como norma general, el valor del campo **Coste unitario** de la ficha de producto se basa en el coste estándar de los productos que utilizan el método de costes estándar. Para los productos que utilizan los demás métodos de coste, este valor se basa en el cálculo del inventario disponible (costes facturados y previstos) dividido por la cantidad física disponible. Para obtener más información, consulte [Comprender el cálculo del coste unitario](inventory-how-adjust-item-costs.md#understanding-unit-cost-calculation).

En [!INCLUDE[d365fin](includes/d365fin_md.md)], los costes de producto se actualizan automáticamente cada vez que aparece una transacción de inventario, como al registrar una factura de compra para un producto.

También puede usar una función para ajustar manualmente los costes de uno o varios productos. Esto resulta útil, por ejemplo, si sabe que los costes de producto han cambiado por motivos distintos a las transacciones de producto.

Los costes de producto ajustan por el método FIFO o Promedio, según la selección en la guía de configuración asistida **Configurar mi empresa** o en el campo **Valoración de existencias** de la ficha de producto. Para obtener más información, vea [Registrar nuevos productos](inventory-how-register-new-items.md).  

Si utiliza el método de costes FIFO, el coste unitario de un producto es el valor real de cualquier recepción del producto. El inventario se valora con el supuesto de que los primeros productos colocados en el inventario se venden primero.

Si utiliza el método de costes Promedio, el coste unitario de un producto se calcula como el coste unitario medio en cada momento después de una compra. El inventario se valora con el supuesto de que todos los inventarios se venden simultáneamente. Para aquellos productos que utilizan este método, puede elegir el campo **Coste unitario** de la ficha del producto para ver el historial de las transacciones con las que se calcula el coste medio

La función de ajuste de precios solo procesa los movimientos de valores que aún no se hayan ajustado. Si la función encuentra una situación en que es necesario transferir los precios de entrada cambiados a movimientos de salida asociados, se crean nuevos movimientos de valor de ajuste, que se basan en la información de los movimientos de valor de ajuste, pero contienen el importe de ajuste. La función de ajuste de precios usa la fecha de registro del movimiento de valor original en el movimiento de ajuste, a menos que dicha fecha se encuentre dentro de un periodo del inventario que esté cerrado. En ese caso, la aplicación utilizará la fecha de inicio como el siguiente periodo del inventario abierto. Si no se utilizan periodos de inventario, la fecha del campo **Permitir registro desde** de la página **Configuración contabilidad** definirá cuándo se registra el movimiento de ajuste.

## <a name="to-adjust-item-costs-manually"></a>Para ajustar manualmente precios de productos
1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Valorar stock - movs. producto** y luego elija el enlace relacionado.
2. En la página **Valorar stock - movs. producto**, especifique los productos cuyos costes ajustará.
3. Elija el botón **Aceptar**.

## <a name="to-make-general-changes-in-the-direct-unit-cost"></a>Para hacer cambios generales en el precio de compra
Si desea cambiar el precio de compra de varios productos, puede utilizar el proceso **Modificar precios de productos**.  

 Este trabajo modifica el contenido del campo **Precio venta** de ficha producto. El proceso modifica el contenido del campo de la misma forma para todos los productos o para los productos seleccionados. El proceso multiplica el valor del campo por el factor de ajuste especificado.  

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Modificar precios de productos** y luego elija el enlace relacionado.  
2. En el campo de **Campo ajuste**, especifique qué producto o campo de la ficha UA desea ajustar.  
3. En el campo de **Factor ajuste**, especifique el factor por el que el valor se modificará. Por ejemplo, escriba **1,5** para aumentar el valor en un 50%.  
4. En la ficha desplegable **Producto**, especifique, por ejemplo, qué productos procesar con el trabajo por lotes.  
5. Elija el botón **Aceptar**.  

## <a name="understanding-unit-cost-calculation"></a>Comprender el cálculo del coste unitario
Como norma general, el valor del campo **Coste unitario** de la ficha de producto se basa en el coste estándar de los productos que utilizan el método de costes estándar. Para los productos que utilizan los demás métodos de coste, este valor se basa en el cálculo del inventario disponible (costes facturados y previstos) dividido por la cantidad física disponible.  

 En las siguientes secciones, se describe con más detalle la influencia del campo **Valoración existencias** en el cálculo del precio de coste de compras y de ventas.  

## <a name="unit-cost-calculation-for-purchases"></a>Cálculo del coste unitario para las compras  
 Cuando compra productos, el valor del campo **Último precio compra** se copia de la ficha de producto en el campo **Coste unit. directo** de una línea de compra o en la línea Precio unitario de una línea del diario del producto.  

 La opción que elija en el campo **Valoración existencias** influye en el modo en que [!INCLUDE[d365fin](includes/d365fin_md.md)] calcula el contenido del campo **Coste unitario** de las líneas.  

### <a name="costing-method-fifo-lifo-specific-or-average"></a>Métodos de valoración de existencias FIFO, LIFO, Especial o Medio  
 [!INCLUDE[d365fin](includes/d365fin_md.md)] calcula el valor del campo **Coste unitario DL de la línea de compra** o el contenido del campo **Coste unitario** de la línea del diario de productos siguiendo la fórmula siguiente:  

 Coste unitario (DL) = (Precio de compra - (Importe descuento / Cantidad)) × (1 + % Coste indirecto / 100) + Tasa costes generales  

### <a name="costing-method-standard"></a>Método de valoración de existencias Estándar  
 Se rellena el campo **Coste unitario (DL)** en la línea de compra o el campo **Coste unitario** de la línea del diario de productos al copiar el valor del campo **Coste unitario** de la ficha de producto. Cuando se utiliza el método de valoración de existencias Estándar, siempre se basa en el coste estándar.  

 Cuando registra la compra, se copia el coste unitario de la línea de compra o del diario del producto en el movimiento de factura del producto de compra, y lo podrá ver en la lista de movimientos del producto.  

### <a name="all-costing-methods"></a>Todos los métodos de valoración de existencias  
 El programa siempre utiliza el coste unitario de la línea de documento origen para calcular el contenido del campo **Importe coste Real** o, si corresponde, del campo **Importe coste Esperado** relativo a este movimiento de producto, sea cual sea el método de valoración de existencias del producto.  

## <a name="unit-cost-calculation-for-sales"></a>Cálculo del coste unitario de ventas  
 Cuando vende productos, el programa copia el coste unitario que figura en el campo Coste unitario de la ficha de producto en la línea de venta o en la del diario de productos.  

 Al registrar, el programa copia el coste unitario en el movimiento del producto de la factura de venta, por lo que podrá verlo en la lista de movimientos del producto. [!INCLUDE[d365fin](includes/d365fin_md.md)] utilizará el coste unitario de la línea de documento origen para calcular el contenido del campo **Importe coste real** o, si corresponde, del campo **Importe coste Esperado** en el movimiento de valor relativo a este movimiento de producto.  

## <a name="see-also"></a>Consulte también
[Gestión de costes de inventario](finance-manage-inventory-costs.md)  
[Inventario](inventory-manage-inventory.md)  
[Ccial](sales-manage-sales.md)  
[Compras](purchasing-manage-purchasing.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
