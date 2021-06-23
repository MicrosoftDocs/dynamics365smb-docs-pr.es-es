---
title: Realizar seguimiento de productos seguidos
description: Puede ver donde se ha utilizado un producto marcado para seguimiento, incluso cómo y dónde se recibió o se produjo, transfirió, vendió, consumió o devolvió. También puede encontrar todas las instancias actuales de un número de serie o de lote específico en la base de datos. Puede hacerlo con las características Seguimiento de producto y Buscar movimientos.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: bbfe0237beb58f22d3be7bc388d7b2726f05d4ba
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/09/2021
ms.locfileid: "6214758"
---
# <a name="trace-item-tracked-items"></a>Realizar seguimiento de productos seguidos
Puede ver donde se ha utilizado un producto marcado para seguimiento, incluso cómo y dónde se recibió o se produjo, transfirió, vendió, consumió o devolvió. También puede encontrar todas las instancias actuales de un número de serie o de lote específico en la base de datos. Puede hacerlo con las características Seguimiento de producto y [Buscar movimientos](ui-find-entries.md).  

Estas funciones pueden ser especialmente útiles en controles de calidad en los que sea necesario conocer qué clientes recibieron productos con un número de lote en particular, o cuando es necesario conocer de qué lote proviene un componente defectuoso.  

 En la página **Seguimiento productos**, puede realizar un seguimiento hacia adelante y hacia atrás de una secuencia de transacciones registradas del inventario para el número de serie o de lote.  

 En la página **Buscar movimientos**, no puede ver la secuencia de transacciones, pero puede ver todos los registros del número de serie o de lote, tanto las entradas registradas como los registros abiertos.  

 Las dos características se pueden utilizar en combinación mediante la transferencia de un número de serie o de lote rastreado a la página **Buscar movimientos** para terminar un escenario del seguimiento completo. <!-- For more information, see [Walkthrough: Tracing Serial-Lot Numbers](walkthrough-tracing-serial-lot-numbers.md).   -->

## <a name="to-trace-item-tracked-items"></a>Para controlar productos seguidos  

1.  Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Seguimiento productos** y luego elija el enlace relacionado.  
2.  En los campos de filtrado que aparecen en la parte superior de la página, introduzca los números de producto específicos o un filtro sobre los números de producto a los que desea realizar un seguimiento.  
3.  En el campo **Mostrar componentes**, seleccione si desea visualizar también de dónde provienen los componentes para los productos. Las opciones de este campo son las siguientes.  

    |Campo|Description|  
    |----------------------------------|---------------------------------------|  
    |**No**|seleccione esta opción si no desea visualizar ningún componente.|  
    |**Sólo producto seguido**|seleccione esta opción si solamente desea visualizar aquellos componentes que tengan números de lote o de serie.|  
    |**Todos**|seleccione esta opción si desea visualizar todos los componentes.|  

4.  En el campo **Método seguimiento**, seleccione el método que desea utilizar para realizar el seguimiento del producto. Las opciones son las siguientes  

    |Campo|Description|  
    |----------------------------------|---------------------------------------|  
    |**Uso -> Origen**|Este método realiza un seguimiento del producto comenzando por dónde se utilizó hasta de dónde proviene. Por ejemplo, si se vendió un producto fabricado a un cliente, la página **Seguimiento productos** muestra esta información con la línea de albarán de ventas primero, la cual puede expandir para ver de qué orden de producción proviene.|  
    |**Origen->Uso**|este método realiza un seguimiento del producto comenzando por dónde se introdujo en el inventario y terminando por dónde se utilizó. Por ejemplo, si se vendió un producto fabricado a un cliente, la página **Seguimiento productos** muestra esta información con el orden de producto acabado primeramente, el cual puede expandir para ver las líneas del albarán de ventas en los que se ha utilizado el producto.|  

5.  Elija la acción **Realizar seguimiento** para ejecutar el seguimiento.  

> [!NOTE]  
>  Si se ha recibido el mismo lote en más transacciones, la página **Seguimiento producto** no puede mostrar todas las transacciones. Solo se muestran las transacciones liquidadas.  

> [!NOTE]  
>  Si el historial adicional de la transacción bajo la línea de seguimiento del producto ya se ha rastreado por otra línea por encima suyo, la casilla de verificación **Seguimiento en curso** está seleccionada. Para proporcionar una vista más sencilla, las líneas subyacentes no se muestran.  
>   
>  Para buscar las líneas de seguimiento del producto donde el historial de la transacción ya se ha rastreado, seleccione el botón **Ir a rastreado**. La línea de seguimiento de producto en cuestión está seleccionada y se expanden todas las líneas subyacentes.  

## <a name="to-find-item-tracked-items-with-find-entries"></a>Para buscar productos marcados para seguimiento con Buscar movimientos  

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Buscar movimientos** y luego seleccione el vínculo relacionado.  
2. Escoja **Acciones** > **Buscar por** > **Buscar por referencia de producto**.
3. En la ficha desplegable **N.º de serie** y **N.º de lote**, introduzca los números de seguimiento de productos de los que desea realizar un seguimiento.  
4. Elija la acción **Buscar** para buscar todos los casos números de serie o de lote en la base de datos.  

## <a name="see-also"></a>Consulte también

[Inventario](inventory-manage-inventory.md)  
[Trabajar con números de serie, de lote y de paquete](inventory-how-work-item-tracking.md)  
[Detalles de diseño: Seguimiento de productos](design-details-item-tracking.md)  
[Detalles de diseño: Seguimiento de productos y reservas](design-details-item-tracking-and-reservations.md)  
[Reservar artículos](inventory-how-to-reserve-items.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
<!-- [Walkthrough: Tracing Serial-Lot Numbers](walkthrough-tracing-serial-lot-numbers.md)   -->
[Buscar movimientos](ui-find-entries.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]