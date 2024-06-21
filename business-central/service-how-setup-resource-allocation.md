---
title: Configurar asignación de recursos | Documentos de Microsoft
description: Obtener información sobre cómo el sistema puede ayudar a asegurar que se asigna a alguien que tiene las habilidades necesarias para proporcionar un servicio.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'resource, skill, service, zones'
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# Configurar asignación de recursos
Para garantizar que una tarea de servicio esté bien efectuada, es importante encontrar un recurso que esté cualificado para hacer el trabajo. Puede configurar [!INCLUDE[prod_short](includes/prod_short.md)] de forma que resulte fácil asignar a quien tiene las habilidades correctas para el trabajo. En [!INCLUDE[prod_short](includes/prod_short.md)], llamamos a esto _asignación de recursos_. Puede asignar recursos basándose en las habilidades, disponibilidad o si se encuentran en la misma zona que el cliente. 

Para usar la asignación de recursos, debe configurar:  
  
* Las habilidades necesarias para la reparación y mantenimiento de productos de servicio. Las asigna a productos y recursos de servicio.  
* Las áreas geográficas, llamadas zonas, que define para su mercado. Por ejemplo, este, oeste, central, etc. Las asigna a clientes y recursos.  
* Si desea mostrar las habilidades y zonas del recurso y si desea mostrar una advertencia si alguien elige un recurso no calificado, o un recurso que no está en la zona de cliente.  

## Para configurar habilidades
1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , entr en **Cualificaciones** y luego elija el enlace relacionado.  
2. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## Para asignar habilidades a productos y recursos de servicio
1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Productos de servicio** o **Recursos** y luego elija el enlace relacionado.  
2. Abra la ficha del producto o recurso de servicio y elija una de las opciones siguientes:  
  
    * Para productos de servicio, elija **Cualificaciones recurso**.  
    * Para los recursos, elija **Cualificaciones**.  

## Para configurar zonas
1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Zonas** y luego elija el enlace relacionado.  
2. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## Para asignar zonas a clientes y recursos 
1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Clientes** o **Recursos** y luego elija el enlace relacionado.  
2. Abra la ficha del producto o recurso de servicio y elija una de las opciones siguientes:  
  
    * Para los clientes, elija una zona en el campo **Cód. zona servicio**.  
    * Para los recursos, elija la acción de **Zonas servicio**.  

## Para especificar qué mostrar cuando seleccione un recurso
1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración de administración de servicios** y luego elija el enlace relacionado. 
2. En el campo **Opción cualificaciones recurso**, seleccione una de las opciones descritas en la tabla siguiente.  
  
    |**Opción**|**Descripción**|  
    |------------|-------------|  
    |Código mostrado | Se muestra solo el código.|  
    |Advertencia mostrada | Muestra la información y una advertencia si elige un recurso que no está calificado.|  
    |No utilizado | No muestra esta información.|  

## Para actualizar capacidad de recurso  
Es posible que tenga que cambiar la capacidad de los recursos.  
  
1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Capacidad recurso**, y luego elija el enlace relacionado.  
2. Elija el recurso y, a continuación, elija la acción **Fijar capacidad**.  
3. Realice los cambios y, a continuación, seleccione **Actualizar capacidad**.  

## Para actualizar las cualificaciones para los productos, productos de servicio o grupos de producto de servicio
Si desea cambiar los códigos de habilidades asignados a elementos, por ejemplo de **PC** a **PCS**, puede hacerlo para un producto, un producto de servicio o para todos los productos de un grupo de productos de servicio.  
  
1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Productos** o **Producto de servicio** o **Cód. grupo prod. servicio** y, a continuación, elija el vínculo relacionado.  
2. Elija la entidad que desee actualizar y, a continuación, elija la acción **Capacidades recurso**.  
3. En la línea con el código que desea modificar, en el campo **Cód. cualificación**, elija el código de cualificación correspondiente.  
4.  Si el producto tiene productos de servicio asociados, se abrirá un cuadro de diálogo con las dos opciones siguientes:  
  
    * Cambiar el código de capacidad al valor seleccionado: seleccione esta opción si desea reemplazar el antiguo código de cualificación por el nuevo en todos los productos de servicio relacionados.  
    * Elimine los códigos de aptitudes o actualice sus relaciones: seleccione esta opción si desea modificar el código de aptitud solo en este artículo. El código de cualificación de los productos de servicio relacionados se reasignará, es decir, se actualizará el campo **Se asigna de**.  
  
## Consulte también
[Asignar recursos](service-how-to-allocate-resources.md)  
[Configurar horas de trabajo y de servicio](service-how-setup-work-service-hours.md)  
[Crear informes de defecto](service-how-setup-fault-reporting.md)  
[Configurar códigos para servicios estándar](service-how-setup-service-coding.md)  
 



[!INCLUDE[footer-include](includes/footer-banner.md)]