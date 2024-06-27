---
title: 'Detalles de diseño: Métodos de coste'
description: En este tema se describe cómo afecta la valoración de existencias si los valores reales y presupuestados se capitalizan y utilizan en el cálculo de costes.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: null
ms.date: 05/29/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Detalles de diseño: Métodos de coste

La valoración de existencias determina si en el cálculo de costes se capitaliza y utiliza un valor real o uno presupuestado. Junto con la fecha de registro y la secuencia, el método de coste también influye en cómo se registra el flujo de costes.

> [!NOTE]
> No puede modificar la valoración de existencias de un producto si existen movimientos de productos para el producto. Para más información, consulte [Detalles de diseño: cambiar la valoración de exisncias para productos](design-details-changing-costing-methods.md).

En [!INCLUDE[prod_short](includes/prod_short.md)] se admiten las siguientes valoraciones:  

| Método de coste | Descripción | Cuándo se debe usar |
|--|--|--|
| FIFO | El coste unitario de un producto es el valor real de cualquier recepción del producto, seleccionado durante la regla de FIFO.<br /><br /> La valoración del inventario asume que los primeros artículos colocados en el inventario se venden primero. | En entornos empresariales donde el coste de productos es estable.<br /><br /> (Cuando suben los precios, la hoja de balance muestra el valor mayor). Esto significa que las deudas tributarias aumentan, pero las puntuaciones de crédito y capacidad de pedir efectivo prestado mejoran.<br /><br /> En el caso de productos con una vida útil limitada, ya que los productos más antiguos deben venderse antes de que superen su fecha de límite de venta. |
| LIFO | El coste unitario de un producto es el valor real de cualquier recepción del producto, seleccionado durante la regla de LIFO.<br /><br /> La valoración del inventario asume que los últimos artículos colocados en el inventario se venden primero. | No se permite en muchos países o regiones, ya que puede utilizarse para debilitar las ganancias.<br /><br /> (Cuando suben los precios, el valor del balance de ingresos disminuye). Esto significa que las deudas tributarias disminuyen, pero la capacidad de pedir efectivo prestado deteriora. |
| Promedio | El coste unitario de un producto se calcula como el coste unitario medio en cada momento después de una compra.<br /><br /> La valoración de inventarios asume que todas las existencias se venden simultáneamente. | En entornos empresariales donde el coste de productos es inestable.<br /><br /> Cuando se apilan inventarios o se mezclan y no pueden ser diferenciados, tal como sustancias químicas. |
| Especial | El coste unitario de un producto es el coste exacto en el que la unidad determinada fue recibida. | En producción o comercio de productos fácilmente identificables con costes unitarios relativamente elevados.<br /><br /> En el caso de productos que están sujetos normativas.<br /><br /> Para productos con números de serie. |
| Estándar | El coste unitario de un producto se preestablece basándose en una estimación.<br /><br /> Cuando el coste real se realiza posteriormente, el coste estándar se debe ajustar al coste real a través de valores de varianza. | Cuando el control del coste es crítico.<br /><br /> En fabricación repetitiva para establecer el valor de los costes de material directo, mano de obra directa y gastos de fabricación.<br /><br /> Cuando hay disciplina y personal para mantener los estándares. |

En la imagen siguiente se muestra cómo fluyen los costes a través del inventario por cada valoración de existencias.  

![Métodos de valoración de existencias visualizados.](media/design_details_inventory_costing_7_costing_methods.png "Métodos de valoración de existencias visualizados")  

Los métodos de coste varían en cuanto a la forma en que el inventario disminuye y si se utiliza el coste real o el coste estándar como base de valoración. En la tabla siguiente se explican las diferentes características. (Se excluye el método LIFO por ser muy parecido al método FIFO).  
<!--Old  table
|Category|FIFO|Average|Standard|Specific|  
|-|----------|-------------|--------------|--------------|  
|General characteristic|Easy to understand|Based on period options: **Day**/**Week**/**Month**/**Quarter**/**Accounting Period**.<br /><br /> Can be calculated per item or per item/location/variant.|Easy to use, but requires qualified maintenance.|Requires item tracking on both inbound and outbound transaction.<br /><br /> Typically used for serialized items.|  
|Application/Adjustment|Application keeps track of **the remaining quantity**.<br /><br /> Adjustment forwards costs according to quantity application.|Application keeps track of the **remaining quantity**.<br /><br /> Costs are calculated and forwarded per the **valuation date**.|Application keeps track of the **remaining quantity**.<br /><br /> Application is based on FIFO.|All applications are fixed.|  
|Revaluation|Revalues invoiced quantity only.<br /><br /> Can be done per item or per item ledger entry.<br /><br /> Can be done backward in time.|Revalues invoiced quantity only.<br /><br /> Can be done per item only.<br /><br /> Can be done backward in time.|Revalues invoiced and un-invoiced quantities.<br /><br /> Can be done per item or per item ledger entry.<br /><br /> Can be done backward in time.|Revalues invoiced quantity only.<br /><br /> Can be done per item or per item ledger entry.<br /><br /> Can be done backward in time.|  
|Miscellaneous|If you back-date an inventory decrease, then existing entries are NOT reapplied to provide a correct FIFO cost flow.|If you back-date an inventory increase or decrease, then the average cost is recalculated, and all affected entries are adjusted.<br /><br /> If you change the period or calculation type, then all affected entries must be adjusted.|Use the **Standard Worksheet** page to periodically update and roll up standard costs.<br /><br /> Is NOT supported per SKU.<br /><br /> No historic records exist for standard costs.|You can use specific item tracking without using the Specific costing method. Then the cost will NOT follow the lot number, but the cost assumption of the selected costing method.|  
-->
<!--Table flipped for slightly better readability -->

||Característica general|Aplicación/ajuste |Reevaluación|Varios |
|-|---------|---------|---------|---------|
|**FIFO**     |Fácil de comprender|La aplicación hace un seguimiento de **la cantidad pendiente**.<br /><br /> El ajuste desvía los costes según la liquidación de la cantidad. |Revaloriza solo la cantidad facturada.<br /><br /> Se puede hacer por producto o por movimiento de producto.<br /><br /> Se puede realizar retroactivamente.|Si se especifica una fecha retroactiva para una salida de existencias, las entradas existentes NO se volverán a liquidar para proporcionar un flujo correcto FIFO del coste.|
|**Promedio**     |Basándose en opciones de periodo: **Día**/**Semana**/**Mes**/**Trimestre**/**Periodo contable**.<br /><br /> Se puede calcular por producto o por producto, almacén y variante.|La aplicación hace un seguimiento de la **cantidad pendiente**.<br /><br /> Los costes se calculan y se envían por la **fecha de valoración**. |Revaloriza solo la cantidad facturada.<br /><br /> Se puede hacer solo por producto.<br /><br /> Se puede realizar retroactivamente. |Si se retrocede la fecha de una entrada o una salida del inventario, se vuelve a calcular el coste medio y se ajustan todos los registros afectados.<br /><br /> Si cambia el periodo o el tipo de cálculo, todos los registros afectados deben ajustarse.|
|**Estándar**     |Fácil de usar pero requiere mantenimiento cualificado.|La aplicación hace un seguimiento de la **cantidad pendiente**.<br /><br /> La aplicación se basa en el método FIFO.|Revaloriza las cantidades facturadas y no facturadas.<br /><br /> Se puede hacer por producto o por movimiento de producto.<br /><br /> Se puede realizar retroactivamente.|Utilice la página **Hoja de trabajo estándar** para actualizar y distribuir periódicamente los costes estándar.<br /><br /> NO se admite por UA.<br /><br /> No existe ningún registro histórico para los costes estándar.|
|**Especial**     |Requiere el seguimiento de producto en la transacción de entrada y de salida.<br /><br /> Normalmente se usa para productos serializados.|Toda las liquidaciones son fijas.|Revaloriza solo la cantidad facturada.<br /><br /> Se puede hacer por producto o por movimiento de producto.<br /><br /> Se puede realizar retroactivamente.|Puede utilizar el seguimiento de producto específico sin usar la valoración de existencias Específica. El coste no seguirá el número de lote, sino el coste supuesto de la valoración de existencias seleccionada.|

## Ejemplo

En esta sección se proporcionan ejemplos de cómo las distintas valoraciones de existencias afectan al valor de inventario.  

En la tabla siguiente se muestran las entradas y las salidas de existencias en las que se basan los ejemplos.  

|Fecha registro|Cantidad|Nº mov.|  
|------------------|--------------|---------------|  
|01-01-20|1|1|  
|01-01-20|1|2|  
|01-01-20|1|3|  
|01-02-20|-1|4|  
|01-03-20|-1|5|  
|01-04-20|-1|6|  

> [!NOTE]  
> La cantidad resultante en el inventario es cero. Por tanto, el valor de inventario debe ser cero, independientemente del método de coste.  

### Efecto de los métodos de coste en la valoración de entrada de existencias  

En el caso de productos con métodos de coste que utilizan el coste real como base de valoración (**FIFO**, **LIFO**, **Promedio** o **Específico**), las entradas de existencias se calculan según el coste de compra del producto.  

- **Estándar**  

    En el caso de productos donde se use el método de costes **Estándar**, las entradas de existencias se calculan según el coste estándar actual.  

#### Estándar  

En el caso de productos donde se use el método de costes **Estándar**, las entradas de existencias se calculan según el coste estándar actual.  

### Efecto de los métodos de coste en la valoración de salidas de existencias

- **FIFO**  

    En el caso de productos con método de coste **FIFO**, los productos que se compraron primero se venden siempre primero (números de movimiento 3, 2 y 1 en este ejemplo). Así pues, las salidas de existencias se calculan tomando el valor de la primera entrada de existencias.  

     El CV se calcula a partir del valor de la primera adquisición del inventario.  

     En la tabla siguiente se muestra cómo se valoran las salidas de existencias para la valoración de existencias **FIFO**.  

    |Fecha registro|Cantidad|Importe coste (Real)|Nº mov.|  
    |------------------|--------------|----------------------------|---------------|  
    |01-02-20|-1|-10,00|4|  
    |01-03-20|-1|-20,00|5|  
    |01-04-20|-1|-30,00|6|  

- **LIFO**  

    En el caso de productos con método de coste **LIFO**, los productos que se compraron más recientemente se venden siempre primero (números de movimiento 3, 2 y 1 en este ejemplo). Así pues, las salidas de existencias se calculan tomando el valor de la última entrada de existencias.  

     El CV se calcula a partir del valor de las adquisiciones más recientes del inventario.  

     En la tabla siguiente se muestra cómo se valoran las salidas de existencias para la valoración de existencias **LIFO**.  

    |Fecha registro|Cantidad|Importe coste (Real)|Nº mov.|  
    |------------|--------|--------------------|---------|  
    |01-02-20|-1|-30,00|4|  
    |01-03-20|-1|-20,00|5|  
    |01-04-20|-1|-10,00|6|  

- **Promedio**  

    En el caso de productos que usen el método de coste **Promedio**, las salidas de existencias se valoran calculando un promedio ponderado del inventario que queda en el último día del periodo de coste medio en el cual se ha registrado una salida de existencias. Para obtener más información, consulte [Detalles de diseño: Coste medio](design-details-average-cost.md).  

     En la tabla siguiente se muestra cómo se valoran las salidas de existencias para la valoración de existencias **Media**.  

    | Fecha registro | Cantidad | Importe coste (Real) | Nº mov. |
    |--|--|--|--|
    | 01-02-20 | -1 | -20,00 | 4 |
    | 01-03-20 | -1 | -20,00 | 5 |
    | 01-04-20 | -1 | -20,00 | 6 |

- **Estándar**  

    En el caso de productos con método de coste **Estándar**, las salidas de existencias se valoran de forma parecida al método de coste **FIFO**, a menos que la valoración se base en un coste estándar y no en el coste real.  

    En la tabla siguiente se muestra cómo se valoran las salidas de existencias para la valoración de existencias **Estándar**.  

    |Fecha registro|Cantidad|Importe coste (Real)|Nº mov.|  
    |------------------|--------------|----------------------------|---------------|  
    |01-02-20|-1|-15,00|4|  
    |01-03-20|-1|-15,00|5|  
    |01-04-20|-1|-15,00|6|  

- **Específico**  

    Los métodos de coste determinan el flujo de costes desde una entrada de existencias a una salida de existencias. No obstante, si existe información más exacta sobre el flujo del coste, puede omitir esta suposición creando una liquidación fija entre los movimientos. Una liquidación fija crea un vínculo entre una salida de existencias y una entrada de existencias específica y direcciona el flujo de costes según corresponda.  

    En el caso de productos con método de coste **Específico**, las salidas de existencias se valoran según la entrada de existencias que vincula la liquidación fija.  

    En la tabla siguiente se muestra cómo se valoran las salidas de existencias para la valoración de existencias **Específica**.  

    |Fecha registro|Cantidad|Importe coste (Real)|Liq. por nº orden|Nº mov.|
    |------------|--------|--------------------|----------------|---------|  
    |01-02-20|-1|-20,00|**2**|4|  
    |01-03-20|-1|-10,00|**1**|5|  
    |01-04-20|-1|-30,00|**3**|6|  

## Consulte también

[Detalles de diseño: coste de inventario](design-details-inventory-costing.md)  
[Detalles de diseño: desviación](design-details-variance.md)  
[Detalles de diseño: coste medio](design-details-average-cost.md)  
[Detalles de diseño: liquidación de productos](design-details-item-application.md)  
[Gestión de costes de inventario](finance-manage-inventory-costs.md)  
[Finanzas](finance.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Glosario de términos de procesos de negocio de Dynamics 365](/dynamics365/guidance/business-processes/glossary)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
