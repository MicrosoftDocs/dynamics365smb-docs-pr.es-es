---
title: "Cómo realizar un seguimiento de productos marcados para seguimiento | Documentos de Microsoft"
description: "Puede ver donde se ha utilizado un producto marcado para seguimiento, incluso cómo y dónde se recibió o se produjo, transfirió, vendió, consumió o devolvió. También puede encontrar todas las instancias actuales de un número de serie o de lote específico en la base de datos. Puede hacerlo con las funciones Seguimiento de producto y Navegar."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: cc24989d2cf770cd88bbde23d483e3859ff4a68a
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="trace-item-tracked-items"></a>Realizar seguimiento de productos seguidos
Puede ver donde se ha utilizado un producto marcado para seguimiento, incluso cómo y dónde se recibió o se produjo, transfirió, vendió, consumió o devolvió. También puede encontrar todas las instancias actuales de un número de serie o de lote específico en la base de datos. Puede hacerlo con las funciones Seguimiento de producto y Navegar.  

 Estas funciones pueden ser especialmente útiles en controles de calidad en los que sea necesario conocer qué clientes recibieron productos con un número de lote en particular, o cuando es necesario conocer de qué lote proviene un componente defectuoso.  

 En la ventana **Seguimiento productos**, puede realizar un seguimiento hacia adelante y hacia atrás de una secuencia de transacciones registradas del inventario para el número de serie o de lote.  

 En la ventana **Navegar**, no puede ver la secuencia de transacciones, pero puede ver todos los registros del número de serie o de lote, tanto las entradas registradas como los registros abiertos.  

 Las dos características se pueden utilizar en combinación mediante la transferencia de un número de serie o de lote rastreado a la ventana **Navegar** para terminar un escenario del seguimiento completo. Si desea obtener más información, consulte [Tutorial: seguimiento de números de serie-lote](walkthrough-tracing-serial-lot-numbers.md).  

## <a name="to-trace-item-tracked-items"></a>Para controlar productos seguidos  

1.  Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Seguimiento productos** y, a continuación, seleccione el vínculo relacionado.  
2.  En los campos de filtrado que aparecen en la parte superior de la ventana, introduzca los números de producto específicos o un filtro sobre los números de producto a los que desea realizar un seguimiento.  
3.  En el campo **Mostrar componentes**, seleccione si desea visualizar también de dónde provienen los componentes para los productos. Las opciones de este campo son las siguientes.  

    |Campo|Description|  
    |----------------------------------|---------------------------------------|  
    |**No**|seleccione esta opción si no desea visualizar ningún componente.|  
    |**Sólo producto seguido**|seleccione esta opción si solamente desea visualizar aquellos componentes que tengan números de lote o de serie.|  
    |**Todos**|seleccione esta opción si desea visualizar todos los componentes.|  

4.  En el campo **Método seguimiento**, seleccione el método que desea utilizar para realizar el seguimiento del producto. Las opciones son las siguientes  

    |Campo|Description|  
    |----------------------------------|---------------------------------------|  
    |**Uso -> Origen**|Este método realiza un seguimiento del producto comenzando por dónde se utilizó hasta de dónde proviene. Por ejemplo, si se vendió un producto fabricado a un cliente, la ventana **Seguimiento productos** muestra esta información con la línea de albarán de ventas primero, la cual puede expandir para ver de qué orden de producción proviene.|  
    |**Origen->Uso**|este método realiza un seguimiento del producto comenzando por dónde se introdujo en el inventario y terminando por dónde se utilizó. Por ejemplo, si se vendió un producto fabricado a un cliente, la ventana **Seguimiento productos** muestra esta información con el orden de producto acabado primeramente, el cual puede expandir para ver las líneas del albarán de ventas en los que se ha utilizado el producto.|  

5.  Elija la acción **Realizar seguimiento** para ejecutar el seguimiento.  

> [!NOTE]  
>  Si se ha recibido el mismo lote en más transacciones, la ventana **Seguimiento producto** no puede mostrar todas las transacciones. Solo se muestran las transacciones liquidadas.  

> [!NOTE]  
>  Si el historial adicional de la transacción bajo la línea de seguimiento del producto ya se ha rastreado por otra línea por encima suyo, la casilla de verificación **Seguimiento en curso** está seleccionada. Para proporcionar una vista más sencilla, las líneas subyacentes no se muestran.  
>   
>  Para buscar las líneas de seguimiento del producto donde el historial de la transacción ya se ha rastreado, seleccione el botón **Ir a rastreado**. La línea de seguimiento de producto en cuestión está seleccionada y se expanden todas las líneas subyacentes.  

## <a name="to-find-item-tracked-items-with-navigate"></a>Para buscar productos marcados para seguimiento con Navegar  

1.  Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Navegar** y, a continuación, seleccione el vínculo relacionado.  
2.  En la ficha desplegable **Seguim. prod.**, en los campos **Nº serie** y **Nº lote**, introduzca los números de seguimiento de productos de los que desea realizar un seguimiento.  
3.  Elija la acción **Buscar** para buscar todos los casos números de serie o de lote en la base de datos.  

## <a name="see-also"></a>Consulte también  
[Grupos contables inventario](inventory-manage-inventory.md)  
[Detalles de diseño: seguimiento de productos](design-details-item-tracking.md)
[Detalles de diseño. Seguimiento y reservas de productos](design-details-item-tracking-and-reservations.md)  
[Reservar artículos](inventory-how-to-reserve-items.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
[Tutorial: seguimiento de números de serie/lote](walkthrough-tracing-serial-lot-numbers.md)

