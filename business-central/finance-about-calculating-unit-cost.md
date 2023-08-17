---
title: Acerca del cálculo de coste unitario
description: Aprenda cómo el método de cálculo de costes y otros factores influyen en el campo Coste unitario de la ficha de producto.
author: rubenseishima
ms.service: dynamics365-business-central
ms.topic: article
ms.date: 03/06/2022
ms.author: edupont
---
# <a name="about-unit-cost-calculation"></a>Acerca del cálculo de coste unitario

Cada artículo tiene un coste unitario que se calcula en función del método de cálculo de costes de la empresa y otros factores. Como norma general, con el método de costes *Estándar*, el valor del campo **Coste unitario** se basa en el coste estándar del producto. Para todos los demás métodos de gestión de costes (*FIFO*, *LIFO*, *Específico* y *Promedio*), el coste unitario se calcula en función del coste unitario medio durante un período de tiempo.  

Para obtener más información, vea [Administrar costes de inventario](finance-manage-inventory-costs.md).  

## <a name="when-is-the-unit-cost-field-updated"></a>Cuando se actualiza el campo de coste unitario

El método de gestión de costes elegido influye en la actualización del campo **Coste unitario**.

Cuando el método de gestión de costes se establece como *Estándar*, el campo **Coste unitario** se actualiza cada vez que se cambia el coste estándar y los usuarios no pueden editar el campo **Coste unitario**. Para obtener más información, consulte [Actualizar costes estándar](finance-how-to-update-standard-costs.md).

Si el método de gestión de costes es *FIFO*, *LIFO*, *Especial* o *Promedio*, el **Coste unitario** se actualiza en los siguientes casos:

* Cuando el artículo se ajusta por coste, automáticamente o por una tarea [Ajustar coste](inventory-how-adjust-item-costs.md#to-adjust-item-costs-manually).
* Durante el registro de las facturas de compra, salida o ajuste positivo, si una de las siguientes condiciones es verdadera:
  * El total de unidades facturadas del producto cambia de cero o negativo a positivo.
  * El coste unitario actual es cero.

Si una de estas condiciones es verdadera, el campo **Coste unitario** se actualiza con el valor del campo **Último coste directo** de la ficha de producto.

> [!NOTE]
> El campo **Coste unitario** no se actualiza si el coste unitario actual es mayor que cero y el nuevo coste unitario es cero. Un coste unitario de cero se considera una excepción del negocio normal. Por tanto, el coste unitario actual se conserva para proporcionar el último valor relevante conocido. Esta excepción se aplica incluso si el inventario existente se ha revalorizado a cero.

En el campo **Coste unitario** de la ficha de producto, puede explorar en profundidad para comprobar el historial de transacciones de donde se calcula el coste promedio de unidades disponibles en la ventana **Inf. general cálculo cte. medio**.

## <a name="unit-cost-calculation-for-purchases"></a>Cálculo del coste unitario para las compras

Cuando compra productos, el valor del campo **Último precio compra** se copia de la ficha de producto al campo **Coste unit. directo** de una línea de compra o a la línea **Precio unitario** de una línea del diario del producto.

La opción que elija en el campo **Valoración existencias** influye en el modo en que [!INCLUDE[prod_short](includes/prod_short.md)] calcula el contenido del campo **Coste unitario** de las líneas.

### <a name="costing-method-fifo-lifo-specific-or-average"></a>Métodos de gestión de costes FIFO, LIFO, Específico o Promedio

[!INCLUDE[prod_short](includes/prod_short.md)] calcula el valor del campo **Coste unitario DL de la línea de compra** o el contenido del campo **Coste unitario** de la línea del diario de productos siguiendo la fórmula siguiente:

*Coste unitario (DL) = (Precio de compra - (Importe descuento / Cantidad)) × (1 + % Coste indirecto / 100) + Tasa costes generales*

### <a name="costing-method-standard"></a>Método de valoración de existencias Estándar

Se rellena el campo **Coste unitario (DL)** en la línea de compra o el campo **Coste unitario** de la línea del diario de productos al copiar el valor del campo **Coste unitario** de la ficha de producto. Cuando se utiliza el método de valoración de existencias *Estándar*, este valor siempre se basa en el coste estándar.

Cuando registra la compra, [!INCLUDE[prod_short](includes/prod_short.md)] usa el coste unitario de la línea de compra o del diario del producto en el movimiento de factura del producto de compra. Puede verlo en la lista de entrada del artículo.

### <a name="all-costing-methods"></a>Todos los métodos de valoración de existencias

El programa siempre utiliza el coste unitario de la línea de documento origen para calcular el contenido del campo **Importe coste Real** o, si corresponde, del campo **Importe coste Esperado** relativo a este movimiento de producto, sea cual sea el método de valoración de existencias del producto.

## <a name="unit-cost-calculation-for-sales"></a>Cálculo del coste unitario de ventas

Cuando vende productos, se copia el coste unitario que figura en el campo **Coste unitario** de la ficha de producto en la línea de venta o en la del diario de productos.

Al registrar, el programa copia el coste unitario en el movimiento del producto de la factura de venta, por lo que podrá verlo en la lista de movimientos del producto. [!INCLUDE[prod_short](includes/prod_short.md)] utilizará el coste unitario de la línea de documento origen para calcular el contenido del campo **Importe coste real** o, si corresponde, del campo **Importe coste Esperado** en el movimiento de valor relativo a este movimiento de producto.

## <a name="see-also"></a>Consulte también .

[Gestión de costes de inventario](finance-manage-inventory-costs.md)  
[Registro de productos nuevos](inventory-how-register-new-items.md)  
[Acerca del coste de inventario](finance-learn-about-costing.md)  
[Inventario](inventory-manage-inventory.md)  
[Ventas](sales-manage-sales.md)  
[Compras](purchasing-manage-purchasing.md)  
[Detalles de diseño: IVA no deducible](design-details-nondeductible-vat.md)
[Procedimientos recomendados de configuración: valoración de existencias](setup-best-practices-costing-method.md)  
[Detalles de diseño: métodos de coste](design-details-costing-methods.md)  
[Detalles de diseño: Ajuste de coste](design-details-cost-adjustment.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
