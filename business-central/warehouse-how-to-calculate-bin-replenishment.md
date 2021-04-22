---
title: Cómo calcular la reposición de ubicaciones | Documentos de Microsoft
description: Cuando la ubicación se configure para utilizar ubicación y picking directos, se tendrán en cuenta las prioridades de la plantilla de ubicación para esa ubicación al situar las recepciones.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 626e023d97c869d9d0fe63346053ecb42120a0ee
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2021
ms.locfileid: "5782739"
---
# <a name="calculate-bin-replenishment"></a>Calcular reposición ubicación
Cuando la ubicación se configure para utilizar ubicación y picking directos, se tendrán en cuenta las prioridades de la plantilla de ubicación para esa ubicación al situar las recepciones. Las prioridades incluyen las cantidades mínimas y máximas de contenido de la ubicación que se han establecido para una ubicación determinada, y los ranking de ubicación. Por tanto, si llegan productos a un ritmo estable, se rellenarán las ubicaciones de picking más utilizadas en cuanto se vacíen.  

Pero las existencias no siempre llegan a un ritmo constante. A veces, los productos se compran en grandes cantidades por lo que la empresa puede obtener un mejor precio, o su departamento de producción puede fabricar un lote de un producto para conseguir un menor precio de coste unitario. Así los productos no se volverán a recibir en el almacén durante algún tiempo y el almacén necesita mover productos periódicamente a las ubicaciones de picking desde las áreas de almacenamiento masivas.  

También es posible que el almacén espere pronto la llegada de nuevas existencias y desee vaciar el área de almacenamiento masivo de productos antes de que llegue la mueva mercancía.  

Finalmente, si ha definido sus ubicaciones de almacenamiento masivo con un tipo de ubicación sólo con la acción **Ubicar**, es decir, que el tipo de ubicación no tiene activada la acción **Picking**, siempre debe mantener las ubicaciones de picking llenas, ya que no se sugerirá un picking de existencias desde ubicaciones de tipo Ubicación.  

## <a name="to-replenish-pick-bins"></a>Para reponer ubicaciones de picking  
1.  Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Hoja trabajo mov.** y luego elija el enlace relacionado.  
2.  Elija la acción **Calcular reposición ubicación** para abrir la página de solicitud de informes.  
3.  Rellene la página del proceso para limitar el alcance de las sugerencias de reposición que se calcularán. Por ejemplo, puede que esté preocupado por determinadas zonas, ubicaciones o productos.  
4.  Elija el botón **Aceptar**. Se crearán líneas para los movimientos de reposición que es necesario realizar según las reglas que se han configurado para las ubicaciones y contenido de ubicaciones, es decir, productos en ubicaciones.  
5.  Si desea ejecutar todas las sugerencias de reposición, elija la acción **Crear movimiento**. Los empleados pueden encontrar instrucciones en el elemento de menú **Movimientos**, ejecutarlas y registrarlas.  
6.  Si sólo desea ejecutar algunas sugerencias, elimine las líneas menos importantes y, a continuación, cree un movimiento.  

La próxima vez que calcule la reposición de la ubicación, se volverán a crear las sugerencias que ha eliminado, si siguen siendo válidas en ese momento.  

> [!NOTE]  
>  Si un producto cumple las siguientes condiciones:  
>   
>  -   El producto tiene fecha de caducidad y  
> -   Se selecciona el campo **Picking según FEFO (Primero en caducar, primero en salir)** de la ficha de almacén. y  
> -   Utilice la funcionalidad **Calcular reposición ubicación**  
>   
>  los campos **Desde zona** y **Desde ubicación** estarán en blanco, ya que el algoritmo para calcular desde dónde se van a mover los productos sólo se ejecuta al activar la función **Crear movimiento**.  

## <a name="see-also"></a>Consulte también  
[Gestión almacén](warehouse-manage-warehouse.md)  
[Realización de picking por el FEFO](warehouse-picking-by-fefo.md)  
[Grupos contables inventario](inventory-manage-inventory.md)  
[Configuración de la gestión del almacén](warehouse-setup-warehouse.md)     
[Gestión de ensamblaje](assembly-assemble-items.md)    
[Detalles de diseño: Gestión de almacén](design-details-warehouse-management.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]