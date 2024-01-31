---
title: 'Detalles de diseño: coste medio'
description: El costo medio de un artículo se calcula con una media ponderada periódica.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.search.form: '8645,'
ms.date: 06/06/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Detalles de diseño: coste medio

El costo medio de un artículo se calcula con una media ponderada periódica. La media se basa en el período de coste medio que se configura en [!INCLUDE[prod_short](includes/prod_short.md)].  

La fecha de valoración se establece automáticamente.  

## Configurar el cálculo del coste medio

En la tabla siguiente se describen los dos campos de la página **Configuración de inventario** que se deben rellenar para habilitar el cálculo de coste medio.  

|Campo|Descripción|  
|---------------------------------|---------------------------------------|  
|**Periodo coste medio**|Especifica en qué periodo se calcula el coste medio. Las siguientes opciones están disponibles:<br /><br /> - **Día**<br />- **Semana**<br />- **Mes**<br />- **Periodo contable**<br /><br /> Reducciones en inventario que se registraran en el periodo de coste medio reciben el coste medio calculado para dicho periodo.|  
|**Tipo cálculo cte. medio**|Especifica cómo se calcula el coste medio. Las siguientes opciones están disponibles:<br /><br /> - **Producto**<br />- **Producto, variante y almacén**<br /> Con esta opción, se calcula el coste medio por cada producto, por cada ubicación y por cada variante del producto. El coste medio de este producto dependerá de dónde se encuentre almacenado y de la variante que seleccione, por ejemplo, el color.|  

> [!NOTE]  
> Solo puede usar un periodo de coste medio y un tipo de coste medio en un ejercicio.  
>
> La página **Pedidos contables** muestra el periodo de coste medio y el tipo de cálculo de coste medio que está en vigor durante ese periodo, por cada periodo contable.  

## Cálculo de coste promedio

 Cuando se registra una transacción para un producto que utiliza el método de valoración de existencias Medio, se crea un movimiento en la tabla **Punto de entrada aj. coste promedio**. Este movimiento contiene el número de producto, el código de variante y el código de almacén de la transacción. El movimiento también contiene el campo **Fecha valoración**, el cual especifica la última fecha del periodo de coste medio en la que se registró la transacción.  

> [!NOTE]  
> Este campo no se debe confundir con el campo **Fecha valoración** de la tabla **Movimiento valor**, que muestra la fecha en la que el valor surte efecto y se usa para determinar el periodo de coste medio al que corresponde el movimiento de valoración.  

 El coste medio de una transacción se calcula al ajustar el coste del producto. Para obtener más información, consulte [Detalles de diseño: Ajuste de coste](design-details-cost-adjustment.md). Un ajuste de costes utiliza los movimientos de la tabla **Punto de entrada aj. coste promedio** para identificar para qué productos (o productos, almacenes y variantes) se deben calcular los costes medio. Para cada movimiento cuyo coste no se haya ajustado aún, el ajuste de coste realiza lo siguiente para determinar el coste medio:  

- Determinar el coste del producto al comienzo del periodo de coste medio.  
- Añade la suma de los costes de entrada que fueron registrados durante el periodo de coste medio. Esto incluye las compras, las devoluciones de venta, los ajustes positivos y las salidas de producción y ensamblado.  
- Resta la suma de los costes de cualquier transacción saliente que se aplicaron de forma fija a las recepciones del periodo de coste medio. Estas suelen incluir las devoluciones de compra y las salidas negativas.  
- Divide por la cantidad total del inventario para la fecha final del periodo de coste medio. Excluye salidas de existencias que se están valorando.  

 El programa aplica el coste medio calculado a las salidas de existencias del elemento (producto, almacén o variante) con fechas de registro durante el periodo de coste medio. Para las salidas de existencias que se aplican de forma fija a salidas de existencias en el periodo de coste medio, [!INCLUDE [prod_short](includes/prod_short.md)] reenvía el coste medio calculado desde la entrada a la salida.  

### Ejemplo: Periodo de coste medio = Día

En el ejemplo siguiente se muestra el efecto de calcular el coste medio basado en un periodo de coste medio de un día. El campo **Tipo cálculo cte. medio** en la página **Configuración de inventario** está configurado en **Producto**.  

En la tabla siguiente se muestran los movimientos de producto del producto del coste medio de muestra, ITEM1, antes de que se haya ejecutado el proceso **Valorar stock - movs. producto**.  

| **Fecha reg.** | **Tipo mov. producto** | **Cantidad** | **Importe coste (Real)** | **N.º de movimiento** |
|--|--|--|--|--|
| 01-01-23 |   Compra | 1 | 20.00 | 1 |
| 01-01-23 |   Compra | 1 | 40.00 | 2 |
| 01-01-23 |   Venta | -1 | -20,00 | 3 |
| 02-01-23 |   Venta | -1 | -40,00 | 4 |
| 02-02-23 |   Compra | 1 | 100.00 | 5 |
| 02-03-23 |   Venta | -1 | -100,00 | 6 |

> [!NOTE]  
> Al no haberse producido aún el ajuste del coste, los valores del campo **Importe coste (real)** del inventario disminuyen según las entradas de existencias a las que se aplican.  

 En la tabla siguiente se muestran los movimientos en la tabla **Punto de entrada aj. coste promedio** que se aplican a los movimientos de valor que son el resultado de los movimientos de producto en la tabla anterior.  

| **N.º producto** | **Cód. variante** | **Código de almacén** | **Fecha valoración** | **Coste ajustado** |
|--|--|--|--|--|
| PROD1 |  | AZUL | 01-01-23 |   No |
| PROD1 |  | AZUL | 02-01-23 |   No |
| PROD1 |  | AZUL | 02-02-23 |   No |
| PROD1 |  | AZUL | 02-03-23 |   No |

 En la tabla siguiente se muestran los mismos movimientos de producto después de que se haya ejecutado el proceso **Valorar stock - movs. producto**. Se calcula el coste medio por día y se aplica a las salidas de existencias.  

| **Fecha reg.** | **Tipo mov. producto** | **Cantidad** | **Importe coste (Real)** | **N.º de movimiento** |
|--|--|--|--|--|--|
| 01-01-23 |   Compra | 1 | 20.00 | 1 |
| 01-01-23 |   Compra | 1 | 40.00 | 2 |
| 01-01-23 |   Venta | -1 | -30,00 | 3 |
| 02-01-23 |   Venta | -1 | -30,00 | 4 |
| 02-02-23 |   Compra | 1 | 100.00 | 5 |
| 02-03-23 |   Venta | -1 | -100,00 | 6 |

### Ejemplo: Periodo de coste medio = Mes

 En este ejemplo se muestra el efecto de calcular el coste medio basado en un periodo de coste medio de un mes. El campo **Tipo cálculo cte. medio** en la página **Configuración de inventario** está configurado en **Producto**.  

 Si el periodo de coste medio es un mes, [!INCLUDE [prod_short](includes/prod_short.md)] crea una entrada para cada combinación de número de producto, código de variante, código de almacén y fecha de valoración.  

 En la tabla siguiente se muestran los movimientos de producto del producto del coste medio de muestra, ITEM1, antes de que se haya ejecutado el proceso **Valorar stock - movs. producto**.  

| **Fecha reg.** | **Tipo mov. producto** | **Cantidad** | **Importe coste (Real)** | **N.º de movimiento** |
|--|--|--|--|--|
| 01-01-23 |   Compra | 1 | 20.00 | 1 |
| 01-01-23 |   Compra | 1 | 40.00 | 2 |
| 01-01-23 |   Venta | -1 | -20,00 | 3 |
| 02-01-23 |   Venta | -1 | -40,00 | 4 |
| 02-02-23 |   Compra | 1 | 100.00 | 5 |
| 02-03-23 |   Venta | -1 | -100,00 | 6 |

> [!NOTE]  
> Al no haberse producido aún el ajuste del coste, los valores del campo **Importe coste (real)** del inventario disminuyen según las entradas de existencias a las que se aplican.  

En la tabla siguiente se muestran los movimientos en la tabla **Punto de entrada aj. coste promedio** que se aplican a los movimientos de valor que son el resultado de los movimientos de producto en la tabla anterior.  

| **N.º producto** | **Cód. variante** | **Código de almacén** | **Fecha valoración** | **Coste ajustado** |
|--|--|--|--|--|
| PROD1 |  | AZUL | 01-31-23 |   No |
| PROD1 |  | AZUL | 02-28-23 |   No |

> [!NOTE]  
> La fecha de valoración se establece como el último día del periodo de coste medio, que, en este caso, es el último día del mes.  

En la tabla siguiente se muestran los mismos movimientos de producto después de que se haya ejecutado el proceso **Valorar stock - movs. producto**. Se calcula el coste medio por mes y se aplica a las salidas de existencias.  

|**Fecha reg.** | **Tipo mov. producto** | **Cantidad** | **Importe coste (Real)** | **N.º de movimiento** |
|--|--|--|--|--|
| 01-01-23 | Compra | 1 | 20.00 | 1 |
| 01-01-23 | Compra | 1 | 40.00 | 2 |
| 01-01-23 | Venta | -1 | -30,00 | 3 |
| 02-01-23 | Venta | -1 | -65,00 | 4 |
| 02-02-23 | Compra | 1 | 100.00 | 5 |
| 02-03-23 | Venta | -1 | -65,00 | 6 |

El costo medio de la entrada número 3 se calcula en el período de coste medio de enero. El costo medio de las entrada 4 y 6 se calcula en el período de coste medio de febrero.  

Para obtener el coste medio para febrero, [!INCLUDE [prod_short](includes/prod_short.md)] agrega el coste medio del producto recibido en el inventario (100,00) se suma al coste medio al comienzo del periodo (30,00). La suma (130,00) luego se divide por la cantidad total en el inventario (2). Este cálculo da el coste medio resultante del producto en el período de febrero (65,00). El programa asigna dicho coste medio a las salidas de existencias ocurridas en el periodo (entradas 4 y 6).  

## Definición de la fecha de valoración

 El campo **Fecha valoración** de la tabla **Movimiento valor** determina a qué periodo de coste medio pertenece un movimiento de salida de existencias. Este ajuste también se aplica al inventario de trabajo en curso.  

 En la tabla siguiente se muestran los criterios que se usan para establecer la fecha de valoración.  

| Caso | Fecha reg. | Cdad. valorada | Reevaluación | Fecha valoración |
|--|--|--|--|--|
| 1 |  | Positivo | No | Fecha de registro del movimiento de producto |
| 2 | Posterior a la última fecha de valoración de los movimientos de valoración aplicados | Negativo | No | Fecha de registro del movimiento de producto |
| 3 | Anterior a la última fecha de valoración de los movimientos de valorización aplicados | Positivo | No | Última fecha de valoración de los movimientos de valoración aplicados |
| 4 |  | Negativo | Sí | Fecha de registro del movimiento de valoración de revalorización |

### Ejemplo

En la siguiente tabla de movimientos de valoración se ilustran los distintos escenarios.  

| Caso | Fecha reg. | Tipo mov. producto | Fecha valoración | Cdad. valorada | Importe coste (real) | N.º mov. producto | N.º de movimiento |
|--|--|--|--|--|--|--|--|
| 1 | 01-01-20 | Compra | 01-01-20 | 2 | 20.00 | 1 | 1 |
| 2 | 15-01-20 | (Cargo de producto) | 01-01-20 | 2 | 8.00 | 1 | 2 |
| 3 | 01-02-20 | Venta | 01-02-20 | -1 | -14,00 | 2 | 3 |
| 4 | 01-03-20 | (Revalorización) | 01-03-20 | 1 | -.4,00 | 1 | 4 |
| 5 | 01-02-20 | Venta | 01-03-20 | -1 | -10,00 | 3 | 5 |

> [!NOTE]  
> En el número de movimiento 5 en la tabla anterior, el usuario ha introducido un pedido de venta con una fecha de registro (01-02-20) anterior a la fecha de última valoración de las entradas de valor aplicadas (01-03-20). Si el valor correspondiente en el campo **Importe coste (real)** para esta fecha (02-01-20) se usara para este registro, sería 14,00. Esto provocaría una situación en la que la cantidad de existencias es cero, pero el valor de inventario es -4,00.  
>
> Para evitar una discordancia de cantidad-valor, la fecha de valoración se establece en igual que la última fecha de valoración de los movimientos de valoración liquidados (01-03-20). El valor del campo **Importe coste (real)** se convierte en 10,00 (después de la revalorización), lo que significa que la cantidad de existencias es cero y el valor de inventario también es cero.  

> [!CAUTION]  
> Dado que el informe **Valoración inventario** se basa en la fecha de registro, el informe reflejará cualquier discordancia de cantidad y valor en supuestos como el ejemplo anterior. Para obtener más información, consulte [Detalles de diseño: Valoración de inventario](design-details-inventory-valuation.md).  

Si la cantidad en el inventario es menor que cero después de registrar la salida de existencias, la fecha de valoración se establece en la fecha de registro de la salida de existencias. Esta fecha se puede modificar cuando se aplica la entrada de existencias, según las reglas descritas en la nota anteriormente en esta sección.  

## Nuevo cálculo de coste promedio

Valorar las salidas de existencias como media ponderada sería sencillo en varios escenarios:

- Las compras siempre se facturan antes que las ventas.
- Los registros nunca tienen una fecha anterior.
- Nunca se cometen errores.

Sin embargo, la realidad es diferente.  

Tal como se muestra en los ejemplos en este artículo, la fecha de valoración se define como la fecha a partir de la cual la entrada de valor se incluye en el cálculo del coste medio. Esta configuración le permite hacer varias cosas para producto con la valoración de existencias Media:  

- Facturar la venta de un producto antes de facturar su compra.  
- Especificar fecha retroactiva para un registro.  
- Recuperar un registro erróneo.  

> [!NOTE]  
> Otro motivo de esta flexibilidad es la liquidación fija. Para obtener más información acerca de la liquidación fija, consulte [Detalles de diseño: Liquidación de productos](design-details-item-application.md).  

Esta flexibilidad puede obligar a volver a calcular el coste medio después de haberse producido el registro. Por ejemplo, si registra una entrada o una salida de existencias con una fecha de valoración anterior a una salida de existencias. El recálculo del coste medio se producirá automáticamente cuando ejecute el proceso **Valorar stock - movs. producto**, manual o automáticamente.  

Puede cambiar la base de valoración del inventario dentro de un periodo contable si se modifican los valores de los campos **Periodo coste medio** y **Tipo cálculo cte. medio**. Sin embargo, le recomendamos que tenga cuidado y consulte a su auditor.  

### Ejemplo de coste medio recalculado

Este ejemplo muestra cómo [!INCLUDE [prod_short](includes/prod_short.md)] recalcula el coste medio cuando se registra en una fecha anterior a una salida de existencias. El ejemplo se basa en el periodo de coste medio de **Día**.  

En la tabla siguiente se muestran los movimientos de valoración que hay para el producto antes de que se haya introducido el registro.  

| Fecha valoración | Cantidad | Importe coste (real) | N.º de movimiento |
|--|--|--|--|
| 01-01-20 | 1 | 10.00 | 1 |
| 02-01-20 | 1 | 20.00 | 2 |
| 15-02-20 | -1 | -15,00 | 3 |
| 16-02-20 | -1 | -15,00 | 4 |

El usuario registra una entrada de existencias (movimiento número 5) con una fecha de valoración (03-01-20) que es anterior a una salida de existencias. Para equilibrar el inventario, se debe recalcular el coste medio y ajustarlo a 17,00.  

En la tabla siguiente se muestran los movimientos de valoración que hay para el producto después de que se haya introducido el movimiento número 5.  

| Fecha valoración | Cantidad | Importe coste (real) | N.º de movimiento |
|--|--|--|--|
| 01-01-20 | 1 | 10.00 | 1 |
| 02-01-20 | 1 | 20.00 | 2 |
| 03-01-20 | 1 | 21.00 | 5 |
| 15-02-20 | -1 | -17,00 | 3 |
| 16-02-20 | -1 | -17,00 | 4 |

## Consulte también

[Detalles de diseño: coste de inventario](design-details-inventory-costing.md)  
[Detalles de diseño: métodos de coste](design-details-costing-methods.md)  
[Detalles de diseño: ajuste de coste](design-details-cost-adjustment.md)  
[Detalles de diseño: liquidación de productos](design-details-item-application.md)  
[Gestión de costes de inventario](finance-manage-inventory-costs.md)  
[Finanzas](finance.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Glosario de términos de procesos de negocio de Dynamics 365](/dynamics365/guidance/business-processes/glossary)  
[Definir resumen de costes de productos y servicios](/dynamics365/guidance/business-processes/product-service-define-cost-overview)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
