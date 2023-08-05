---
title: Replanificar o actualizar órdenes de producción directamente
description: Este tema describe los procedimientos sobre cómo replanificar órdenes de producción y actualizar órdenes de producción directamente.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '99000842, 99000843, 99000861, 99000862, 99000863'
ms.date: 06/25/2021
ms.author: edupont
---
# Replanificar o actualizar órdenes de producción directamente

Se utiliza normalmente la función **Replanificar** después de haber agregado o cambiado componentes que conforman órdenes de producción subyacentes. La función de planificación calcula los cambios realizados en las líneas de componentes y rutas e incluye a los productos de los niveles de L.M. de producción inferiores, para los que puede crear nuevas órdenes de producción.  

De acuerdo con los cambios realizados en las líneas de componentes y rutas, la función de replanificación calcula y planifica la nueva demanda de la orden de producción.  

La función **Actualizar** en órdenes de producción se utiliza normalmente después de que se haya hecho una de las siguientes opciones:

- Se crea manualmente una cabecera de orden de producción para calcular y crear por primera vez los datos de las líneas.
- Se realizan cambios en la cabecera de la orden de producción para volver a calcular los datos de las líneas.

La función de actualizar calcula los cambios realizados en una cabecera de orden de producción sin que resulten afectados los niveles de L.M. de producción. La función calcula e inicia los valores de las líneas de componentes y de ruta basada en los datos maestros definidos en la L.M. de producción asignada y la ruta, de acuerdo con la cantidad a solicitar y la fecha de vencimiento de la cabecera de la orden de producción.

Puede insertar las líneas de la orden de producción manualmente o utilizar la función que calcula las líneas desde la cabecera.  

> [!NOTE]
> Si utiliza la función Actualizar para recalcular las líneas de orden de producción, se eliminan las líneas antiguas y se calculan las nuevas.  

## Para replanificar una orden de producción

1. Elija el icono ![Bombilla que abre la función Dígame 1.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **O.P. Planificadas en firme** y, a continuación, elija el vínculo relacionado.  
2. Abra la orden de producción que desea replanificar.  
3. En la ficha desplegable **Líneas**, elija la acció **Líneas** y, a continuación **Componentes**.  
4. Agregue un componente que sea un producto fabricado o un producto semiterminado.  
5. Desde la orden de producción, seleccione la acción **Replanificar**.  

    En la página **Replanificar orden de producción**, defina cómo y qué se va a replanificar.  
6. En el campo **Dirección programación**, seleccione una de las siguientes opciones.  

    | Opción | Description |
    |--|--|
    | **Atrás** | Calcula la secuencia de la operación hacia atrás desde la primera fecha final posible, definida por la fecha de vencimiento u otras órdenes programadas, hasta la última fecha inicial posible. **Nota**: esta opción predeterminada es la que se utiliza en la mayoría de las situaciones. |
    | **Anticipada** | Calcula la secuencia de la operación hacia delante desde la última fecha inicial posible, definida por la fecha de vencimiento u otras órdenes programadas, hasta la primera fecha final posible. **Nota**: Esta opción sólo se utiliza para pedidos urgentes. |

7. En el campo **Planificar**, indique si desea calcular las necesidades de producción para los productos fabricados en la L.M. de producción, como se detalla a continuación.  

    |Opción|Description|  
    |----------------------------------|---------------------------------------|  
    |**Sin niveles**|No tenga en cuenta la producción de niveles inferiores. Esta opción sólo actualiza el programa del producto, como Actualizar.|  
    |**Un nivel**|Planificar la demanda de producción del primer nivel. Se pueden crear órdenes de producción de primer nivel.|  
    |**Todos los niveles**|Planificar la demanda de producción de todos los niveles. Se pueden crear órdenes de producción de todos los niveles.|  

8. Seleccione **Un nivel** y elija el botón **Aceptar** para replanificar la orden de producción, y calcular y crear una nueva orden subyacente para el producto semiterminado incluido, si no está totalmente disponible.  

> [!NOTE]  
> Es muy probable que los cambios realizados con la función **Replanificar** modifiquen la necesidad de capacidad de la orden de producción y que, por tanto, tenga que reprogramar las operaciones a continuación.  

## Para actualizar una orden de producción

Si ha modificado líneas de orden de producción, componentes o líneas de ruta, debe también actualizar la información en la orden de producción. En siguiente procedimiento, se calculan los componentes para una orden de producción planificada en firme. Los pasos son parecidos para las líneas de ruta.

1. Elija el icono ![Bombilla que abre la función Dígame 2.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Orden produc. planif. en firme** y, a continuación, elija el vínculo relacionado.  
2. Seleccione la acción **Nuevo**. Para obtener más información, consulte [Crear órdenes de producción](production-how-to-create-production-orders.md).  
3. Seleccione la acción **Actualizar**.
4. En la página **Actualizar orden de producción**, seleccione una de las siguientes opciones:

    |Campo|Opción|Descripción|  
    |----------------------------------|---------------|---------------------------------------|  
    |**Dirección programación**|**Anticipada**|La programación empieza en la fecha inicial y avanza hasta la fecha final. Debe rellenar la fecha inicial para utilizar esta opción.|  
    ||**Atrás**|La programación empieza en la fecha final y retrocede hasta la fecha inicial.|  
    |**Calcular**|**Líneas**|Seleccione este campo para calcular las líneas del orden de producción.|  
    ||**Rutas**|Este campo no tiene influencia en el cálculo de las líneas de producción.|  
    ||**Nec. componente**|Este campo no tiene influencia en el cálculo de las líneas de producción.|  
    |**Almacén**|**Crear solicitud de entrada**|Este campo no tiene influencia en el cálculo de las líneas de producción.|  

5. Elija el botón **Aceptar** para confirmar la selección. Se han calculado las líneas de la orden de producción.

> [!NOTE]  
> El cálculo de los componentes de la orden de producción elimina cambios realizados anteriormente en los mismos.

## Consulte también

[Planificación](production-planning.md)  
[Configuración de fabricación](production-configure-production-processes.md)  
[Fabricación](production-manage-manufacturing.md)    
[Grupos contables inventario](inventory-manage-inventory.md)  
[Compras](purchasing-manage-purchasing.md)  
[Detalles de diseño: planificación de aprovisionamiento](design-details-supply-planning.md)   
[Procedimientos recomendados de configuración: planificación de suministros](setup-best-practices-supply-planning.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]