---
title: Flujos de trabajo en Dynamic 365 Business Central
description: Use las capacidades de flujo de trabajo integradas para configurar flujos de trabajo de aprobación para complementar los flujos de trabajo automatizados basados en Power Automate. Puede configurar pasos para asignar tareas a diferentes personas como parte de las diferentes tareas del proceso empresarial.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 05/12/2022
ms.author: edupont
ms.openlocfilehash: 84d4a87a0edab18be342b9ed5732de0350a31645
ms.sourcegitcommit: bc645e7ecb1940a85b2c433aa894d3494c9b10df
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2022
ms.locfileid: "8743676"
---
# <a name="workflows-in-dynamics-365-business-central"></a>Flujos de trabajo en Dynamics 365 Business Central

Puede configurar y utilizar flujos de trabajo que vinculen tareas de procesos empresariales realizadas por distintos usuarios. Las tareas de sistema, como registros automáticos, se pueden incluir como pasos en los flujos de trabajo, antes o después de las tareas de usuario. Solicitar y conceder aprobaciones para crear registros nuevos son pasos habituales de un flujo de trabajo.  

La versión predeterminada de [!INCLUDE [prod_short](includes/prod_short.md)] admite tres tipos de flujos de trabajo:

* Flujos de trabajo de aprobación automatizados basados en plantillas de flujo de trabajo integradas  

  En la página **Plantillas de flujo de trabajo**, puede ver todos los flujos de trabajo disponibles. La versión de prueba de [!INCLUDE[prod_short](includes/prod_short.md)] incluye un número de flujos de trabajo preconfigurados que están representados por plantillas de flujo de trabajo que puede copiar para crear flujos de trabajo. Cuando abre una plantilla de flujo de trabajo desde la página **Plantillas de flujo de trabajo** y el nombre del flujo de trabajo comienza por *MS-*, Microsoft agrega la plantilla de flujo de trabajo.  
* Flujos automatizados que usted mismo configura  

  Cualquier plantilla de flujo de trabajo que cree con Power Automate se agrega a la lista de plantillas de flujo de trabajo en [!INCLUDE[prod_short](includes/prod_short.md)]. Para obtener más información, consulte [Usar Business Central en flujos de Power Automate](across-how-use-financials-data-source-flow.md).  
* Flujos activados manualmente desde la acción **Automatizar** (solo en [!INCLUDE [prod_short](includes/prod_short.md)] en línea). Para obtener más información, consulte [Flujos instantáneos manuales](across-how-use-financials-data-source-flow.md#manual-instant-flows).  

## <a name="power-automate-flows"></a>Flujos de Power Automate

Para [!INCLUDE [prod_short](includes/prod_short.md)] en línea, puede registrarse en Power Automate y luego crear potentes flujos automatizados que puede ejecutar desde dentro de [!INCLUDE [prod_short](includes/prod_short.md)]. Para obtener más información, consulte [Usar [!INCLUDE[prod_short](includes/prod_short.md)] en flujos de Power Automate](across-how-use-financials-data-source-flow.md).  

## <a name="automated-approval-workflows"></a>Flujos de trabajo de aprobación automatizados

Puede crear un flujo de trabajo de aprobación haciendo una lista de los pasos utilizados en las líneas. Cada paso consta de un evento del flujo de trabajo, moderado por condiciones de evento, y una respuesta de flujo de trabajo, moderada por las opciones de respuesta. Los pasos del flujo de trabajo se definen rellenando los campos de las líneas de flujo de trabajo en listas fijas de valores de evento y respuesta que representan los escenarios de flujo de trabajo que admite el código de aplicación.  

Si un escenario empresarial requiere un evento de flujo de trabajo o una respuesta que no se admite en la versión predeterminada, regístrese en Power Automate. Para obtener más información, consulte [Usar [!INCLUDE[prod_short](includes/prod_short.md)] en flujos de Power Automate](across-how-use-financials-data-source-flow.md). Alternativamente, obtenga una aplicación o trabaje con un socio de Microsoft para personalizar el código de la aplicación.  

Para configurar y usar flujos de trabajo que no están definidos en Power Automate, consulte los siguientes artículos:  

|**Para**|**Vea**|  
|------------|-------------|  
|Configure usuarios de flujo de trabajo, especifique cómo reciben notificaciones los usuarios y cree nuevos flujos de trabajo. Para nuevos flujos de trabajo en situaciones no compatibles, implemente los elementos de flujo de trabajo necesarios personalizando el código de aplicación.|[Configurar flujos de trabajo](across-set-up-workflows.md)|  
|Habilite flujos de trabajo, actúe al recibir notificaciones de flujos de trabajo, incluida la aprobación de solicitudes, para realizar un paso del flujo de trabajo. Archive y elimine flujos de trabajo.|[Usar flujos de trabajo](across-use-workflows.md)|  

## <a name="see-also"></a>Consulte también

[Ccial](sales-manage-sales.md)  
[Compras](purchasing-manage-purchasing.md)  
[Administrar proyectos](projects-manage-projects.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Usar [!INCLUDE[prod_short](includes/prod_short.md)] en flujos de Power Automate](across-how-use-financials-data-source-flow.md)  
[Solucionar problemas de sus [!INCLUDE[prod_short](includes/prod_short.md)] flujos de trabajo automatizados](across-flow-troubleshoot.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]