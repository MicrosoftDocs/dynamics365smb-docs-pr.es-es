---
title: 'Detalles de diseño: Reevaluación | Documentos de Microsoft'
description: Puede revalorizar el inventario según la base de valoración que refleja de forma más precisa el valor de inventario. También puede especificar una fecha retroactiva para una revalorización, de modo que el coste total de las mercancías vendidas se actualice correctamente para los productos que ya se han vendido. Los productos que usan la valoración de existencias Estándar que no se han facturado por completo también se pueden volver a valorar.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: d0e779587a409232a6ab618ec80f5ad1ae17e31f
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/01/2020
ms.locfileid: "3184777"
---
# <a name="design-details-revaluation"></a>Detalles de diseño: Revalorización
Puede revalorizar el inventario según la base de valoración que refleja de forma más precisa el valor de inventario. También puede especificar una fecha retroactiva para una revalorización, de modo que el coste total de las mercancías vendidas se actualice correctamente para los productos que ya se han vendido. Los productos que usan la valoración de existencias Estándar que no se han facturado por completo también se pueden volver a valorar.  

En [!INCLUDE[d365fin](includes/d365fin_md.md)], dispone de la flexibilidad siguiente en cuanto a revalorización:  

-   La cantidad revalorizable se puede calcular para cualquier fecha, también en el pasado.  
-   En el caso de productos con método de coste Estándar, los movimientos de coste previstos se incluyen en la revalorización.  
-   Las salidas de existencias afectadas por la revalorización se detectan.  

## <a name="calculating-the-revaluable-quantity"></a>Cálculo de la cantidad revalorizable  
 La cantidad revalorizable es la cantidad restante en el inventario disponible para la revalorización en una fecha determinada. Se calcula como la suma total de las cantidades de movimientos de producto totalmente facturados con una fecha de registro igual o anterior a la fecha de registro de la revalorización.  

> [!NOTE]  
>  Los productos que usan la valoración de existencias Estándar se tratan de distinta forma al calcular la cantidad que puede volver a valorar por producto, ubicación y variante. Las cantidades y los valores de los movimientos de producto que no se han facturado completamente están incluidos en la cantidad revalorizable.  

Después de que se haya registrado una revalorización, puede registrar una entrada de existencias o una salida con una fecha de registro anterior a la fecha de registro de la revalorización. No obstante, esta cantidad no se verá afectada por la revalorización. Para equilibrar el inventario, solo se tiene en cuenta la cantidad revalorizable original.  

Dado que la operación de revalorización se puede realizar en cualquier fecha, deben existir convenciones para cuando un producto se considere parte del inventario desde un punto de vista financiero. Por ejemplo, cuando el producto está en el inventario y está catalogado como trabajo en curso (WIP).  

### <a name="example"></a>Ejemplo  
En el ejemplo siguiente se ilustra cuándo forman parte del inventario las transiciones de producto de trabajo en curso. El ejemplo se basa en la producción de una cadena con 150 eslabones.  

![Inventario WIP y revalorización](media/design_details_inventory_costing_10_revaluation_wip.png "Inventario WIP y revalorización")  

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
La cantidad revalorizable XE "Cantidad revalorizable" XE "Cantidad;Revalorizable" se calcula como la suma de la cantidad XE "cantidad" de movimientos de producto totalmente facturados XE "Factura" X· "Movimiento producto" con una fecha de registro igual o anterior a la fecha de revalorización XE "Revalorización". Esto significa que, cuando se reciben o envían productos pero no se facturan, su valor de inventario no se puede calcular XE "Valor de inventario". Los productos que usan la valoración de existencias Estándar no están limitados en este sentido. XE "Valor"  

> [!NOTE]  
>  Otro tipo de coste esperado que puede ser revalorizado es el inventario WIP, con determinadas reglas. Para obtener más información, consulte la sección "Revalorización de inventario WIP" en este tema.  

Al calcular la cantidad revalorizable de los productos mediante la valoración de existencias Estándar, los movimientos de producto que no se han facturado por completo se incluyen en el cálculo. A continuación, estos movimientos se revalorizan al registrar la revalorización. Cuando se factura la entrada revalorizada, se crean los siguientes movimientos de valoración:  

-   El movimiento de valoración facturado habitual con el tipo de movimiento **Coste directo**. El importe de coste de establece movimiento es el coste directo de la línea de origen.  
-   Una entrada de valor con tipo de entrada **Desviación**. Este movimiento registra la diferencia entre el coste facturado y el coste estándar revalorizado.  
-   Una entrada de valor con tipo de entrada **Revalorización**. Este movimiento registra la reversión de la revalorización del coste previsto.  

### <a name="example"></a>Ejemplo  
En el ejemplo siguiente, que se basa en la producción de la cadena del ejemplo anterior, se muestra cómo se crean los tres tipos de movimientos. Se basa en el siguiente caso:  

1.  El usuario registra los eslabones comprados como recibidos con un coste unitario de 2,00 DL.  
2.  A continuación, el usuario registra una revalorización de los eslabones con un nuevo coste unitario de 3,00 DL, con lo que se actualiza el coste estándar a 3,00 DL.  
3.  El usuario registra la compra original de los eslabones como facturados, que crea el siguiente:  

    1.  Un movimiento de valor facturado con un tipo de entrada **Coste directo**.  
    2.  Una entrada de valor con tipo de entrada **Revalorización** para registrar la reversión de revalorización del coste previsto.  
    3.  Una entrada de valor con tipo de entrada Desviación para registrar la diferencia entre el coste facturado y el coste estándar revalorizado.  
En la tabla siguiente se muestran los movimientos de valoración resultantes.  

|Paso|Fecha registro|Tipo mov.|Fecha valoración|Importe coste (Esperado)|Importe coste (Real)|Nº mov. producto|Nº mov.|  
|----------|------------------|----------------|--------------------|------------------------------|----------------------------|---------------------------|---------------|  
|1.|15-01-20|Coste directo|15-01-20|300,00|0.00|1|1|  
|2.|20-01-20|Revaluación|20-01-20|150,00|0.00|1|2|  
|3.a.|15-01-20|Coste directo|15-01-20|-300,00|0.00|1|3|  
|3.b.|15-01-20|Revaluación|20-01-20|-150,00|0.00|1|4|  
|3.c.|15-01-20|Desviación|15-01-20|0.00|450,00|1|5|  

## <a name="determining-if-an-inventory-decrease-is-affected-by-revaluation"></a>Determinación de si una salida de existencias se ve afectada por la revalorización  
La fecha del registro o de la revalorización se usa para determinar si una salida de existencias está afectada por una revalorización.  

En la tabla siguiente se muestran los criterios que se usan para un producto que no usa la valoración de existencias Media.  

|Caso|Nº mov.|Tiempo|Afectado por revalorización|  
|--------------|---------------|------------|-----------------------------|  
|A|Anterior al número de movimiento de revalorización|Anterior a la fecha de registro de revalorización|No|  
|B|Anterior al número de movimiento de revalorización|Igual a la fecha de registro de revalorización|No|  
|C|Anterior al número de movimiento de revalorización|Posterior a la fecha de registro de revalorización|Sí|  
|D|Posterior al movimiento de revalorización número|Anterior a la fecha de registro de revalorización|Sí|  
|E|Posterior al movimiento de revalorización número|Igual a la fecha de registro de revalorización|Sí|  
|F|Posterior al movimiento de revalorización número|Posterior a la fecha de registro de revalorización|Sí|  

### <a name="example"></a>Ejemplo  
El ejemplo siguiente, en el que se ilustra la revalorización de un producto que usa la valoración de existencias FIFO, se basa en el escenario siguiente:  

1.  El 01-01-20, el usuario registra una compra de 6 unidades.  
2.  El 01-02-20, el usuario registra una venta de 1 unidad.  
3.  El 01-03-20, el usuario registra una venta de 1 unidad.  
4.  El 01-04-20, el usuario registra una venta de 1 unidad.  
5.  El 01-03-20, el usuario calcula el valor de inventario del producto y registra una revalorización del coste unitario del producto de 10,00 DL a 8,00 DL.  
6.  El 01-02-20, el usuario registra una venta de 1 unidad.  
7.  El 01-03-20, el usuario registra una venta de 1 unidad.  
8.  El 01-04-20, el usuario registra una venta de 1 unidad.  
9. El usuario ejecuta el proceso **Valorar stock - movs. producto**.  

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
La revalorización del inventario de trabajo en curso implica la revalorización de los componentes que están registrados como parte del inventario de trabajo en curso en el momento de la revalorización.  

Teniendo en cuenta esto, es importante establecer convenciones, por ejemplo, cuándo se considera que un producto forma parte del inventario de trabajo en curso desde un punto de vista financiero. En [!INCLUDE[d365fin](includes/d365fin_md.md)] existen las convenciones siguientes:  

-   Un componente comprado pasa a formar parte del inventario de materias primas desde el momento de registrar una compra como facturada.  
-   Un componente comprado o haga subensamblado pasa a formar parte del inventario WIP desde el momento de registrar su consumo en relación a una orden de producción.  
-   Un componente comprado/subensamblado sigue siendo parte del inventario WIP hasta el momento en el que se factura una orden de producción (producto fabricado).  

La forma en que se configura la fecha de valoración del movimiento de valoración sigue las mismas reglas que en el caso del inventario que no es del trabajo en curso. Para obtener más información, consulte “Determinación de si una salida de existencias se ve afectada por la revalorización” en este tema.  

El inventario de trabajo en curso se puede revalorizar siempre y cuando la fecha de revalorización no sea posterior a la de registro de los movimientos de producto correspondientes del tipo Consumo y siempre y cuando la orden de producción correspondiente no se haya facturado todavía.  

> [!CAUTION]  
>  El informe **Valoración inventario - WIP** muestra el valor de los movimientos de orden de producción registradas y, por lo tanto, puede ser algo confuso para los productos del trabajo en curso que se han revalorizado.  

## <a name="see-also"></a>Consulte también  
 [Detalles de diseño: Coste de inventario](design-details-inventory-costing.md)   
 [Detalles de diseño: Métodos de coste](design-details-costing-methods.md)   
 [Detalles de diseño: valoración de inventario](design-details-inventory-valuation.md) [Gestión de costes de inventario](finance-manage-inventory-costs.md)  
 [Finanzas](finance.md)  
 [Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
