---
title: Configurar horas de trabajo y de servicio | Documentos de Microsoft
description: Puede especificar las horas de servicio habituales de la empresa. Estas horas de servicio se utilizarán para calcular la fecha y tiempo de respuesta de pedidos y ofertas de servicio y para enviar advertencias de tiempo de respuesta.
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
ms.openlocfilehash: 223d69df17dad2a1309d333fc64be8b208262530
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/08/2019
ms.locfileid: "806408"
---
# <a name="set-up-work-hours-and-service-hours"></a>Configurar horas de trabajo y de servicio
Normalmente, un sistema de gestión de servicios realiza un seguimiento de horas de recursos y del estado del pedido de servicio para prever cargas de trabajo y necesidades de servicio. [!INCLUDE[d365fin](includes/d365fin_md.md)] incorpora herramientas que puede personalizar para registrar este tipo de información.  
  
Una vez configuradas las horas de servicio predeterminadas de su empresa, puede calcular tiempos de respuesta para pedidos de servicio o enviar advertencias o alertas cuando entran llamadas de servicio. La función de alerta se implementa de manera conjunta con el planificador de tareas.   
  
A medida que trabaje en un pedido de servicio, querrá actualizar su estado para poder controlar el progreso. El estado de pedido de servicio indica el estado de reparación de todos los productos de servicio del pedido de servicio. Para obtener más información, vea [Comprensión de pedido de servicio y estado de reparación](service-order-repair-status.md). 

## <a name="to-set-up-default-service-hours"></a>Para configurar horas de servicio genéricas  
La página **Horas servicio genér.** sirve para configurar las horas de servicio habituales de la empresa. Estas horas de servicio se utilizarán para calcular la fecha y tiempo de respuesta de pedidos y ofertas de servicio y para enviar advertencias de tiempo de respuesta. Las horas de servicio genéricas se utilizarán para contratos de servicio, a no ser que especifique horas de servicio especiales para un contrato.  
  
1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Horas de serv. predeterminadas** y luego elija el enlace relacionado.  
2. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
  
> [!IMPORTANT]  
>  Si deja vacías las líneas de la página **Horas servicio genér.**, el valor predeterminado será 24 horas, válido sólo para el calendario de días laborables.  
  
## <a name="to-set-up-work-hour-templates"></a>Para configurar plantillas de trabajo-hora
La página **Plantilla trabajo-hora** sirve para configurar plantillas que contienen las horas de trabajo habituales de la empresa. Por ejemplo, puede crear plantillas para técnicos empleados a tiempo completo y para técnicos empleados a tiempo parcial. Puede utilizar plantillas de horas de trabajo al añadir capacidad a recursos.  
  
1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Plantillas trabajo-hora** y luego elija el enlace relacionado.  
2. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
  
> [!Note]
> Una vez introducidas las horas de trabajo de cada día, el valor del campo **Total por semana** se calculará automáticamente.  

## <a name="to-set-up-contract-specific-service-hours"></a>Para configurar horas de servicio específicas de contrato  
Puede utilizar la página **Horas servicio** para configurar horas de servicio específicas para el cliente propietario del contrato de servicio. Las horas de servicio se utilizarán para calcular la fecha y el tiempo de respuesta de pedidos y ofertas de servicio que pertenezcan al contrato de servicio.  
  
Si no configura horas de servicio específicas para un contrato de servicio, se utilizarán las horas de servicio genéricas para los contratos de servicio.  
  
1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Contratos servicio** y luego elija el enlace relacionado.  
2. Abra el contrato de servicio para el que desee configurar horas de servicio específicas y elija **Horas servicio**.  
4. Para configurar horas de servicio basadas en horas de servicio genéricas, elija la acción **Copiar horas serv. genéricas**.  
5. Modifique los campos de los movimientos de horas de servicio. Inserte o elimine los movimientos para establecer las horas de servicio para el contrato. Tenga en cuenta que los campos **Día**, **Hora de inicio** y **Hora final** son obligatorios para cada movimiento.  
6. Si desea que las horas de servicio sean válidas desde una fecha concreta, rellene el campo **Fecha inicial**.  
7. Si desea que las horas de servicio sean válidas en vacaciones, active el campo **Válido en festivos**.  

## <a name="see-also"></a>Consulte también  
[Descripción del estado de asignación y estado de reparación](service-allocation-status-and-repair-status.md)  
[Configurar la gestión de servicios](service-setup-service.md)  
[Descripción del estado de pedido de servicio y de reparación](service-order-repair-status.md)  
