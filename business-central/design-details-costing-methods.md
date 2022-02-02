---
title: 'Detalles de diseño: Métodos de coste'
description: En este tema se describe cómo afecta la valoración de existencias si los valores reales y presupuestados se capitalizan y utilizan en el cálculo de costes.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 30, 42, 43
ms.date: 06/14/2021
ms.author: bholtorf
ms.openlocfilehash: 78c69d4849dc7e7687f6bb0cdeb0229baeec1b0c
ms.sourcegitcommit: 1e6addcd6ecc25489fc17388409989440a210895
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/14/2022
ms.locfileid: "7974997"
---
# <a name="design-details-costing-methods"></a>Detalles de diseño: Métodos de coste

La valoración de existencias determina si en el cálculo de costes se capitaliza y utiliza un valor real o uno presupuestado. Junto con la fecha de registro y la secuencia, el método de coste también influye en cómo se registra el flujo de costes.

> [!NOTE]
> No puede modificar la valoración de existencias de un producto si existen movimientos de productos para el producto. Para más información, consulte [Detalles de diseño: cambiar la valoración de exisncias para productos](design-details-changing-costing-methods.md).

En [!INCLUDE[prod_short](includes/prod_short.md)] se admiten las siguientes valoraciones:  

| Método de coste | Descripción | Cuándo se debe usar |
|--|--|--|
| FIFO | El coste unitario de un producto es el valor real de cualquier recepción del producto, seleccionado durante la regla de FIFO.<br /><br /> En la valoración del inventario, se presupone que los primeros productos colocados en el inventario se venden primero. | En entornos empresariales donde el coste de productos es estable.<br /><br /> (Cuando suben los precios, la hoja de balance muestra el valor mayor). Esto significa que las deudas tributarias aumentan, pero las puntuaciones de crédito y capacidad de pedir efectivo prestado mejoran.<br /><br /> En el caso de productos con una vida útil limitada, ya que los productos más antiguos deben venderse antes de que superen su fecha de límite de venta. |
| LIFO | El coste unitario de un producto es el valor real de cualquier recepción del producto, seleccionado durante la regla de LIFO.<br /><br /> En la valoración del inventario, se presupone que los últimos productos colocados en el inventario se venden primero. | No se permite en muchos países o regiones, ya que puede utilizarse para debilitar las ganancias.<br /><br /> (Cuando suben los precios, el valor del balance de ingresos disminuye). Esto significa que las deudas tributarias disminuyen, pero la capacidad de pedir efectivo prestado deteriora. |
| Promedio | El coste unitario de un producto se calcula como el coste unitario medio en cada momento después de una compra.<br /><br /> De la valoración del inventario, se presupone que todos los inventarios se venden simultáneamente. | En entornos empresariales donde el coste de productos es inestable.<br /><br /> Cuando se apilan inventarios o se mezclan y no pueden ser diferenciados, tal como sustancias químicas. |
| Específico | El coste unitario de un producto es el coste exacto en el que la unidad determinada fue recibida. | En producción o comercio de productos fácilmente identificables con costes unitarios relativamente elevados.<br /><br /> En el caso de productos que están sujetos normativas.<br /><br /> Para productos con números de serie. |
| Estándar | El coste unitario de un producto se preestablece basándose en una estimación.<br /><br /> Cuando el coste real se realiza posteriormente, el coste estándar se debe ajustar al coste real a través de valores de varianza. | Cuando el control del coste es crítico.<br /><br /> En fabricación repetitiva para establecer el valor de los costes de material directo, mano de obra directa y gastos de fabricación.<br /><br /> Cuando hay disciplina y personal para mantener los estándares. |

En la imagen siguiente se muestra cómo fluyen los costes a través del inventario por cada valoración de existencias.  

 ![Valoraciones de existencias.](media/design_details_inventory_costing_7_costing_methods.png "Valoraciones de existencias")  

Los métodos de coste varían en cuanto a la forma en que el inventario disminuye y si se utiliza el coste real o el coste estándar como base de valoración. En la tabla siguiente se explican las diferentes características. (Se excluye el método LIFO por ser muy parecido al método FIFO).  

|Categoría|FIFO|Promedio|Estándar|Específico|  
|-|----------|-------------|--------------|--------------|  
|Característica general|Fácil de comprender|Basándose en opciones de periodo: **Día**/**Semana**/**Mes**/**Trimestre**/**Periodo contable**.<br /><br /> Se puede calcular por producto o por producto, almacén y variante.|Fácil de usar pero requiere mantenimiento cualificado.|Requiere el seguimiento de producto en la transacción de entrada y de salida.<br /><br /> Normalmente se usa para productos serializados.|  
|Aplicación/ajuste|La aplicación hace un seguimiento de **la cantidad pendiente**.<br /><br /> El ajuste desvía los costes según la liquidación de la cantidad.|La aplicación hace un seguimiento de la **cantidad pendiente**.<br /><br /> Los costes se calculan y se envían por la **fecha de valoración**.|La aplicación hace un seguimiento de la **cantidad pendiente**.<br /><br /> La aplicación se basa en el método FIFO.|Toda las liquidaciones son fijas.|  
|Revaluación|Revaloriza solo la cantidad facturada.<br /><br /> Se puede hacer por producto o por movimiento de producto.<br /><br /> Se puede realizar retroactivamente.|Revaloriza solo la cantidad facturada.<br /><br /> Se puede hacer solo por producto.<br /><br /> Se puede realizar retroactivamente.|Revaloriza las cantidades facturadas y no facturadas.<br /><br /> Se puede hacer por producto o por movimiento de producto.<br /><br /> Se puede realizar retroactivamente.|Revaloriza solo la cantidad facturada.<br /><br /> Se puede hacer por producto o por movimiento de producto.<br /><br /> Se puede realizar retroactivamente.|  
|Varios|Si se especifica una fecha retroactiva para una salida de existencias, las entradas existentes NO se volverán a liquidar para proporcionar un flujo correcto FIFO del coste.|Si se retrocede la fecha de una entrada o una salida del inventario, se vuelve a calcular el coste medio y se ajustan todos los registros afectados.<br /><br /> Si cambia el periodo o el tipo de cálculo, todos los registros afectados deben ajustarse.|Utilice la página **Hoja de trabajo estándar** para actualizar y distribuir periódicamente los costes estándar.<br /><br /> NO se admite por UA.<br /><br /> No existe ningún registro histórico para los costes estándar.|Puede utilizar el seguimiento de producto específico sin usar la valoración de existencias Específica. El coste NO seguirá el número de lote, sino el coste supuesto de la valoración de existencias seleccionada.|  

## <a name="example"></a>Ejemplo

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

### <a name="effect-of-costing-methods-on-valuing-inventory-increases"></a>Efecto de los métodos de coste en la valoración de entrada de existencias

- **FIFO**/**LIFO**/**Promedio**/**Específico**  

    En el caso de productos con métodos de coste que utilizan el coste real como base de valoración (**FIFO**, **LIFO**, **Promedio** o **Específico**), las entradas de existencias se calculan según el coste de compra del producto.  

    En la tabla siguiente se muestra cómo se valoran las entradas de existencias para todas las valoraciones de existencias excepto **Estándar**.  

    |Fecha registro|Cantidad|Importe coste (Real)|Nº mov.|  
    |------------------|--------------|----------------------------|---------------|  
    |01-01-20|1|10.00|1|  
    |01-01-20|1|20,00|2|  
    |01-01-20|1|30,00|3|  

- **Estándar**  

    En el caso de productos donde se use el método de costes **Estándar**, las entradas de existencias se calculan según el coste estándar actual.  

    En la tabla siguiente se muestra cómo se valoran las entradas de existencias para la valoración de existencias **Estándar**.  

    |Fecha registro|Cantidad|Importe coste (Real)|Nº mov.|  
    |------------------|--------------|----------------------------|---------------|  
    |01-01-20|1|15.00|1|  
    |01-01-20|1|15.00|2|  
    |01-01-20|1|15.00|3|  

### <a name="effect-of-costing-methods-on-valuing-inventory-decreases"></a>Efecto de los métodos de coste en la valoración de salidas de existencias

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
    |------------------|--------------|----------------------------|---------------|  
    |01-02-20|-1|-30,00|4|  
    |01-03-20|-1|-20,00|5|  
    |01-04-20|-1|-10,00|6|  

- **Promedio**  

    En el caso de productos que usen el método de coste **Promedio**, las salidas de existencias se valoran calculando un promedio ponderado del inventario que queda en el último día del periodo de coste medio en el cual se ha registrado una salida de existencias. Para obtener más información, consulte [Detalles de diseño: Coste medio](design-details-average-cost.md).  

    En la tabla siguiente se muestra cómo se valoran las salidas de existencias para la valoración de existencias **Media**.  

    |Fecha registro|Cantidad|Importe coste (Real)|Nº mov.|  
    |------------------|--------------|----------------------------|---------------|  
    |01-02-20|-1|-20,00|4|  
    |01-03-20|-1|-20,00|5|  
    |01-04-20|-1|-20,00|6|  

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

## <a name="see-also"></a>Consulte también

[Detalles de diseño: Coste de inventario](design-details-inventory-costing.md)   
[Detalles de diseño: Desviación](design-details-variance.md)   
[Detalles de diseño: Coste medio](design-details-average-cost.md)   
[Detalles de diseño: Liquidación de productos](design-details-item-application.md)  
[Gestión de costes de inventario](finance-manage-inventory-costs.md)  
[Finanzas](finance.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]