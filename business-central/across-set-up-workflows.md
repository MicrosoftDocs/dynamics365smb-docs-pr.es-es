---
title: Configurar flujos de trabajo (contiene vídeo)
description: Configure flujos de trabajo, usuarios de flujo de trabajo y usuarios de aprobación para conectar tareas del sistema de procesos de negocio realizadas por estos diferentes usuarios.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/11/2021
ms.author: edupont
ms.openlocfilehash: d9cf7f41f399d2747b554f3784c40b51fb9d71da
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2022
ms.locfileid: "8133257"
---
# <a name="set-up-workflows"></a>Configurar flujos de trabajo

Puede configurar y utilizar flujos de trabajo que vinculen tareas de procesos empresariales realizadas por distintos usuarios. Las tareas de sistema, como registros automáticos, se pueden incluir como pasos en los flujos de trabajo, antes o después de las tareas de usuario. Solicitar y conceder aprobaciones para crear registros nuevos son pasos habituales de un flujo de trabajo. Para obtener más información, consulte [Uso de flujos de trabajo](across-use-workflows.md).  

 Antes de empezar a utilizar flujos de trabajo, debe configurar usuarios de flujo de trabajo y usuarios de aprobación, especificar cómo reciben los usuarios notificaciones sobre pasos del flujo de trabajo y, a continuación, crear los flujos de trabajo potencialmente precedidos por personalización del código.  

 En la página **Flujo de trabajo** puede crear un flujo de trabajo haciendo una lista de los pasos utilizados en las líneas. Cada paso consta de un evento del flujo de trabajo, moderado por condiciones de evento, y una respuesta de flujo de trabajo, moderada por las opciones de respuesta. Los pasos del flujo de trabajo se definen rellenando los campos de las líneas de flujo de trabajo en listas fijas de valores de evento y respuesta que representan los escenarios de flujo de trabajo que admite el código de aplicación.  

 Si una situación de negocio requiere un evento de flujo de trabajo o respuesta no compatibles, un asociado de Microsoft tiene que implementarlos a través de código o puede configurar un flujo de trabajo mediante Power Automate. Para más información, ver [Utilizando [!INCLUDE[prod_short](includes/prod_short.md)] en un flujo de trabajo automatizado](across-how-use-financials-data-source-flow.md) o [Eventos en AL](/dynamics365/business-central/dev-itpro/developer/devenv-events-in-al) en la ayuda del desarrollador, respectivamente.

 En la tabla siguiente se indican una serie de tareas con vínculos a los temas que las describen.  

|**Para**|**Consulte**|  
|------------|-------------|  
|Configurar usuarios de flujo de trabajo y grupos de usuarios.|[Configurar usuarios de flujo de trabajo](across-how-to-set-up-workflow-users.md)|  
|Configurar usuarios de flujo de trabajo que participan en flujos de trabajo de aprobación.|[Configurar usuarios de aprobación](across-how-to-set-up-approval-users.md)|  
|Especificar cómo se notifica a los usuarios del flujo de trabajo los pasos del flujo de trabajo, incluidas las solicitudes de aprobación.|[Configurar notificaciones de flujo de trabajo](across-setting-up-workflow-notifications.md)|  
|Especifique si los usuarios reciben notificaciones por correo electrónico o nota, y con qué frecuencia se envían las notificaciones.|[Especificar cómo y cuándo recibir notificaciones](across-how-to-specify-when-and-how-to-receive-notifications.md)|  
|Personalice el contenido de la notificación por correo electrónico si modifica el informe 1320, Correo electrónico de notificación.|[Crear y modificar diseños de informe personalizados](ui-how-create-custom-report-layout.md)|  
|Configure un servidor SMTP para habilitar la comunicación de correo electrónico dentro y fuera de [!INCLUDE[prod_short](includes/prod_short.md)]|[Configurar correo electrónico](admin-how-setup-email.md)|
|Especificar los diferentes pasos de un flujo de trabajo por conexión de eventos de flujo de trabajo con respuestas de flujo de trabajo.|[Crear flujos de trabajo](across-how-to-create-workflows.md)|  
|Utilizar plantillas de flujo de trabajo para crear flujos de trabajo nuevos.|[Crear flujos de trabajo a partir de plantillas de flujo de trabajo](across-how-to-create-workflows-from-workflow-templates.md)|  
|Compartir flujos de trabajo con otras bases de datos de [!INCLUDE[prod_short](includes/prod_short.md)].|[Importar y exportar flujos de trabajo](across-how-to-export-and-import-workflows.md)|  
|Aprender a configurar un flujo de trabajo para documentos de venta aprobados siguiendo un procedimiento de extremo a extremo.|[Tutorial: Configuración y uso de un flujo de trabajo de aprobación de compra](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)|  

## <a name="example-of-an-approval-workflow"></a>Ejemplo de un flujo de trabajo de aprobación
Este video muestra cómo configurar un flujo de trabajo que requerirá que alguien solicite la aprobación de otra persona antes de que pueda cambiar la información sobre un cliente existente o crear un nuevo cliente.  
<br><br>  

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4jzHI?rel=0]

## <a name="see-also"></a>Consulte también  
 [Uso de flujos de trabajo](across-use-workflows.md)   
 [Flujo de trabajo](across-workflow.md)   
 [Tutorial: Configuración y uso de un flujo de trabajo de aprobación de compra](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
 [Trabajar con Business Central](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]