---
title: Cómo planificar órdenes de proyecto | Documentos de Microsoft
description: Esta tarea de planificación se inicia desde un pedido de venta y para realizarla se utiliza la página **Planificación pedido venta**. Una vez creada la orden de producción de un proyecto, puede seguir planificándola en la página **Planificación de pedidos**.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 4cb63a7dc26e13c7947ba2ae071c3dff87c53e9d
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/08/2019
ms.locfileid: "806658"
---
# <a name="plan-project-orders"></a>Planificar órdenes de proyecto
Esta tarea de planificación se inicia desde un pedido de venta y para realizarla se utiliza la página **Planificación pedido venta**. Una vez creada la orden de producción de un proyecto, puede seguir planificándola en la página **Planificación de pedidos**.  

## <a name="to-create-a-project-production-order"></a>Para crear una orden de producción de un proyecto  

1.  Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Pedidos de venta** y luego elija el enlace relacionado.  
2.  Seleccione el pedido de venta que representa el proyecto de producción y después seleccione la acción **Planificación**.  
4.  En la página **Planificación de pedido de venta**, seleccione la acción **Crear orden de producción**.  
5.  En la página **Crear pedido a partir de las ventas**, en el campo **Tipo orden**, seleccione **Orden proyecto**.  
6.  Elija el botón **Sí**.  
7.  Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Órdenes de producción** y luego elija el enlace relacionado.
8. Abra la orden de producción que acaba de crear.  

    Tenga en cuenta que el campo **Tipo de procedencia** de la orden de producción contiene **Cabecera de ventas** y la orden tiene varias líneas, una para cada producto de línea de venta que debe fabricarse.  
9. Seleccione la acción **Planificación**.
10. En la página **Planificación de pedidos**, seleccione la acción **Actualizar** para calcular una nueva demanda.  

Se mostrará la línea de cabecera de la orden del proyecto con todas las líneas de demanda no satisfecha expandidas bajo ella. Aunque la orden de producción contiene líneas para varios productos fabricados, la demanda total de todas las líneas de la orden de producción aparece bajo una línea de cabecera de la orden en la página **Programación de pedidos** y se muestra el nombre del cliente original. Ahora puede empezar a planificar la demanda, según se indica en [Planificar nueva demanda pedido por pedido](production-how-to-plan-for-new-demand.md).  

> [!NOTE]  
>  Las líneas de demanda en el orden de producción del proyecto que disponen de **Prod. Pedido** en el campo de **Sistema reposición** representan las órdenes de producción subyacentes. Después de generar estas órdenes de producción, deberá volver a calcular un plan en la página **Programación de pedidos** para identificar la demanda de componentes no satisfecha. En ese caso, estas líneas se muestran como líneas de demanda bajo una línea de cabecera de orden de producción normal, es decir, la relación del proyecto ya no se muestra en la página. Sin embargo, si utiliza la función Seguimiento pedido, puede retroceder y avanzar por todos los pedidos de suministro creados bajo el pedido de venta original.  

## <a name="see-also"></a>Consulte también
[Planificación](production-planning.md)   
[Configuración de fabricación](production-configure-production-processes.md)  
[Fabricación](production-manage-manufacturing.md)    
[Grupos contables inventario](inventory-manage-inventory.md)  
[Compras](purchasing-manage-purchasing.md)  
[Detalles de diseño: planificación de aprovisionamiento](design-details-supply-planning.md)   
[Procedimientos recomendados de configuración: planificación de suministros](setup-best-practices-supply-planning.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
