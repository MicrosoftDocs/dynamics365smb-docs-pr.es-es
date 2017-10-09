---
title: "Configurar asignación de recursos | Documentos de Microsoft"
description: "Obtener información sobre cómo el sistema puede ayudar a asegurar que se asigna a alguien que tiene las habilidades necesarias para proporcionar un servicio."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: resource, skill, service, zones
ms.date: 08/22/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 6c20c0b346186adad6e4b125dbd48bd0d3f56ab2
ms.contentlocale: es-es
ms.lasthandoff: 09/22/2017

---

# <a name="how-to-set-up-resource-allocation"></a>Configurar asignación de recursos
Para garantizar que una tarea de servicio esté bien efectuada, es importante encontrar un recurso que esté cualificado para hacer el trabajo. Puede configurar [!INCLUDE[d365fin](includes/d365fin_md.md)] de forma que resulte fácil asignar a quien tiene las habilidades correctas para el trabajo. En [!INCLUDE[d365fin](includes/d365fin_md.md)], llamamos a esto _asignación de recursos_. Puede asignar recursos basándose en las habilidades, disponibilidad o si se encuentran en la misma zona que el cliente. 

Para usar la asignación de recursos, debe configurar:  
  
* Las habilidades necesarias para la reparación y mantenimiento de productos de servicio. Las asigna a productos y recursos de servicio.  
* Las áreas geográficas, llamadas zonas, que define para su mercado. Por ejemplo, este, oeste, central, etc. Las asigna a clientes y recursos.  
* Si desea mostrar las habilidades y zonas del recurso y si desea mostrar una advertencia si alguien elige un recurso no calificado, o un recurso que no está en la zona de cliente.  

## <a name="to-set-up-skills"></a>Para configurar habilidades
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Habilidades** y, a continuación, seleccione el vínculo relacionado.  
2. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-assign-skills-to-service-items-and-resources"></a>Para asignar habilidades a productos y recursos de servicio
1. Elija el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), especifique **Producto de servicio** o **Recursos**, y elija el vínculo relacionado.  
2. Abra la ficha del producto o recurso de servicio y elija una de las opciones siguientes:  
  
    * Para productos de servicio, elija **Cualificaciones recurso**.  
    * Para los recursos, elija **Cualificaciones**.  

## <a name="to-set-up-zones"></a>Para configurar zonas
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Zonas** y, a continuación, seleccione el vínculo relacionado.  
2. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-assign-zones-to-customers-and-resources"></a>Para asignar zonas a clientes y recursos 
1. Elija el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), especifique **Clientes** o **Recursos**, y elija el vínculo relacionado.  
2. Abra la ficha del producto o recurso de servicio y elija una de las opciones siguientes:  
  
    * Para los clientes, elija una zona en el campo **Cód. zona servicio**.  
    * Para los recursos, elija la acción de **Zonas servicio**.  

## <a name="to-specify-what-to-show-when-a-resource-is-chosen"></a>Para especificar qué mostrar cuando seleccione un recurso
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Configuración del servicio** y, a continuación, seleccione el vínculo relacionado. 
2. En el campo **Opción cualificaciones recurso**, seleccione una de las opciones descritas en la tabla siguiente.  
  
    |**Opción**|**Descripción**|  
    |------------|-------------|  
    |Código mostrado | Se muestra solo el código.|  
    |Advertencia mostrada | Muestra la información y una advertencia si elige un recurso que no está calificado.|  
    |No utilizado | No muestra esta información.|  

## <a name="to-update-resource-capacity"></a>Para actualizar capacidad de recurso  
Es posible que tenga que cambiar la capacidad de los recursos.  
  
1. Elija el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), especifique **Capacidad recurso** y elija el vínculo relacionado.  
2. Elija el recurso y, a continuación, elija la acción **Fijar capacidad**.  
3. Realice los cambios y, a continuación, seleccione **Actualizar capacidad**.  

## <a name="to-update-skills-for-items-service-items-or-service-item-groups"></a>Para actualizar las cualificaciones para los productos, productos de servicio o grupos de producto de servicio
Si desea cambiar los códigos de habilidades asignados a elementos, por ejemplo de **PC** a **PCS**, puede hacerlo para un producto, un producto de servicio o para todos los productos de un grupo de productos de servicio.  
  
1. Elija el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), especifique **Productos**, **Productos de servicio** o **Grupo productos de servicio** y elija el vínculo relacionado.  
2. Elija la entidad que desee actualizar y, a continuación, elija la acción **Capacidades recurso**.  
3. En la línea con el código que desea modificar, en el campo **Cód. cualificación**, elija el código de cualificación correspondiente.  
4.  Si el producto tiene productos de servicio asociados, se abrirá un cuadro de diálogo con las dos opciones siguientes:  
  
    * Cambiar el código de capacidad al valor seleccionado: seleccione esta opción si desea reemplazar el antiguo código de cualificación por el nuevo en todos los productos de servicio relacionados.  
    * Elimine los códigos de aptitudes o actualice sus relaciones: seleccione esta opción si desea modificar el código de aptitud solo en este artículo. El código de cualificación de los productos de servicio relacionados se reasignará, es decir, se actualizará el campo **Se asigna de**.  
  
## <a name="see-also"></a>Consulte también
[Asignar recursos](service-how-to-allocate-resources.md)  
[Configurar horas de trabajo y de servicio](service-how-setup-work-service-hours.md)  
[Procedimiento: creación de informes de defecto](service-how-setup-fault-reporting.md)  
[Cómo configurar códigos para servicios estándar](service-how-setup-service-coding.md)  
 


