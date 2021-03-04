---
title: Cómo crear productos de servicio | Documentos de Microsoft
description: Cuando reciba un producto no registrado para servicio, puede registrarlo como un producto de servicio.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: e45c23c8ed3b6f96c24e78666822c6fb9ef9859f
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "4757897"
---
# <a name="create-service-items"></a>Crear productos de servicio
En [!INCLUDE[prod_short](includes/prod_short.md)], el término “producto de servicio” se refiere el equipo o productos que requieren servicio. Al crear un pedido de servicio, se especifican los productos que necesitan servicio. En el pedido, puede vincular un producto de servicio a un producto en existencias o un grupo de productos de servicio.    

Cuando reciba un producto que necesita servicio, puede registrarlo como un producto de servicio. Existen varias formas de hacerlo. Por ejemplo, puede crear un producto de servicio en la página **Productos de servicio**, o como parte de otro proceso, por ejemplo al trabajar con un pedido de servicio.   

## <a name="to-create-a-service-item"></a>Para crear un producto de servicio  
1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Productos de servicio** y luego elija el enlace relacionado.
2. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-create-service-items-within-a-service-order"></a>Para crear productos de servicio en un pedido de servicio  
Cuando se reciben productos para servicio que desea registrar como productos de servicio, puede crearlos como productos de servicio en las páginas **Pedido servicio** u **Oferta servicio**.  

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Pedidos de servicio** y luego elija el enlace relacionado.  
2. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Elija la acción **Crear producto de servicio**.  

    Se asignará un número al artículo de servicio y se creará una ficha de artículo de servicio. El campo **Nº producto servicio** se rellenará con el número del nuevo producto de servicio.

## <a name="to-create-a-service-item-when-shipping-items"></a>Para crear un producto de servicio al enviar productos  
Cuando se envían los productos al registrar los pedidos o las facturas de venta, los productos enviados se registran automáticamente como productos de servicio cuando se cumple la condición siguiente. Los artículos deben pertenecer a un grupo de artículo de servicio con la casilla **Crear prod. servicio** activada. Si los artículos tienen números de serie registrados en la página Líns. seguim. prod., esta información se copiará automáticamente al campo **Nº serie** en la ficha de artículo de servicio al crear artículos de servicio.  

El siguiente procedimiento muestra cómo crear productos de servicio al enviar productos de pedidos de venta.  

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Pedidos de venta** y luego elija el enlace relacionado.  
2. Abra el pedido de venta correspondiente.  
3. Seleccione la acción **Registrar** o **Registrar e imprimir**.  
4. Seleccione la acción **Enviar** o **Enviar y facturar**.  
5. Se crearán automáticamente productos de servicio para los productos del pedido, siempre que pertenezcan a un grupo de productos de servicio que se ha configurado para crear productos de servicio. Si ha registrado números de serie específicos en la página **Líns. seguim. prod.**, éstos se asignarán a los productos de servicio.  

> [!NOTE]  
>  Si un producto es una L.M. y la ha desplegado, los productos de la L.M. desplegada se procesarán de la misma forma que los productos comunes. Los productos de servicio se crean en base a la condición del grupo de productos de servicio y, de manera opcional, en la condición de los números de serie. Además, si se crea un producto de servicio para un producto de la L.M. desplegada compuesto por otros componentes de la L.M., estos productos se crearán como componentes de un producto de servicio para el producto de servicio de la L.M. desplegada.  
>   
>  Si un producto es una L.M. y no ha desplegado la L.M., se crea un producto de servicio para aquel basándose en la condición del grupo de productos de servicio y, de manera opcional, en la condición de los números de serie.  

## <a name="to-insert-a-starting-fee-for-a-service-item"></a>Para insertar un gasto de inicio para un producto de servicio
1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Tareas de servicio** y luego elija el enlace relacionado.
2. Elija la acción **Hoja de producto**.
3. Seleccione la línea de servicio y, a continuación elija **Acciones**, seleccione **Funciones** y luego la acción **Insertar cuota inicial**.  

    Se insertará una línea de servicio del tipo **Coste** con el gasto de inicio. El gasto de inicio se aplica al producto de servicio seleccionado.

## <a name="see-also"></a>Consulte también  
[Configurar componentes de servicio y de productos](service-how-setup-service-items.md)  
[Configurar la gestión de servicios](service-setup-service.md)  
[Gestión de servicios](service-service.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]