---
title: Obtener un resumen de disponibilidad
description: Puede obtener información sobre la disponibilidad de los productos o existencias en distintos almacenes, por eventos de venta o de compra, por un periodo de tiempo, etc.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: overview
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: stock
ms.date: 06/16/2021
ms.author: edupont
ms.openlocfilehash: 5a65e56a58f0224230770dd9d2c847b754125d20
ms.sourcegitcommit: 8464b37c4f1e5819aed81d9cfdc382fc3d0762fc
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/19/2022
ms.locfileid: "8012320"
---
# <a name="view-the-availability-of-items"></a>Consultar la disponibilidad de los productos
En el contexto de una tarea de negocio, puede obtener la información avanzada acerca de cuándo y dónde está disponible un producto, por ejemplo, al hablar con un cliente sobre una fecha de entrega.

Puede consultar la disponibilidad de todos los productos por ubicación y puede consultar la disponibilidad de cada producto por evento o por periodo también. Un evento es cualquier transacción de producto programada, como un albarán de venta o un albarán de transferencia de entrada.

> [!NOTE]  
>   Las vistas de disponibilidad por ubicación requieren que se mantenga el inventario en varias ubicaciones. Para obtener más información, consulte [Configurar ubicaciones](inventory-how-setup-locations.md).

Si utiliza la funcionalidad de almacén, la disponibilidad varía en función de las asignaciones en el nivel de ubicación cuando tienen lugar actividades de almacén, como selección y movimientos, y cuando el programa de reservas de inventario impone restricciones. Un algoritmo bastante complejo comprueba que todas las condiciones se cumplan antes de asignar cantidades a selecciones para los flujos de salida. Para obtener más información, consulte [Detalles de diseño: Disponibilidad en el almacén](design-details-availability-in-the-warehouse.md).

En [!INCLUDE[prod_short](includes/prod_short.md)], las cifras de disponibilidad normalmente se muestran en dos campos diferentes, cada uno con una definición distinta:

* El campo **Cantidad disponible**, en algunas parte se denomina **Inventario**, muestra la cantidad real hoy de acuerdo con los movimientos de producto registrados.
* El campo **Saldo disponible estimado** calcula y muestra el stock disponible más las recepciones programadas menos las necesidades brutas. (En [!INCLUDE[prod_short](includes/prod_short.md)], las recepciones programadas incluyen cantidades en los pedidos de compra y pedidos de transferencia de entrada. Las necesidades brutas incluyen cantidades de los pedidos de venta y los pedidos de transferencia de salida).

> [!TIP]  
>   El saldo disponible estimado es muy relevante consultarlo en las páginas **Existencias producto** y **Disponibilidad prod. por evento** porque contienen la dimensión de fecha.  

> [!NOTE]  
>   Los procedimientos siguientes describen cómo ver la información de disponibilidad avanzada de la lista de productos y la ficha de producto. También puede tener acceso a la información de las líneas del documento de venta, correspondiente al producto de la línea. Para obtener más información, vea [Vender productos](sales-how-sell-products.md).

## <a name="to-view-the-availability-of-an-item-according-to-when-it-will-be-received-or-shipped"></a>Para consultar la disponibilidad de un producto según cuándo se recibirá o enviará
Puede ver la disponibilidad de un producto según las transacciones de producto programadas en la página **Disponibilidad por evento**.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Productos**, y luego elija el enlace relacionado.
2. Abra la ficha de un producto del que quiera ver su disponibilidad.
3. Elija la acción **Disponibilidad prod. por** y, a continuación, elija la acción **Evento**.

    La página **Disponibilidad prod. por evento** muestra cómo la cantidad de existencias del producto se desarrollará con el tiempo según los eventos programados de envío y recepción. La página proporciona una vista condensada que muestra una línea de información acumulada por el intervalo de tiempo en el que cambian las cantidades de inventario. Los intervalos de tiempo en que no se ha producido ningún evento no se muestran. Puede expandir cada línea para consultar información acerca del evento o los eventos que causaron la cantidad acumulada en la línea.
4. Elija el valor en el campo **Saldo disponible estimado** para ver los movimientos de productos o documentos abiertos que constituyen el valor.

## <a name="to-view-the-availability-of-an-item-in-different-periods"></a>Para consultar la disponibilidad de un producto en distintos periodos
Puede ver la disponibilidad de un producto a lo largo del tiempo para periodos de tiempo específicos en la página **Existencias producto**.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Productos**, y luego elija el enlace relacionado.
2. Abra la ficha de un producto del que quiera ver su disponibilidad.
3. Elija la acción **Disponibilidad prod. por** y, a continuación, elija la acción **Periodo**.

    La página **Existencias producto** muestra cómo la cantidad de existencias del producto se desarrollarán a lo largo del tiempo, lo que se muestra para un periodo seleccionado, por ejemplo día, semana o trimestre.
4. Elija el valor en el campo **Saldo disponible estimado** para ver los movimientos de productos o documentos abiertos que constituyen el valor.

## <a name="to-view-the-availability-of-an-item-at-the-locations-where-it-is-stored"></a>Para consultar la disponibilidad de un producto en las ubicaciones donde se almacena
Puede ver la disponibilidad de un producto en distintos sitios donde se almacena en la página **Disponib. prod. por almacén**.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Productos**, y luego elija el enlace relacionado.
2. Abra la ficha de un producto del que quiera ver su disponibilidad.
3. Elija la acción **Disponibilidad prod. por** y, a continuación, elija la acción **Almacén**.

    La página **Disponib. prod. por almacén** muestra cómo la cantidad de existencias del producto se desarrollará en el futuro, mostrando cada almacén donde se almacena.
4. Elija el valor en el campo **Cantidad física disponible** para ver los movimientos de productos que constituyen el valor.
5. Elija el valor en el campo **Saldo disponible estimado** para ver los movimientos de productos o documentos abiertos que constituyen el valor.

## <a name="to-view-the-availability-of-all-items-by-the-location-where-they-are-stored"></a>Para consultar la disponibilidad de todos los productos en las ubicaciones donde se almacenan
Puede ver la disponibilidad de todos sus productos en todas sus ubicaciones en la página **Productos por almacén**.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Productos**, y luego elija el enlace relacionado.
2. Elija la acción **Productos por almacén**.

    La página **Productos por almacén** muestra la cantidad de todos sus productos que hay disponible en cada ubicación.
3. Elija el valor en el campo **Cantidad física disponible** para ver los movimientos de productos que constituyen el valor.

## <a name="to-view-the-availability-of-an-item-by-its-use-in-assembly-or-production-boms"></a>Para consultar la disponibilidad de un producto por su uso en las L.M. de ensamblado o producción
Si un producto forma parte de las L.M. de ensamblado o producción, como producto principal o como componente, puede ver cuántas unidades se requieren en la página **Disponibilidad producto por nivel L.M.**. La página muestra cuántas unidades de un producto principal se pueden producir según la disponibilidad de productos secundarios en las líneas subyacentes. Cualquier producto cuya L.M. de ensamblado o producción se muestre en la página como una línea contraíble. Puede expandir esta línea para ver los componentes subyacentes y subconjuntos de nivel inferior con sus propias L.M.

Por ejemplo, puede utilizar la página para determinar si puede completar una pedido de venta para un producto en una fecha especificada consultando su disponibilidad actual en y las cantidades que sus componentes pueden suministrar. También puede utilizar la página para especificar los cuellos de botella en las L.M. relacionadas.

En cada línea de la página para los productos principales y los productos secundarios, los siguientes campos de clave especifican las cifras de disponibilidad. Puede usar estas cifras para comprometer cuántas unidades de un producto principal puede suministrar si inicia el proceso de ensamblado relacionado.

|Campo|Descripción|
|------|-----------|
|**Puede hacer elemento primario**|Muestra cuántas unidades de cualquier producto semiterminado del producto superior puede producir. El campo especifica cuántas unidades principales inmediatas puede ensamblar. El valor se basa en la disponibilidad del producto de la línea.|
|**Puede hacer prod. ppal.**|Muestra cuántas unidades del producto superior puede producir. El campo especifica cuántas unidades del producto de la L.M. de la línea superior puede ensamblar. El valor se basa en la disponibilidad del producto de la línea.|

### <a name="to-view-the-availability-of-an-item-according-to-demand-for-its-parent"></a>Para ver la disponibilidad de un producto según la demanda para su principal
La página **Disponibilidad prod. por nivel L.M.** muestra información acerca del producto de la línea de ficha o documento para el que se ha abierto la página. El producto siempre se muestra en la línea superior. Puede ver la información de otros productos o de todos los productos cambiando el valor del campo **Filtro producto**.

> [!NOTE]  
>   De forma predeterminada, las cifras de disponibilidad de las líneas muestran la disponibilidad total de todos los productos bajo el producto superior. Estas cifras se muestran en el campo **Cdad. disponible**, y el foco está en el producto superior. Sin embargo, la información de cuántos productos semiterminados puede producir puede estar desviada. Para obtener una indicación verdadera de cuántos de los productos semiterminados mostrados puede producir, debe desactivar la casilla **Mostrar disponibilidad total** y después consultar la cifra en el campo **Puede hacer elemento primario**.

El campo **Cuello de botella** especifica qué producto de una estructura de L.M. le impide producir una cantidad mayor que la cantidad que se muestra en el campo **Puede hacer prod. ppal.** Por ejemplo, el artículo de embotellamiento puede ser un componente comprado con una fecha de recepción esperada que es demasiado atrasada para realizar las unidades de artículos adicionales del artículo superior por la fecha del campo **Fecha en que se necesita**.

## <a name="to-view-the-availability-of-an-item-by-its-units-of-measure"></a>Para ver la disponibilidad de un producto por sus unidades de medida
La página **Disponibilidad de producto por unidad de medida** muestra la disponibilidad de un producto en las unidades de medida en las que está almacenada.

> [!NOTE]  
> Para mantener esta información precisa, debe convertir las unidades de medida del producto. Por ejemplo, si compra un artículo en una unidad de medida, como cajas, y vende artículos en otra unidad de medida, como piezas, debe usar un diario de artículos para convertir las unidades de medida o "desempaquetar" artículos. Puede usar una línea de diario de elementos de ajuste negativo para reducir el inventario en la unidad de medida de compra, por ejemplo, cajas, y un ajuste positivo para aumentar el inventario en la unidad de medida de ventas, por ejemplo, piezas. 

## <a name="assembly-availability-page"></a>Página Disponibilidad de ensamblado
La página **Disponibilidad de ensamblado** muestra la información de disponibilidad detallada para el elemento del ensamblado. Abre:

- Automáticamente de una línea del pedido de venta en los escenarios de ensamblar para pedido cuando se introduce una cantidad que causa un problema de disponibilidad de componente.
- Automáticamente de una cabecera del pedido de ensamblado cuando se introduce un valor en el campo Cantidad que causa un problema de disponibilidad de componente.
- Manualmente cuando se abre desde un pedido de ensamblado. En la pestaña Acciones, en el grupo Funciones, haga clic en Mostrar disponibilidad.

La ficha desplegable **Detalles** muestra información detallada de la disponibilidad del elemento de ensamblado, incluida cuánta de la cantidad del pedido de ensamblado se puede ensamblar para la fecha de vencimiento basándose en la disponibilidad de los componentes necesarios. Esto se mostrará en el campo Capaz de ensamblar en la ficha desplegable Detalles.

El valor del campo de **Capaz de ensamblar** se muestra en una fuente de color rojo si la cantidad es menor que la que hay en el campo **Cantidad pendiente**, lo que indica que no hay suficientes componentes disponibles para ensamblar la cantidad total.

La ficha desplegable **Líneas** muestra información detallada de la disponibilidad de los componentes del ensamblado.

Si uno o más componentes del ensamblado no están disponibles, se reflejará en el campo **Capaz de ensamblar** en la línea en cuestión como cantidad inferior que la del campo **Cantidad pendiente** en la ficha desplegable **Detalles**.

## <a name="see-also"></a>Consulte también
[Gestionar inventario](inventory-manage-inventory.md)  
[Gestión de ensamblaje](assembly-assemble-items.md)  
[Trabajar con listas de materiales](inventory-how-work-BOMs.md)    
[Configurar ubicaciones](inventory-how-setup-locations.md)  
[Transferir el inventario entre almacenes](inventory-how-transfer-between-locations.md)  
[Vender productos](sales-how-sell-products.md)      
[Trabajar con Business Central](ui-work-product.md)  
[Funciones empresariales generales](ui-across-business-areas.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]