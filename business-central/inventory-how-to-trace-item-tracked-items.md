---
title: Rastreo de artículos rastreados
description: 'Puede ver dónde se usó un artículo rastreado, incluso cómo y cuándo se recibió, produjo o devolvió con las funciones Rastreo de artículos y Buscar entradas.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.search.forms: '6520,'
ms.date: 05/16/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Rastreo de artículos rastreados

Puede ver donde se ha utilizado un producto marcado para seguimiento, incluso cómo y dónde se recibió o se produjo, transfirió, vendió, consumió o devolvió. También puede encontrar todas las instancias actuales de un número de serie o de lote específico en la base de datos. Puede hacerlo con las características Seguimiento de producto y [Buscar movimientos](ui-find-entries.md).  

Estas funciones pueden ser útiles en el control de calidad cuando necesita saber qué clientes recibieron productos con un número de lote particular o cuando necesita saber de qué lote proviene un componente defectuoso.  

 En la página **Seguimiento productos**, puede realizar un seguimiento hacia adelante y hacia atrás de una secuencia de transacciones registradas del inventario para el número de serie o de lote.  

 En la página  **Buscar entradas**, no puede ver la secuencia de transacciones, pero puede ver todos los registros del número de serie o lote, tanto las entradas contabilizadas como los registros abiertos.  

 Las dos características se pueden utilizar en combinación mediante la transferencia de un número de serie o de lote rastreado a la página **Buscar movimientos** para terminar un escenario del seguimiento completo. <!-- For more information, see [Walkthrough: Tracing Serial-Lot Numbers](walkthrough-tracing-serial-lot-numbers.md).   -->

## Para controlar productos seguidos  

1.  Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Seguimiento de productos**, y luego elija el enlace relacionado.  
2.  En los campos de filtrado que aparecen en la parte superior de la página, introduzca los números de producto específicos o un filtro sobre los números de producto a los que desea realizar un seguimiento.  
3.  En el campo **Mostrar componentes**, seleccione si quiere visualizar también de dónde provienen los componentes para los productos. La siguiente tabla describe las opciones.  

    |Campo|Descripción|  
    |----------------------------------|---------------------------------------|  
    |**No**|No mostrar componentes.|  
    |**Sólo producto seguido**|Muestre solo los componentes que tienen números de lote o de serie.|  
    |**Todo**|Mostrar todos los componentes.|  

4.  En el campo **Método seguimiento**, seleccione el método que quiere utilizar para realizar el seguimiento del producto. La siguiente tabla describe las opciones.  

    |Campo|Descripción|  
    |----------------------------------|---------------------------------------|  
    |**Uso -> Origen**|Siga el producto comenzando por donde se utilizó hasta de donde proviene. Por ejemplo, si se vendió un producto fabricado a un cliente, la página **Seguimiento productos** muestra esta información con la línea de albarán de ventas primero, la cual puede expandir para ver de qué orden de producción proviene.|  
    |**Origen->Uso**|Siga el producto comenzando por donde llegó al inventario hasta donde se utilizó. Por ejemplo, si se vendió un producto fabricado a un cliente, la página **Seguimiento productos** muestra esta información con el pedido de producto acabado primero, el cual luego puede expandir para ver las líneas del albarán de ventas en las que se ha utilizado el producto.|  

5.  Elija la acción **Realizar seguimiento** para ejecutar el seguimiento.  

> [!NOTE]  
>  Solo se muestran las transacciones liquidadas. Si se ha recibido el mismo lote en varias transacciones, la página **Seguimiento de producto** no puede mostrar todas las transacciones.   

> [!NOTE]  
>  Si el historial adicional de la transacción bajo la línea de seguimiento del producto ya se ha rastreado por otra línea por encima suyo, la casilla de verificación **Seguimiento en curso** está seleccionada. Para proporcionar una vista más sencilla, las líneas subyacentes no se muestran.  
>   
>  Para buscar las líneas de seguimiento del producto donde el historial de la transacción ya se ha rastreado, seleccione el botón **Ir a rastreado**. La línea de seguimiento de producto en cuestión está seleccionada y se expanden todas las líneas subyacentes.  

## Para buscar productos marcados para seguimiento con Buscar movimientos  

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Buscar movimientos** y, a continuación, elija el vínculo relacionado.  
2. Seleccione **Buscar referencias de artículos**.
3. En la ficha desplegable **N.º de serie** y **N.º de lote**, introduzca los números de seguimiento de productos de los que desea realizar un seguimiento.  
4. Elija la acción **Buscar** para buscar todos los casos números de serie o de lote en la base de datos.  

## Consulte también .

[Grupos contables inventario](inventory-manage-inventory.md)  
[Trabajar con números de serie, de lote y de paquete](inventory-how-work-item-tracking.md)  
[Detalles de diseño: Seguimiento de productos](design-details-item-tracking.md)  
[Detalles de diseño: Seguimiento de productos y reservas](design-details-item-tracking-and-reservations.md)  
[Reservar artículos](inventory-how-to-reserve-items.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
<!-- [Walkthrough: Tracing Serial-Lot Numbers](walkthrough-tracing-serial-lot-numbers.md)   -->
[Buscar movimientos](ui-find-entries.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
