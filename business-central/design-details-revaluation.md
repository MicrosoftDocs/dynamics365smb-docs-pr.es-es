---
title: 'Detalles de diseño: Revalorización'
description: Puede revalorizar el inventario según la base de valoración que refleja de forma más precisa el valor de inventario.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 07/07/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
---

# <a name="design-details-revaluation"></a>Detalles de diseño: Revalorización

Puede revalorizar el inventario según la base de valoración que refleja de forma más precisa el valor de inventario. También puede especificar una fecha retroactiva para actualizar correctamente el coste total de las mercancías vendidas se actualice correctamente para los productos que ya se han vendido. Los productos que usan la valoración de existencias Estándar que no se han facturado por completo también se pueden volver a valorar.  

En [!INCLUDE[prod_short](includes/prod_short.md)], dispone de la flexibilidad siguiente en cuanto a revalorización:  

- La cantidad revalorizable se puede calcular para cualquier fecha, también en el pasado.  
- En el caso de productos con método de coste Estándar, los movimientos de coste previstos se incluyen en la revalorización.  
- Las salidas de existencias afectadas por la revalorización se detectan.  

## <a name="calculate-the-revaluable-quantity"></a>Calcular la cantidad revalorizable

La cantidad que puede revalorizar es el inventario restante disponible en una fecha determinada. La cantidad es el total de movimientos de productos completamente facturados que contabiliza en la fecha de revalorización o antes.  

> [!NOTE]  
>  Los productos que usan la valoración de existencias Estándar se tratan de distinta forma al calcular la cantidad que puede volver a valorar por producto, ubicación y variante. Las cantidades y los valores de los movimientos de producto que no se han facturado completamente están incluidos en la cantidad revalorizable.  

Después de que se haya registrado una revalorización, puede registrar una entrada de existencias o una salida con una fecha de registro anterior a la fecha de registro de la revalorización. No obstante, esta cantidad no se verá afectada por la revalorización. Para equilibrar el inventario, solo se tiene en cuenta la cantidad revalorizable original.  

Dado que puede revalorizar en cualquier fecha, debe tener convenciones para cuando considere un artículo como parte del inventario. Por ejemplo, cuando el producto está en el inventario y está catalogado como trabajo en curso (WIP).  

### <a name="example"></a>Ejemplo

En el ejemplo siguiente se ilustra cuándo forman parte del inventario las transiciones de producto de trabajo en curso. El ejemplo se basa en la producción de una cadena con 150 eslabones.  

![Inventario WIP y revalorización.](media/design_details_inventory_costing_10_revaluation_wip.png "Inventario WIP y revalorización")  

**1T**: el usuario registra vínculos de comprados según se reciben. En la tabla siguiente se muestra el movimiento de producto resultante.  

|Fecha registro|Producto|Tipo mov.|Cantidad|Nº mov.|  
|------------------|----------|----------------|--------------|---------------|  
|01-01-20|VÍNCULO|Compra|150|1|  

> [!NOTE]  
>  Ahora, un producto que use la valoración de existencias Estándar estará disponible para la revalorización.  

**1V**: el usuario registra vínculos de comprados como facturados y los vínculos se convierten en parte del inventario desde un punto de vista financiero. En la tabla siguiente se muestran los movimientos de valoración resultantes.  

|Fecha registro|Tipo mov.|Fecha valoración|Importe coste (Real)|Nº mov. producto|Nº mov.|  
|------------------|----------------|--------------------|----------------------------|---------------------------|---------------|  
|15-01-20|Coste directo|01-01-20|150,00|1|1|  

 **2T + 2V**: el usuario registra vínculos de comprados como consumidos para la producción de la cadena de hierro. Desde un punto de vista financiero, los vínculos pasan a formar parte del inventario WIP.  En la tabla siguiente se muestra el movimiento de producto resultante.  

|Fecha registro|Producto|Tipo mov.|Cantidad|Nº mov.|  
|------------------|----------|----------------|--------------|---------------|  
|01-02-20|VÍNCULO|Consumo|-150|1|  

En la tabla siguiente se muestra el movimiento de valoración resultante.  

|Fecha registro|Tipo mov.|Fecha valoración|Importe coste (Real)|Nº mov. producto|Nº mov.|  
|------------------|----------------|--------------------|----------------------------|---------------------------|---------------|  
|01-02-20|Coste directo|01-02-20|-150,00|2|2|  

La fecha de valoración se establece en la fecha del registro de consumo (01-02-20), como una salida de existencias normal.  

**3T**: el usuario registra la cadena como salida y termina el orden de producción. En la tabla siguiente se muestra el movimiento de producto resultante.  

|Fecha registro|Producto|Tipo mov.|Cantidad|N.º de movimiento|  
|------------------|----------|----------------|--------------|---------------|  
|15-02-20|CADENA|Output|1|3|  

**3V**: El usuario ejecuta el trabajo por lotes de **Ajuste de costes - Movimientos de producto**, el cual registra la cadena como facturada para indicar que todo el consumo de material se ha facturado completamente. Desde un punto de vista financiero, los enlaces ya no forman parte del inventario WIP cuando se factura y se ajusta totalmente la salida. En la tabla siguiente se muestran los movimientos de valoración resultantes.  

|Fecha registro|Tipo mov.|Fecha valoración|Importe coste (Real)|Nº mov. producto|Nº mov.|  
|------------------|----------------|--------------------|----------------------------|---------------------------|---------------|  
|15-01-20|Coste directo|01-01-20|150,00|2|2|  
|01-02-20|Coste directo|01-02-20|-150,00|2|2|  
|15-02-20|Coste directo|15-02-20|150.00|3|3|  

## <a name="expected-cost-in-revaluation"></a>Coste previsto en revalorización

La cantidad que puede revalorizar se calcula como la suma de la cantidad de movimientos de producto totalmente facturados con una fecha de registro igual o anterior a la fecha de revalorización. Cuando se reciben o envían productos pero no se facturan, su valor de inventario no se puede calcular. Los productos que usan la valoración de existencias Estándar no están limitados en este sentido.  

> [!NOTE]  
>  Otro tipo de coste esperado que puede ser revalorizado es el inventario WIP, con determinadas reglas. Para obtener más información, vea [Revaluación de inventario WIP](design-details-revaluation.md#wip-inventory-revaluation).  

Al calcular la cantidad revalorizable de los productos que usan la valoración de existencias Estándar, el cálculo incluye los movimientos de producto que no se han facturado por completo. A continuación, estos movimientos se revalorizan al registrar la revalorización. Cuando se factura la entrada revalorizada, se crean los siguientes movimientos de valoración:  

- El movimiento de valoración facturado habitual con el tipo de movimiento **Coste directo**. El importe de coste de establece movimiento es el coste directo de la línea de origen.  
- Una entrada de valor con tipo de entrada **Desviación**. Este movimiento registra la diferencia entre el coste facturado y el coste estándar revalorizado.  
- Una entrada de valor con tipo de entrada **Revalorización**. Este movimiento registra la reversión de la revalorización del coste previsto.

### <a name="example-1"></a>Ejemplo

El siguiente ejemplo se basa en la producción de la cadena del ejemplo anterior. Este ejemplo ilustra cómo se crean los tres tipos de entradas, según el siguiente escenario:  

1.  Se registran los eslabones comprados como recibidos con un coste unitario de 2,00 DL.  
2.  Se registra una revalorización de los eslabones con un nuevo coste unitario de 3,00 DL, con lo que se actualiza el coste estándar a 3,00 DL.  
3.  Se registra la compra original de los eslabones como facturados, que crea los siguientes movimientos de valor:  

    1.  Un movimiento de valor facturado con un tipo de entrada **Coste directo**.  
    2.  Una entrada de valor con tipo de entrada **Revalorización** para registrar la reversión de revalorización del coste previsto.  
    3.  Una entrada de valor con tipo de entrada Desviación para registrar la diferencia entre el coste facturado y el coste estándar revalorizado.  

La siguiente tabla muestra los resultados.  

|Paso|Fecha de registro|Tipo mov.|Fecha valoración|Importe coste (Esperado)|Importe coste (Real)|Nº mov. producto|Nº mov.|  
|----------|------------------|----------------|--------------------|------------------------------|----------------------------|---------------------------|---------------|  
|1.|15-01-20|Coste directo|15-01-20|300,00|0.00|1|1|  
|2.|20-01-20|Revaluación|20-01-20|150,00|0.00|1|2|  
|3.a.|15-01-20|Coste directo|15-01-20|-300,00|0.00|1|3|  
|3.b.|15-01-20|Revaluación|20-01-20|-150,00|0.00|1|4|  
|3.c.|15-01-20|Desviación|15-01-20|0.00|450.00|1|5|  

## <a name="determine-whether-revaluation-affects-an-inventory-decrease"></a>Determinar si la revalorización afecta a una disminución del inventario

Use la fecha del registro o de la revalorización se usa para determinar si una salida de existencias está afectada por una revalorización.  

En la tabla siguiente se muestran los criterios que se usan para un producto que no usa la valoración de existencias Media.  

|Escenario|N.º de movimiento|Tiempo|Afectado por revalorización|  
|--------------|---------------|------------|-----------------------------|  
|A|Anterior al número de movimiento de revalorización|Anterior a la fecha de registro de revalorización|No|  
|B|Anterior al número de movimiento de revalorización|Igual a la fecha de registro de revalorización|No|  
|C|Anterior al número de movimiento de revalorización|Posterior a la fecha de registro de revalorización|Sí|  
|D|Posterior al movimiento de revalorización número|Anterior a la fecha de registro de revalorización|Sí|  
|E|Posterior al movimiento de revalorización número|Igual a la fecha de registro de revalorización|Sí|  
|F|Posterior al movimiento de revalorización número|Posterior a la fecha de registro de revalorización|Sí|  

### <a name="example-2"></a>Ejemplo

El ejemplo siguiente ilustra la revalorización de un producto que usa la valoración de existencias FIFO. El ejemplo se basa en el siguiente caso:  

1.  El 01-01-20, registra una compra de 6 unidades.  
2.  El 02-01-20, registra una venta de 1 unidad.  
3.  El 03-01-20, registra una venta de 1 unidad.  
4.  El 04-01-20, registra una venta de 1 unidad.  
5.  El 01-03-20, calcula el valor de inventario del producto y registra una revalorización del coste unitario del producto de 10,00 DL a 8,00 DL.  
6.  El 02-01-20, registra una venta de 1 unidad.  
7.  El 03-01-20, registra una venta de 1 unidad.  
8.  El 04-01-20, registra una venta de 1 unidad.  
9. Ejecuta el proceso **Valorar stock - movs. producto**.  

En la tabla siguiente se muestran los movimientos de valoración resultantes.  

|Caso|Fecha registro|Tipo mov.|Fecha valoración|Cdad. valorada|Importe coste (Real)|Nº mov. producto|Nº mov.|  
|--------------|------------------|----------------|--------------------|---------------------|----------------------------|---------------------------|---------------|  
||01-01-20|Compra|01-01-20|6|60.00|1|1|  
||01-03-20|Revaluación|01-03-20|4|-8,00|1|5|  
|A|01-02-20|Venta|01-02-20|-1|-10,00|2|2|  
|B|01-03-20|Venta|01-03-20|-1|-10,00|3|3|  
|C|01-04-20|Venta|01-04-20|-1|-10,00|4|4|  
||01-04-20|Venta|01-04-20|-1|2.00|4|9|  
|D|01-02-20|Venta|01-03-20|-1|-10,00|5|6|  
||01-02-20|Venta|01-03-20|-1|2.00|5|10|  
|E|01-03-20|Venta|01-03-20|-1|-10,00|6|7|  
||01-03-20|Venta|01-03-20|-1|2.00|6|11|  
|F|01-04-20|Venta|01-04-20|-1|-10,00|7|8|  
||01-04-20|Venta|01-04-20|-1|2.00|7|12|  

## <a name="wip-inventory-revaluation"></a>Revalorización de inventario WIP

La revalorización del inventario WIP implica la revalorización de los componentes registrados como inventario WIP.  

Es importante disponer de convenciones que controlen cuándo un artículo es inventario WIP desde un punto de vista financiero. En [!INCLUDE[prod_short](includes/prod_short.md)] existen las convenciones siguientes:  

- Un componente comprado pasa a formar parte del inventario de materias primas cuando se registra una compra como facturada.  
- Un componente comprado o subensamblado pasa a formar parte del inventario WIP cuando se registra su consumo con una orden de producción.  
- Un componente comprado/subensamblado sigue siendo parte del inventario WIP hasta que factura una orden de producción (producto fabricado).  

La forma en que se configura la fecha de valoración del movimiento de valoración sigue las mismas reglas que en el caso del inventario que no es del trabajo en curso. Para obtener más información, vaya a [Determinar si la revalorización afecta a una disminución del inventario](#determine-whether-revaluation-affects-an-inventory-decrease).  

Puede revalorizar el inventario WIP en las siguientes condiciones:

- La fecha de revalorización es anterior a las fechas de registro de los costes de movimiento de productos correspondientes del tipo Consumo.
- No ha facturado el pedido de producción.  

> [!CAUTION]  
> El informe **Valoración inventario - WIP** muestra el valor de los movimientos de orden de producción registradas y, por lo tanto, puede ser algo confuso para los productos del trabajo en curso que se han revalorizado.  

## <a name="revaluate-items-with-the-average-costing-method"></a>Revalorizar productos con el método de valorización de existencias Media

Solo puede revalorizar productos que usan la valorización de existencias Media si **Calcular por** es *Producto*.

Solo puede realizar una revaluación al final del período seleccionado en el campo **Período coste promedio** en la página **Configuración de inventario**.

La revalorización no afectará a las transacciones negativas del mes en curso, por lo que tampoco se incluyen los asientos de entrada totalmente aplicados.

### <a name="example-3"></a>Ejemplo

Este ejemplo muestra lo que sucede cuando calcula el valor de inventario en la página **Diario de revalorización de productos** . En la página **Configuración de inventario**, **Producto** se elige en el campo **Tipo cálculo cte. medio** y **Mes** se elige en el campo **Periodo coste promedio**.

La siguiente tabla muestra movimientos de productos para el artículo de coste medio de muestra, ITEM1.

|Fecha de registro|Tipo mov. producto|Cantidad|Importe coste (Real)|N.º de movimiento|
|----|----|----|----|----|
25-04-23|Compra|5|5.00|1
26-04-23|Compra|3|3.00|2
27-04-23|Venta|-5|-5,00|3
28-04-23|Venta|-1|-1,00|4
13-05-23|Compra|2|20.00|5
17-06-23|Venta|-6|-22,00|6

La siguiente tabla muestra el resultado de ejecutar el informe **Calcular valor inventario** con diferentes fechas de presentación.

|Fecha de registro|Cantidad|Comentario|
|---|---|-------------|
30-04-23|2|Incluye solo la cantidad restante de la entrada 2. La entrada 1 se aplica completamente antes de la fecha de contabilización y la entrada 5 es posterior a la fecha de contabilización.
31-05-23|4|Incluye las cantidades restantes de las entradas 2 y 13.
30-06-23|0|No hay cantidad restante en la fecha de registro.

El resultado de las siguientes entradas será 0, independientemente de la fecha de registro.

|Fecha de registro|Tipo mov. producto|Cantidad|Importe coste (Real)|N.º de movimiento|
|----|----|----|----|----|
13-05-23|Compra|5|5.00|1
26-04-23|Venta|-5|5.00|2

## <a name="see-also"></a>Consulte también

[Detalles de diseño: coste de inventario](design-details-inventory-costing.md)   
[Detalles de diseño: Métodos de coste](design-details-costing-methods.md)   
[Detalles de diseño: valoración de inventario](design-details-inventory-valuation.md)
[Gestión de costes de inventario](finance-manage-inventory-costs.md)  
[Finanzas](finance.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
