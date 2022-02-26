---
title: Configurar notificaciones de flujo de trabajo
description: Este tema le explica cómo configurar notificaciones de flujo de trabajo para alertar a un usuario de que ha ocurrido un evento al que debe reaccionar; se requiere una respuesta de flujo de trabajo.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.workload: na
ms.search.keywords: ''
ms.date: 06/11/2021
ms.author: edupont
ms.openlocfilehash: f0db9d63257d37fe6be5d31fc58541caf968907a
ms.sourcegitcommit: 04055135ff13db551dc74a2467a1f79d2953b8ed
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/08/2021
ms.locfileid: "7482437"
---
# <a name="workflow-notifications"></a>Notificaciones de flujo de trabajo

Configure sus flujos de trabajo para notificar automáticamente a los usuarios cuando se requiera su atención para un paso en ese flujo de trabajo. Muchas respuestas del flujo de trabajo corresponden a la notificación al usuario de un evento que se ha producido y en el que deben realizar una acción. Por ejemplo, en un paso del flujo de trabajo, el evento puede ser que el usuario 1 apruebe la solicitud de un registro nuevo y la respuesta que se envíe una notificación al usuario 2, el aprobador. En el siguiente paso del flujo de trabajo, el evento puede ser que el usuario 2 apruebe el registro y la respuesta que se envíe una notificación al usuario 3 para iniciar el procesamiento relacionado del registro aprobado. En el caso de los pasos del flujo de trabajo relacionados con la aprobación, cada notificación está vinculada a un movimiento de aprobación. Para obtener más información, consulte [Flujo de trabajo](across-workflow.md).  

> [!NOTE]  
> La versión genérica de [!INCLUDE[prod_short](includes/prod_short.md)] utiliza las notificaciones como correo electrónico y como notas internas.  

> [!IMPORTANT]  
> Todas las notificaciones de flujo de trabajo se envían a través de una cola de proyectos. Asegúrese de que la cola de proyectos en la instalación está configurada para gestionar las notificaciones de flujo de trabajo, así como que la casilla **Iniciar automáticamente desde servidor** esté seleccionada. Para obtener más información, consulte [Uso de colas de proyectos para programar tareas](admin-job-queues-schedule-tasks.md).

## <a name="set-up-notifications"></a>Configuración de notificaciones

Se configuran distintos aspectos de las notificaciones de flujo de trabajo en los lugares siguientes:  

* Notificación de aprobador

    Para los flujos de trabajo de aprobación, configure los destinatarios de las notificaciones del flujo de trabajo rellenando una línea en la página **Config. usuario aprobación** para cada usuario que participe en el flujo de trabajo.  

    Por ejemplo, si se ha especificado el usuario 2 en el campo **Id. aprobador** en la línea del usuario 1, la notificación de solicitud de aprobación se envía el usuario 1. Para obtener más información, vea . Para obtener más información, vea [Configurar usuarios de aprobación](across-how-to-set-up-approval-users.md).  
* Programaciones de notificación

    Para definir cuándo y cómo los usuarios reciben notificaciones de flujo de trabajo debe rellenarse la página **Programación de notificación** para cada usuario del flujo de trabajo. Para obtener más información, consulte [Especificar cómo y cuándo recibir notificaciones](across-how-to-specify-when-and-how-to-receive-notifications.md).  
* Personalizar las notificaciones por correo electrónico

    Si lo desea, puede personalizar el contenido de la notificación por correo electrónico si modifica el informe 1320, Correo electrónico de notificación. Para obtener más información, vea [Crear y modificar diseños de informe personalizados](ui-how-create-custom-report-layout.md).  

    > [!NOTE]
    > Si desea utilizar el correo electrónico como método de notificación, debe configurarlo para el remitente y para el destinatario en[!INCLUDE [prod_short](includes/prod_short.md)]. Para obtener más información, consulte [Configurar correo electrónico](admin-how-setup-email.md).

* Opciones de respuesta

    Deberá configurarse el contenido específico y las reglas para una notificación de flujo de trabajo al crear el flujo de trabajo en cuestión. Para ello, seleccione las opciones correspondientes en la página **Opciones de respuesta de flujo de trabajo** para la respuesta de flujo de trabajo que represente la notificación. Para obtener más información, consulte el paso 9 en [Crear flujos de trabajo](across-how-to-create-workflows.md).  

* Notificar al remitente

    Para los flujos de trabajo de aprobación, agregue un paso de respuesta de flujo de trabajo para notificar al remitente cuando su solicitud se ha aprobado o rechazado. Para obtener más información, consulte el paso 9 en [Crear flujos de trabajo](across-how-to-create-workflows.md).  

## <a name="see-also"></a>Consulte también

[Configurar usuarios de aprobación](across-how-to-set-up-approval-users.md)  
[Configurar usuarios de flujo de trabajo](across-how-to-set-up-workflow-users.md)  
[Especificar cómo y cuándo recibir notificaciones](across-how-to-specify-when-and-how-to-receive-notifications.md)  
[Crear flujos de trabajo](across-how-to-create-workflows.md)  
[Crear y modificar diseños de informe personalizados](ui-how-create-custom-report-layout.md)  
[Uso de colas de proyectos para programar tareas](admin-job-queues-schedule-tasks.md)  
[Configurar correo electrónico](admin-how-setup-email.md)  
[Tutorial: Configuración y uso de un flujo de trabajo de aprobación de compra](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Flujo de trabajo](across-workflow.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]