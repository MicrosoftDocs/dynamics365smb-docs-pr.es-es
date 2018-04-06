---
title: "Configurar información de defectos en la gestión de servicios | Documentos de Microsoft"
description: "Más información sobre la configuración de los procesos de creación de informes de defecto."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/22/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: ea8351924e8e4af4b16b41fa7bc92bf59069ac01
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---

# <a name="set-up-fault-reporting"></a>Crear informes de defecto
El informe de defectos le permite configurar estándares para registrar información de defectos de productos de servicio. Por ejemplo, puede especificar de qué problema se trata, los síntomas que detecta, el motivo del problema y cómo resolverlo.  

Los códigos de defecto describen los típicos defectos de producto de servicio o las acciones realizadas sobre productos de servicio. Dependiendo del nivel de información de defecto de la empresa, puede que necesite configurar códigos de área de defecto y códigos de síntoma para poder registrar códigos de defecto. Las áreas de defecto describen las áreas de los defectos de productos de servicio. Los códigos de razón de defecto describen la causa de los defectos de producto de servicio y, si es necesario, si se excluyen los descuentos de garantía y de contrato. Por ejemplo, puede que desee excluir el descuento de garantía y de contrato si el cliente es el responsable del defecto en el producto de servicio. Asigne códigos de razón de defecto a pedidos de servicio. Para obtener más información, consulte [Trabajar con tareas de servicio](service-how-to-work-on-service-tasks.md).  

## <a name="to-specify-the-overall-level-of-fault-reporting-to-use"></a>Para especificar el nivel total de información de defecto que se utilizará
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Configuración del servicio** y, a continuación, seleccione el vínculo relacionado. 
2. En el campo **Nivel inform. defecto**, seleccione una de las opciones descritas en la tabla siguiente.  
  
    |**Nivel defecto**|**Descripción**|  
    |------------|-------------|  
    |Ninguno | No se utiliza ningún código de información.|  
    |Defecto | Los códigos se muestran en la tabla **Cód. defecto**. Estos códigos identifican defectos de productos de servicio o acciones que realizar en productos de servicio. Puede agrupar los códigos relacionados en agrupaciones de **Cód. área defecto**.|  
    |Defecto + Síntoma | Proporcione una combinación de códigos en las tablas **Cód. defecto** y **Cód. síntoma**. Los códigos de síntoma habituales incluyen indicadores que puede usar un cliente para describir un problema, como un ruido o calidad.|  
    |Defecto + Síntoma + Area | Utilice Cód. defecto, Cód. síntoma y Cód. área defecto, como implementación del sistema internacional de codificación de reparaciones (IRIS).|  
  
Para finalizar la configuración del informe de defectos, también puede especificar las reparaciones o resoluciones asociadas con un defecto. Se configura en la página **Relación códs. defecto/resol.**, donde se configuran combinaciones de códigos para el grupo de productos de servicio del producto de servicio desde el que se ha accedido a la ventana y el número de ocurrencias de cada uno.

## <a name="to-create-fault-and-resolution-code-relationships"></a>Para crear relaciones de códigos de defecto y resolución
<!--this needs to go in a working with topic-->
Para poder ver los métodos más habituales de reparación de determinados defectos de producto durante el servicio de los productos, deberá crear información acerca de las relaciones de códigos de defecto/resolución. Utilice el trabajo por lotes **Insertar relac. cód. def./res.** para buscar todas las combinaciones de códigos de defecto y resolución en los pedidos de servicio registrados y, a continuación, registrarlos en la página **Relac. códs. defecto/resol.** 
  
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Insertar relac. cód. def./res.** y, a continuación, seleccione el vínculo relacionado.  
2. Introduzca las fechas para definir el periodo que desea incluir en el proceso.  
3. Para agrupar las relaciones por grupos de producto de servicio, elija la casilla **Relación basada en grupo prod. serv.**.  
4. Para retener los registros que insertó manualmente en la página **Relaciones códigos defecto/resolución**, elija la casilla **Retiene registro insertado manualmente**.  

## <a name="see-also"></a>Consulte también
[Configurar la gestión de servicios](service-setup-service.md)  
[Gestión de servicios](service-service.md)  

