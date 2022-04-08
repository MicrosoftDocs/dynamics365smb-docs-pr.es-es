---
title: Flujos de trabajo en Dynamic 365 Business Central
description: Utilice flujos de trabajo para conectar tareas de procesos empresariales realizadas por distintos usuarios. Las tareas del sistema, como la publicación automática, se pueden incluir como pasos del flujo de trabajo.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/11/2021
ms.author: edupont
ms.openlocfilehash: 9cfdcc9bbf8e24675c6894b8ca2efbf10129d990
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2022
ms.locfileid: "8511186"
---
# <a name="workflows-in-dynamics-365-business-central"></a>Flujos de trabajo en Dynamics 365 Business Central

Puede configurar y utilizar flujos de trabajo que vinculen tareas de procesos empresariales realizadas por distintos usuarios. Las tareas de sistema, como registros automáticos, se pueden incluir como pasos en los flujos de trabajo, antes o después de las tareas de usuario. Solicitar y conceder aprobaciones para crear registros nuevos son pasos habituales de un flujo de trabajo.  

 En la página **Flujo de trabajo** puede crear un flujo de trabajo haciendo una lista de los pasos utilizados en las líneas. Cada paso consta de un evento del flujo de trabajo, moderado por condiciones de evento, y una respuesta de flujo de trabajo, moderada por las opciones de respuesta. Los pasos del flujo de trabajo se definen rellenando los campos de las líneas de flujo de trabajo en listas fijas de valores de evento y respuesta que representan los escenarios de flujo de trabajo que admite el código de aplicación.  

 La versión genérica de [!INCLUDE[prod_short](includes/prod_short.md)] incluye un número de flujos de trabajo preconfigurados que están representados por plantillas de flujo de trabajo que puede copiar para crear flujos de trabajo. El código para las plantillas de flujo de trabajo agregadas por Microsoft llevan el prefijo “MS-“. Para más información, consulta las plantillas de la lista de flujo de trabajo en la página Plantillas de flujo de trabajo.  

 Si una situación de negocio requiere un evento de flujo de trabajo o respuesta no compatibles, puede utilizar Power Automate o trabajar con un socio de Microsoft para personalizar el código de aplicación. Para obtener más información, consulte [Usar [!INCLUDE[prod_short](includes/prod_short.md)] en un flujo de trabajo automatizado](across-how-use-financials-data-source-flow.md).

Cualquier plantilla de flujo de trabajo que cree con Power Automate se agrega a la lista de plantillas de flujo de trabajo en [!INCLUDE[prod_short](includes/prod_short.md)]. Para obtener más información, consulte [Usar Business Central en un flujo de trabajo automatizado](across-how-use-financials-data-source-flow.md).  

 En la tabla siguiente se indican una serie de tareas con vínculos a los temas que las describen.  

|**Para**|**Consulte**|  
|------------|-------------|  
|Configure usuarios de flujo de trabajo, especifique cómo reciben notificaciones los usuarios y cree nuevos flujos de trabajo. Para nuevos flujos de trabajo en situaciones no compatibles, implemente los elementos de flujo de trabajo necesarios personalizando el código de aplicación.|[Configuración de flujos de trabajo](across-set-up-workflows.md)|  
|Habilite flujos de trabajo, actúe al recibir notificaciones de flujos de trabajo, incluida la aprobación de solicitudes, para realizar un paso del flujo de trabajo. Archive y elimine flujos de trabajo.|[Usar flujos de trabajo](across-use-workflows.md)|  

## <a name="see-also"></a>Consulte también

[Ccial](sales-manage-sales.md)  
[Compras](purchasing-manage-purchasing.md)  
[Administrar proyectos](projects-manage-projects.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]