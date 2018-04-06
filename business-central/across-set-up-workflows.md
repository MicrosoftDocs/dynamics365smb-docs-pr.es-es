---
title: Configurar flujos de trabajo | Documentos de Microsoft
description: "Puede configurar y utilizar flujos de trabajo que vinculen tareas de procesos empresariales realizadas por distintos usuarios. Las tareas de sistema, como registros automáticos, se pueden incluir como pasos en los flujos de trabajo, antes o después de las tareas de usuario. Solicitar y conceder aprobaciones para crear registros nuevos son pasos habituales de un flujo de trabajo."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 02/20/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: d2301b31308c1300961d78478ce1ada807eddeab
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="setting-up-workflows"></a>Configuración de flujos de trabajo
Puede configurar y utilizar flujos de trabajo que vinculen tareas de procesos empresariales realizadas por distintos usuarios. Las tareas de sistema, como registros automáticos, se pueden incluir como pasos en los flujos de trabajo, antes o después de las tareas de usuario. Solicitar y conceder aprobaciones para crear registros nuevos son pasos habituales de un flujo de trabajo. Para obtener más información, consulte [Uso de flujos de trabajo](across-use-workflows.md).  

 Antes de empezar a utilizar flujos de trabajo, debe configurar usuarios de flujo de trabajo y usuarios de aprobación, especificar cómo reciben los usuarios notificaciones sobre pasos del flujo de trabajo y, a continuación, crear los flujos de trabajo potencialmente precedidos por personalización del código.  

 En la ventana **Flujo de trabajo** creas un flujo de trabajo haciendo una lista de los pasos utilizados en las líneas. Cada paso consta de un evento del flujo de trabajo, moderado por condiciones de evento, y una respuesta de flujo de trabajo, moderada por las opciones de respuesta. Los pasos del flujo de trabajo se definen rellenando los campos de las líneas de flujo de trabajo en listas fijas de valores de evento y respuesta que representan los escenarios de flujo de trabajo que admite el código de aplicación.  

 Si una situación de negocio requiere un evento de flujo de trabajo o respuesta no compatibles, un asociado de Microsoft tiene que implementarlos personalizando el código de aplicación. Para obtener más información, consulte [Tutorial: Implementación de nuevos eventos y respuestas de flujo de trabajo](/dynamics-nav/Walkthrough--Implementing-New-Workflow-Events-and-Responses) en la ayuda para desarrolladores e informáticos.

 En la tabla siguiente se indican una serie de tareas con vínculos a los temas que las describen.  

|**Para**|**Consulte**|  
|------------|-------------|  
|Configurar usuarios de flujo de trabajo y grupos de usuarios.|[Configurar usuarios de flujo de trabajo](across-how-to-set-up-workflow-users.md)|  
|Configurar usuarios de flujo de trabajo que participan en flujos de trabajo de aprobación.|[Configurar usuarios de aprobación](across-how-to-set-up-approval-users.md)|  
|Especificar cómo se notifica a los usuarios del flujo de trabajo los pasos del flujo de trabajo, incluidas las solicitudes de aprobación.|[Configurar notificaciones de flujo de trabajo](across-setting-up-workflow-notifications.md)|  
|Especificar cuándo recibirán los usuarios las notificaciones y si agregar las notificaciones correspondientes a un periodo para minimizar el número de notificaciones.|[Especificar cómo y cuándo recibir notificaciones](across-how-to-specify-when-and-how-to-receive-notifications.md)|  
|Configurar la disposición y el contenido general de los mensajes de correo de notificaciones de nuevos flujos de trabajo o exportar, modificar y reimportar las plantillas existentes.|[Administrar las plantillas de notificación](across-how-to-manage-notification-templates.md)|  
|Configure un servidor SMTP para habilitar la comunicación de correo electrónico dentro y fuera de [!INCLUDE[d365fin](includes/d365fin_md.md)]|[Configurar correo electrónico](admin-how-setup-email.md)|
|Especificar los diferentes pasos de un flujo de trabajo por conexión de eventos de flujo de trabajo con respuestas de flujo de trabajo.|[Crear flujos de trabajo](across-how-to-create-workflows.md)|  
|Utilizar plantillas de flujo de trabajo para crear flujos de trabajo nuevos.|[Crear flujos de trabajo a partir de plantillas de flujo de trabajo](across-how-to-create-workflows-from-workflow-templates.md)|  
|Compartir flujos de trabajo con otras bases de datos de [!INCLUDE[d365fin](includes/d365fin_md.md)].|[Importar y exportar flujos de trabajo](across-how-to-export-and-import-workflows.md)|  
|Aprender a configurar un flujo de trabajo para documentos de venta aprobados siguiendo un procedimiento de extremo a extremo.|[Tutorial: Configuración y uso de un flujo de trabajo de aprobación de compra](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)|  
|Agregar compatibilidad con un escenario empresarial que necesita nuevos eventos y respuestas personalizando el código de aplicación.|[Tutorial: Implementación de nuevos eventos y respuestas de flujo de trabajo](/dynamics-nav/Walkthrough--Implementing-New-Workflow-Events-and-Responses)|  

## <a name="see-also"></a>Consulte también  
 [Uso de flujos de trabajo](across-use-workflows.md)   
 [Flujo de trabajo](across-workflow.md)   
 [Tutorial: Configuración y uso de un flujo de trabajo de aprobación de compra](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
 [Trabajar con Financials](ui-work-product.md)

