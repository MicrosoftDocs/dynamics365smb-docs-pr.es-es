---
title: Configurar notificaciones de flujo de trabajo de aprobación
description: Este artículo le explica cómo configurar notificaciones de flujo de trabajo para alertar a un usuario de que ha ocurrido un evento al que debe reaccionar; se requiere una respuesta de flujo de trabajo.
author: brentholtorf
ms.topic: conceptual
ms.workload: na
ms.search.keywords: null
ms.date: 09/13/2022
ms.author: bholtorf
---
# Notificaciones de flujo de trabajo de aprobación

Configure sus flujos de trabajo para notificar automáticamente a los usuarios cuando se requiera su atención para un paso en un flujo de trabajo. Muchas respuestas del flujo de trabajo corresponden a la notificación al usuario de un evento que se ha producido y en el que deben realizar una acción.

Por ejemplo, puede establecer que el Usuario 2, el usuario aprobador, reciba una notificación cada vez que el Usuario 1 solicite la aprobación de un nuevo registro. En el siguiente paso del flujo de trabajo, después de que el usuario 2 apruebe el registro, el usuario 3 recibirá una notificación y podrá iniciar el procesamiento relacionado con el registro. Con los pasos del flujo de trabajo de aprobación, cada notificación está vinculada a un movimiento de aprobación. Obtenga más información en [Flujo de trabajo](across-workflow.md).  

> [!NOTE]  
> La versión predeterminada de [!INCLUDE[prod_short](includes/prod_short.md)] utiliza las notificaciones como correo electrónico o como notas internas.  

> [!IMPORTANT]  
> Todas las notificaciones de flujo de trabajo se envían a través de una cola de proyectos. Asegúrese de que la cola de proyectos en la instalación está configurada para gestionar las notificaciones de flujo de trabajo, así como que se haya seleccionado la casilla **Iniciar automáticamente desde servidor**. Obtenga más información en [Uso de colas de proyectos para programar tareas](admin-job-queues-schedule-tasks.md).

## Configuración de notificaciones

Puede configurar distintos aspectos de las notificaciones de flujo de trabajo en los lugares siguientes:  

* Notificación de aprobador

  Para los flujos de trabajo de aprobación, configure los destinatarios de las notificaciones del flujo de trabajo rellenando una línea en la página **Config. usuario aprobación** para cada usuario que participe en el flujo de trabajo.  

  Por ejemplo, si se ha especificado el usuario 2 en el campo **Id. aprobador** en la línea del usuario 1, la notificación de solicitud de aprobación se envía el usuario 2. Para obtener más información, vea . Obtenga más información en [Configurar usuarios de aprobación](across-how-to-set-up-approval-users.md). 
  
* Programaciones de notificación

  Para definir cuándo y cómo los usuarios reciben notificaciones de flujo de trabajo debe rellenarse la página **Programación de notificación** para cada usuario del flujo de trabajo. Obtenga más información en [Especificar cómo y cuándo recibir notificaciones](across-how-to-specify-when-and-how-to-receive-notifications.md). 
  
* Personalizar las notificaciones por correo electrónico

  Si lo desea, puede personalizar el contenido de la notificación por correo electrónico si modifica el informe 1320, Correo electrónico de notificación. Obtenga más información en [Crear y modificar diseños de informe personalizados](ui-how-create-custom-report-layout.md).  

  > [!NOTE]
  > Si desea utilizar el correo electrónico como método de notificación, debe configurarlo para el remitente y para el destinatario en[!INCLUDE [prod_short](includes/prod_short.md)]. Obtenga más información en [Configurar correo electrónico](admin-how-setup-email.md).
  
* Opciones de respuesta

  Configure el contenido específico y las reglas de una notificación de flujo de trabajo cuando cree el flujo de trabajo en cuestión. Seleccione las opciones de personalización en la página **Respuestas de flujo de trabajo** para la respuesta de flujo de trabajo que represente la notificación. Obtenga más información del paso 9 en la sección [Crear flujos de trabajo](across-how-to-create-workflows.md#to-create-a-workflow). 
  
* Notificar al remitente

  Para los flujos de trabajo de aprobación, agregue un paso de respuesta de flujo de trabajo para notificar al remitente cuando su solicitud se ha aprobado o rechazado. Obtenga más información del paso 9 en la sección [Crear flujos de trabajo](across-how-to-create-workflows.md#to-create-a-workflow).   

## Consulte también .

[Configurar usuarios de aprobación](across-how-to-set-up-approval-users.md)  
[Configurar usuarios de flujo de trabajo](across-how-to-set-up-workflow-users.md)  
[Especificar cómo y cuándo recibir notificaciones](across-how-to-specify-when-and-how-to-receive-notifications.md)  
[Crear flujos de trabajo de aprobación](across-how-to-create-workflows.md)  
[Crear y modificar diseños de informe personalizados](ui-how-create-custom-report-layout.md)  
[Uso de colas de proyectos para programar tareas](admin-job-queues-schedule-tasks.md)  
[Configurar correo electrónico](admin-how-setup-email.md)  
[Tutorial: Configuración y uso de un flujo de trabajo de aprobación de compra](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Flujo de trabajo](across-workflow.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
