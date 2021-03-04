---
title: Cómo crear una previsión de la demanda
description: Es posible crear previsiones de ventas y producción desde la página **Previsión de la demanda**.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 01/12/2021
ms.author: edupont
ms.openlocfilehash: c009a4d21cac95645edd7b94f22659f155fe6a34
ms.sourcegitcommit: 311e86d6abb9b59a5483324d8bb4cd1be7949248
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/15/2021
ms.locfileid: "5013697"
---
# <a name="create-a-demand-forecast"></a>Crear una previsión de la demanda
Es posible crear previsiones de ventas y producción desde la página **Previsión de la demanda**.  

La funcionalidad de previsión se utiliza para crear la demanda prevista; la demanda real se crea a partir de las ventas y los pedidos de producción. Durante la creación del Programa de producción principal (MPS), la previsión se liquida con las ventas y los pedidos de producción. La opción *Componente* de la previsión determina qué tipo de requisitos se deben tener en cuenta en el proceso de liquidación. Si la previsión es para un producto de venta, sólo se liquidan los pedidos de venta en la previsión. Si es para componentes, sólo se liquida la demanda que depende de los componentes de la orden de producción en la previsión.  

Mediante la previsión, la empresa puede crear escenarios hipotéticos y planificar y satisfacer la demanda con eficacia y rentabilidad. Una previsión exacta puede aumentar significativamente el grado de satisfacción de los clientes en relación con el cumplimiento de fechas y la entrega puntual.  

## <a name="sales-forecasts-and-production-forecasts"></a>Previsiones de ventas y previsiones de producción  
La funcionalidad de previsión de la aplicación se puede usar para crear previsiones de ventas o de producción, juntas o por separado. Por ejemplo, casi todas las empresas que fabrican contra pedido no disponen de existencias de productos terminados, porque cada producto se fabrica cuando se pide. La previsión de pedidos (previsión de ventas) es esencial para lograr unos plazos de producción de los productos terminados razonables (previsión de producción). Por ejemplo, si las piezas de los componentes tienen tiempos de entrega muy largos, y no están pedidas o en existencias, pueden retrasar la producción.  

-   La previsión de ventas es la mejor previsión del departamento del mismo nombre de lo que se va a vender en el futuro, y se determina por producto y por periodo. Con todo, la previsión de ventas no es siempre adecuada para la producción.  
-   La elaboración de previsiones es la proyección del planificador de producción de cuántos productos finales y productos semiterminados derivados se deben producir en cada periodo específico para cubrir las ventas previstas.  

En la mayoría de los casos, el responsable de la planificación de la producción modifica la previsión de ventas para ajustarla a las condiciones de producción, si bien debe satisfacer la previsión de ventas.  

Las previsiones se crean manualmente en la página **Previsión de la demanda**. En el sistema puede haber muchas previsiones, que se distinguen por el nombre y el tipo. Las previsiones se pueden copiar y editar como sea necesario. Tenga en cuenta que, en un momento dado, sólo se puede usar una previsión para realizar la planificación.  

La previsión está formada por una serie de registros, cada uno de los cuales debe tener un número de producto, una fecha de previsión y una cantidad prevista. La previsión de un producto abarca un periodo de tiempo, definido mediante la fecha de previsión y la fecha de previsión del siguiente registro de la previsión. Desde el punto de vista de la planificación, la cantidad prevista debe estar disponible al principio del periodo de demanda.  

Debe calificar una previsión como de *Producto venta*, *Componente* o *Ambos*. El tipo de previsión *Producto venta* se usa en la previsión de ventas. La previsión de producción se crea con el tipo *Componente*. El tipo de previsión *Ambos* sólo se usa para ofrecer al responsable de la planificación una visión general de las previsiones de ventas y de producción. Con esta opción, los movimientos de previsión no se pueden modificar. Mediante la calificación de estos tipos de previsión aquí, puede usar la misma hoja para introducir una previsión de ventas de la misma forma que se introduce una previsión de producción, y usar la misma hoja para ver las dos previsiones a la vez. Tenga en cuenta que el sistema trata los dos tipos de información (ventas y producción) de distinta forma al calcular la planificación, en función de la configuración del producto, la fabricación y la producción.  

## <a name="component-forecast"></a>Previsión de componentes  
La previsión de componentes es una previsión en relación con un producto principal. Puede resultar útil, por ejemplo, si el responsable de la planificación puede estimar la demanda del componente.  

Dado que la previsión de componentes está diseñada para definir las opciones de un producto principal, debe ser igual a o menor que la cantidad prevista del producto de venta. Si la previsión de componentes es mayor que la previsión del producto de venta, el programa considera la diferencia entre los dos tipos de previsión como demanda independiente.  

## <a name="forecasting-periods"></a>Periodos de previsión  
 El periodo de previsión es válido desde la fecha de inicio hasta la fecha de inicio de la siguiente previsión. La página de intervalo de tiempo proporciona muchas opciones para insertar la demanda en una fecha concreta del periodo. Por ello, es aconsejable no cambiar el periodo de previsión salvo que se desee llevar todos los movimientos a la fecha de inicio de este periodo.  

## <a name="forecast-by-locations"></a>Previsión por ubicación  

Puede indicarse en la página **Configuración de fabricación** cómo desea tratar con las ubicaciones que se definen en las previsiones cuando calcula un plan. 

### <a name="use-forecast-by-locations"></a>User previsiones por almacenes

Si elige el campo **Usar pronóstico por ubicación**, entonces [!INCLUDE[prod_short](includes/prod_short.md)] respetará los códigos de ubicación especificados para cada entrada de Previsión de demanda y calculará la previsión restante para cada ubicación.  

Considere este ejemplo: su empresa compra y vende artículos en dos ubicaciones: EAST y WEST. Para ambas ubicaciones, ha configurado una política de reordenación de lote a lote. Crea una previsión para las dos ubicaciones:

- 10 piezas para ubicación EAST
- 4 piezas para ubicación WEST

Luego, crea un pedido de cliente con una cantidad de 12 en la ubicación WEST. El sistema de planificación le sugerirá que haga lo siguiente:

- Reponga 10 piezas para la ubicación EAST, según los datos del pronóstico.  
- Reponga 12 piezas para la ubicación WEST, según la orden de venta. Las 4 piezas que se especificaron en el pronóstico son consumidas por completo por la demanda real de la orden de venta. Para obtener más información, consulte la sección sobre la [reducción de la demanda de previsión por parte de pedidos de venta](design-details-balancing-demand-and-supply.md#forecast-demand-is-reduced-by-sales-orders). 

> [!NOTE]  
>  Si las previsiones en función de las ubicaciones se observan por separado, la previsión global podría no ser representativa.

### <a name="do-not-use-forecast-by-locations"></a>No use previsiones por almacenes
Si deshabilita **Usar pronóstico por ubicación**, entonces [!INCLUDE[prod_short](includes/prod_short.md)] ignorará los códigos de ubicación especificados para cada entrada de Previsión de demanda y agregará las previsiones en una previsión para ubicaciones vacías.  

Considere este ejemplo: su empresa compra y vende artículos en dos ubicaciones: EAST y WEST. Para ambas ubicaciones, ha configurado una política de reordenación de lote a lote. Crea una previsión para las dos ubicaciones:

- 10 piezas para ubicación EAST
- 4 piezas para ubicación WEST

Luego, crea un pedido de cliente con una cantidad de 12 en la ubicación WEST. El sistema de planificación le sugerirá que haga lo siguiente:

- Reponga 12 piezas para la ubicación WEST, según la orden de venta. 
- Reponga 2 piezas para la ubicación vacía. Las 10 y 4 piezas que se especificaron en el pronóstico son consumidas parcialmente por la demanda real de la orden de venta. [!INCLUDE[prod_short](includes/prod_short.md)] ignoró los códigos de ubicación que fueron especificados por el usuario y en su lugar utiliza una ubicación en blanco.

> [!NOTE]  
>  Puede establecer un filtro por ubicaciones, pero es posible que los resultados basados en la ubicación no coincidan con los resultados de la planificación sin filtros.

## <a name="to-create-a-demand-forecast"></a>Para crear una previsión de la demanda

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Previsión de la demanda** y luego elija el enlace relacionado.  
2. Seleccione una previsión en el campo **Nombre previsión demanda** de la ficha desplegable  **General**. Puede haber varias previsiones, que se distinguen por el nombre y el tipo de previsión.  
3. Seleccione el almacén del campo **Filtro almacén** al que se va a aplicar esta previsión.
4. En el campo **Ver por** para cambiar el periodo que se muestra en cada columna. Se pueden seleccionar los siguientes intervalos: **Día**, **Semana**, **Mes**, **Trimestre**, **Año** o el **Periodo contable** configurado en su área financiera.    

> [!NOTE]  
>  Debería analizar qué intervalo de tiempo desea utilizar para futuras previsiones para que sea el mismo en todas las ocasiones. Si especifica una cantidad de previsión, es válida el primer día del intervalo de tiempo seleccionado. Por ejemplo, si selecciona un mes, debe especificar la cantidad prevista en el primer día del mes. Si selecciona un trimestre, debe especificar la cantidad del primer día del primer mes del trimestre.

5. Seleccione cómo se mostrarán las cantidades de previsión del intervalo de tiempo en el campo **Ver como**. Si se selecciona **Saldo periodo**, se mostrará el balance del saldo del periodo. Si se selecciona **Saldo a la fecha**, la página mostrará el saldo del último día del intervalo de tiempo.  
6. En el campo **Tipo previsión**, seleccione **Producto venta**, **Componente** o **Ambos**. Si selecciona **Producto venta** o **Componente**, puede editar la cantidad según el periodo. Si selecciona **Ambos**, no podrá modificar la cantidad, pero podrá elegir el botón de flecha desplegable y ver los movimientos de previsión de la demanda.  
7. Especifique un **Filtro fecha** si desea limitar la cantidad de datos que se muestran.  
8. En la ficha desplegable **Matriz de previsión de demanda**, introduzca las cantidades pronosticadas escribiendo una cantidad en la celda que represente un producto en una fecha o período en particular. Tenga en cuenta que en las celdas vacías, el botón de búsqueda abre una página vacía que indica que debe introducir un valor manualmente.   

> [!NOTE]  
>  También se puede editar una previsión existente. Haga clic en la página **Matriz de previsión de la demanda**, seleccione la acción **Copiar previsión de la demanda** y rellene la página **Previsión de la demanda** con una previsión existente. Es posible realizar modificaciones a las cantidades según sea pertinente.  

## <a name="see-also"></a>Consulte también  
[Configuración de fabricación](production-configure-production-processes.md)  
[Fabricación](production-manage-manufacturing.md)    
[Grupos contables inventario](inventory-manage-inventory.md)  
[Compras](purchasing-manage-purchasing.md)  
[Detalles de diseño: planificación de aprovisionamiento](design-details-supply-planning.md)   
[Procedimientos recomendados de configuración: planificación de suministros](setup-best-practices-supply-planning.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]