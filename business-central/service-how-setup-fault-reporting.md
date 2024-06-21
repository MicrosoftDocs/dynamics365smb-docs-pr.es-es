---
title: Configurar informes de defectos en gestión de servicios
description: El informe de defectos le permite configurar estándares para registrar información de defectos de productos de servicio con códigos de defectos y más.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 06/23/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# Crear informes de defecto
El informe de defectos le permite configurar estándares para registrar información de defectos de productos de servicio. Por ejemplo, puede especificar de qué problema se trata, los síntomas que detecta, el motivo del problema y cómo resolverlo.  

Los códigos de defecto describen los típicos defectos de producto de servicio o las acciones realizadas sobre productos de servicio. Dependiendo del nivel de información de defecto de la empresa, puede que necesite configurar códigos de área de defecto y códigos de síntoma para poder registrar códigos de defecto. Las áreas de defecto describen las áreas de los defectos de productos de servicio. Los códigos de razón de defecto describen la causa de los defectos de producto de servicio y, si es necesario, si se excluyen los descuentos de garantía y de contrato. Por ejemplo, puede que desee excluir el descuento de garantía y de contrato si el cliente es el responsable del defecto en el producto de servicio. Asigne códigos de razón de defecto a pedidos de servicio. Para obtener más información, consulte [Trabajar con tareas de servicio](service-how-to-work-on-service-tasks.md).  

## Para especificar el nivel total de información de defecto
1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración de servicio** y luego elija el enlace relacionado.
2. En el campo **Nivel inform. defecto**, seleccione una de las opciones descritas en la tabla siguiente.  

    |**Nivel defecto**|**Descripción**|  
    |------------|-------------|  
    |Ninguno | No se utiliza ningún código de información.|  
    |Defecto | Los códigos se muestran en la tabla **Cód. defecto**. Estos códigos identifican defectos de productos de servicio o acciones que realizar en productos de servicio. Puede agrupar los códigos relacionados en agrupaciones de **Cód. área defecto**.|  
    |Defecto + Síntoma | Proporcione una combinación de códigos en las tablas **Cód. defecto** y **Cód. síntoma**. Los códigos de síntoma habituales incluyen indicadores que puede usar un cliente para describir un problema, como un ruido o calidad.|  
    |Defecto + Síntoma + Area | Utilice Cód. defecto, Cód. síntoma y Cód. área defecto, como implementación del sistema internacional de codificación de reparaciones (IRIS).|  

Para finalizar la configuración del informe de defectos, también puede especificar las reparaciones o resoluciones asociadas con un defecto. Se configura en la página **Relación códs. defecto/resol.**, donde se configuran combinaciones de códigos para el grupo de productos de servicio del producto de servicio desde el que se ha accedido a la ventana y el número de ocurrencias de cada uno.

## Para crear relaciones de códigos de defecto y resolución
<!--this needs to go in a working with topic-->
 Para poder ver los métodos más habituales de reparación de determinados defectos de producto durante el servicio de los productos, deberá crear información acerca de las relaciones de códigos de defecto/resolución. Utilice el trabajo por lotes **Insertar relac. cód. def./res.** para buscar todas las combinaciones de códigos de defecto y resolución en los pedidos de servicio registrados y, a continuación, registrarlos en la página **Relac. códs. defecto/resol.**

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Insertar relac. cód. def.res.** y, a continuación, elija el vínculo relacionado.  
2. Introduzca las fechas para definir el periodo que desea incluir en el proceso.  
3. Para agrupar las relaciones por grupos de producto de servicio, elija la casilla **Relación basada en grupo prod. serv.**.  
4. Para retener los registros que insertó manualmente en la página **Relaciones códigos defecto/resolución**, elija la casilla **Retiene registro insertado manualmente**.  

## Consulte también
[Configurar la gestión de servicios](service-setup-service.md)  
[Gestión de servicios](service-service.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]