---
title: Ajustar manualmente los costes de producto
description: Puede ajustar la valoración de inventario de un producto utilizando los métodos de cálculo de costes FIFO o Promedio cuando cambian los costes de los productos.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'cost adjustment, cost forwarding, costing method, inventory valuation, costing'
ms.date: 03/08/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Ajustar costes de productos

El precio de un producto (valor de inventario) que compre y más tarde venda puede cambiar durante su vida útil, por ejemplo, debido a que se agregue un coste de flete a su precio de compra después de que haya vendido el producto. El ajuste de coste es muy relevante en aquellas situaciones en las que se venden bienes antes de generar la factura de compra para dichos bienes. Para conocer siempre el valor de inventario correcto, debería ajustar los costes de productos con frecuencia. Corregir costes ayuda a asegurar que las estadísticas relativas a ventas y beneficios estén actualizadas y que los KPI financieros sean correctos. Para obtener más información, consulte [Detalles de diseño: Ajuste de coste](design-details-cost-adjustment.md).

El valor del campo **Coste unitario** de la ficha de producto se basa en el coste estándar de los productos que utilizan el método de costes estándar. Para los productos que utilizan los demás métodos de coste, este valor se basa en el cálculo del inventario disponible (costes facturados y previstos) dividido por la cantidad física disponible. Para obtener más información, consulte [Comprender el cálculo del coste unitario](inventory-how-adjust-item-costs.md#understanding-unit-cost-calculation).

En [!INCLUDE[prod_short](includes/prod_short.md)], los costes de producto se actualizan automáticamente cada vez que aparece una transacción de inventario, como al registrar una factura de compra para un producto.

También puede ajustar manualmente los costes de uno o varios productos. Por ejemplo, los ajustes manuales son útiles si sabe que los costes de producto han cambiado por motivos distintos a las transacciones de producto.

Los costes de producto ajustan por el método FIFO o Promedio, según la selección en la guía de configuración asistida **Configurar mi empresa** o en el campo **Valoración de existencias** de la ficha de producto. Para obtener más información, vea [Registrar nuevos productos](inventory-how-register-new-items.md).  

Para el método de precio FIFO, el coste unitario de un producto es el valor real de cualquier recepción del producto. El inventario se valora con el supuesto de que los primeros productos colocados en el inventario se venden primero.

Si utiliza el método de costes Promedio, el coste unitario de un producto se calcula como el coste unitario medio en cada momento después de una compra. El inventario se valora con el supuesto de que todos los inventarios se venden simultáneamente. Para aquellos productos que utilizan este método, puede elegir el campo **Coste unitario** de la ficha del producto para ver el historial de las transacciones con las que se calcula el coste medio

El ajuste de precios solo procesa los movimientos de valores que no se hayan ajustado. En una situación en la que es necesario reenviar los costos de entrada modificados a las entradas de salida relacionadas, se crean nuevas entradas de valor de ajuste. Las entradas de valor de ajuste se basan en la información de las entradas de valor originales pero contienen el importe del ajuste. La función de ajuste de precios usa la fecha de registro del movimiento de valor original en el movimiento de ajuste, a menos que dicha fecha se encuentre dentro de un periodo del inventario que esté cerrado. En ese caso, la aplicación utilizará la fecha de inicio como el siguiente periodo del inventario abierto. Si no se utilizan periodos de inventario, la fecha del campo **Permitir registro desde** de la página **Configuración contabilidad** definirá cuándo se registra el movimiento de ajuste.

## Para ajustar manualmente precios de productos

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Ajustar coste: movimientos de producto**, y luego elija el enlace relacionado.
2. En la página **Valorar stock - movs. producto**, especifique los productos cuyos costes ajustará.
3. Elija el botón **Aceptar**.

## Para hacer cambios generales en el precio de compra

Si desea cambiar el precio de compra de varios productos, puede utilizar el proceso **Modificar precios de productos**.  

Este trabajo modifica el contenido del campo **Precio venta** de ficha producto. El proceso modifica el contenido del campo de la misma forma para todos los productos o para los productos seleccionados. El proceso multiplica el valor del campo por el factor de ajuste especificado.  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Modificar precios de productos**, y luego elija el enlace relacionado.  
2. En el campo de **Campo ajuste**, especifique qué producto o campo de la ficha UA desea ajustar.  
3. En el campo de **Factor ajuste**, especifique el factor por el que el valor se modificará. Por ejemplo, escriba **1,5** para aumentar el valor en un 50%.  
4. En la ficha desplegable **Producto**, especifique, por ejemplo, qué productos procesar con el trabajo por lotes.  
5. Elija el botón **Aceptar**.  

## Comprender el cálculo del coste unitario

El valor del campo **Coste unitario** de la ficha de producto se basa en el coste estándar de los productos que utilizan el método de costes estándar. Para los productos que utilizan los demás métodos de coste, este valor se basa en el cálculo del inventario disponible (costes facturados y previstos) dividido por la cantidad física disponible.  

En las siguientes secciones, se describe con más detalle la influencia del campo **Valoración existencias** en el cálculo del precio de coste de compras y de ventas.  

## Cálculo del coste unitario para las compras  

Cuando compra productos, el valor del campo **Último precio compra** se copia de la ficha de producto al campo **Coste unit. directo** de una línea de compra o a la línea **Precio unitario** de una línea del diario del producto.  

La opción que elija en el campo **Valoración existencias** influye en el modo en que [!INCLUDE[prod_short](includes/prod_short.md)] calcula el contenido del campo **Coste unitario** de las líneas.  

### Métodos de gestión de costes FIFO, LIFO, Específico o Promedio  

[!INCLUDE[prod_short](includes/prod_short.md)] usa la fórmula siguiente para calcular el valor del campo **Coste unitario DL de la línea de compra** o el contenido del campo **Coste unitario** de la línea del diario de productos.  

Coste unitario (DL) = (Precio de compra - (Importe descuento / Cantidad)) × (1 + % Coste indirecto / 100) + Tasa costes generales  

### Método de valoración de existencias Estándar  

Se rellena el campo **Coste unitario (DL)** en la línea de compra o el campo **Coste unitario** de la línea del diario de productos al copiar el valor del campo **Coste unitario** de la ficha de producto. Cuando se utiliza el método de valoración de existencias Estándar, este valor siempre se basa en el coste estándar.  

Cuando registra una compra, el coste unitario de la línea de compra o del diario del producto se copia en el movimiento de factura del producto de compra. Aparece en la lista de entrada del artículo.  

### Todos los métodos de valoración de existencias  

Se utilizará el coste unitario de la línea de documento origen para calcular el contenido del campo **Importe coste (real)** o, si corresponde, del campo **Importe coste (esperado)** en el movimiento de valor relativo a este movimiento de producto. El costo se incluye en el cálculo independientemente del método de cálculo del costo del artículo.  

## Cálculo del coste unitario de ventas  

Cuando vende productos, se copia el coste unitario que figura en el campo **Coste unitario** de la ficha de producto en la línea de venta o en la del diario de productos.  

Al registrar, el programa copia el coste unitario en el movimiento del producto de la factura de venta, por lo que podrá verlo en la lista de movimientos del producto. [!INCLUDE[prod_short](includes/prod_short.md)] utilizará el coste unitario de la línea de documento origen para calcular el contenido del campo **Importe coste real** o, si corresponde, del campo **Importe coste Esperado** en el movimiento de valor relativo a este movimiento de producto.  

## Realizar el seguimiento de ajustes de coste de producto

Los costos de los artículos pueden cambiar por muchas razones, por lo que es importante que puedas realizar un seguimiento de los ajustes de costos. Utilice la página **Ajuste de costos de inventario** para administrar y supervisar el proceso de ajuste de costos. Esta página muestra los artículos junto con sus parámetros de cálculo de costes y su estado de ajuste de costes. Puede filtrar la lista para centrarse en elementos que requieren ajuste o que están excluidos del proceso de ajuste de costos. Para obtener más información sobre el seguimiento de los ajustes de costos, vaya a [Seguimiento de los ajustes de costos de los artículos](finance-track-inventory-costs.md).

## Consulte también

[Gestión de costes de inventario](finance-manage-inventory-costs.md)  
[Grupos contables inventario](inventory-manage-inventory.md)  
[Ventas](sales-manage-sales.md)  
[Compras](purchasing-manage-purchasing.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]