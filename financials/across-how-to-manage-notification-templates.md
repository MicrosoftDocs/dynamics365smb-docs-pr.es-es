---
title: "Administrar plantillas de notificación | Documentos de Microsoft"
description: "Las notificaciones se envían a los usuarios del flujo de trabajo para notificarles los pasos que deben realizar o informarles acerca del estado de los pasos del flujo de trabajo. Configure quién y cuándo recibe la notificación mediante la configuración de usuarios de aprobación, la programación de notificaciones de los usuarios y respuestas correspondientes del flujo de trabajo para definir al destinatario de las notificaciones. Para obtener más información, vea [Configuración de notificaciones de flujos de trabajo](across-setting-up-workflow-notifications.md)."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 9163bdb48a10d9b36b670e4bc67c696fbade6b37
ms.contentlocale: es-es
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-manage-notification-templates"></a>Procedimiento: Administrar las plantillas de notificación
Las notificaciones se envían a los usuarios del flujo de trabajo para notificarles los pasos que deben realizar o informarles acerca del estado de los pasos del flujo de trabajo. Configure quién y cuándo recibe la notificación mediante la configuración de usuarios de aprobación, la programación de notificaciones de los usuarios y respuestas correspondientes del flujo de trabajo para definir al destinatario de las notificaciones. Para obtener más información, consulte [Configurar notificaciones de flujo de trabajo](across-setting-up-workflow-notifications.md).  

 Las notificaciones se basan en las plantillas que definen el contenido y el diseño de la notificación. Puede exportar el contenido de una plantilla de notificación, editarla e importarla en la misma plantilla de notificación o en otra nueva. Esto se describe en los procedimientos siguientes:  

 La versión genérica de [!INCLUDE[d365fin](includes/d365fin_md.md)] contiene tres plantillas de notificación: una para notificar las solicitudes de aprobación, otra para notificar los nuevos registros y otra para notificar las solicitudes de aprobación vencidas. Las tres plantillas de notificación predefinidas admiten **Correo electrónico** y **Nota** como método de notificación. Para ver el contenido de las tres plantillas de notificación, vea la sección “Contenido de las plantillas de notificación” en este tema.

## <a name="to-create-a-new-notification-template"></a>Para crear una plantilla de notificación nueva  
1.  Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Plantillas de notificación** y, a continuación, seleccione el vínculo relacionado.  
2.  En la ventana **Plantillas de notificación**, elija la acción **Nuevo**.  
3.  Rellene los campos tal como se describe en la tabla siguiente.  

    |Campo|Description|  
    |---------------------------------|---------------------------------------|  
    |**Código**|Identifique la plantilla de notificación.|  
    |**Descripción**|Describa la plantilla de notificación.|  
    |**Método de notificación**|Especifique si la notificación se envía como un correo electrónico o como una nota.|  
    |**Escriba**|Especifique el proceso empresarial para el que se usará la notificación.<br /><br /> Seleccione uno de los siguientes tipos:<br /><br /> -   **Aprobación** especifica que la plantilla se utiliza para notificar a los usuarios en los flujos de trabajo de aprobación.<br />-   **Registro nuevo** especifica que la plantilla notificará a los aprobadores cuando un nuevo registro (por ejemplo, una ficha cliente) necesita su aprobación.<br />-   **Vencidos** especifica que la plantilla se utiliza para notificar a los usuarios las solicitudes de aprobación vencidas.|  
    |**Predet.**|Especifique si la plantilla de notificación se usará de forma predeterminada.|  

## <a name="to-modify-a-notification-template"></a>Para modificar una plantilla de notificación  
1.  Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Plantillas de notificación** y, a continuación, seleccione el vínculo relacionado.  
2.  En la ventana **Plantillas de notificación**, seleccione la plantilla de notificación que desea modificar.  
3.  Seleccione la acción **Exportar contenido de la plantilla**.  
4.  En la ventana **Exportar archivo**, seleccione el botón **Guardar** y, a continuación, asigne un nombre al archivo HTML y guárdelo en una ubicación adecuada.  
5.  Haga clic con el botón secundario en el archivo, seleccione **Abrir con** y, a continuación, elija el programa correspondiente.  

    > [!NOTE]  
    >  El contenido de las plantillas de notificación del tipo Correo electrónico están en formato HTML. El contenido de las plantillas de notificación del tipo Nota están en formato TXT.  
6.  Edite el contenido de la plantilla de notificación agregando, cambiando o quitando las variables de parámetro para definir el contenido que desee y, a continuación, guárdela. Para obtener más información, vea la sección “Contenido de las plantillas de notificación”.  

    Continúe con la importación del contenido modificado en la misma plantilla de notificación o en una nueva.  
7.  Para modificar la plantilla de notificación que ha exportado, en la ventana **Plantillas de notificación**, elija la plantilla seleccionada en el paso 2.  

    Además, para importar el contenido modificado de la plantilla en una nueva plantilla de notificación, siga el procedimiento “Para crear una plantilla de notificación nueva” y seleccione la nueva plantilla de notificación.  
8.  Seleccione la acción **Importar contenido de la plantilla**.  
9. Si está modificando una plantilla de notificación existente, elija el botón **Sí** en el mensaje acerca de la sobrescritura de la plantilla existente.  
10. En la ventana **Seleccionar un archivo para importar**, elija el archivo HTML que ha modificado en el paso 6 y, a continuación, seleccione el botón **Abrir**.  

La plantilla de notificación existente o nueva en la ventana **Plantillas de notificación** ahora se actualiza con el contenido modificado.  

### <a name="content-of-the-notification-templates"></a>Contenido de las plantillas de notificación  
Los tres tipos de plantilla de notificación, **Registro nuevo**, **Aprobación** y **Vencidos**, tienen contenido diferente.  

Los valores de parámetro se insertan automáticamente en las notificaciones según el tipo de plantilla de notificación.  

#### <a name="new-record"></a>Registro nuevo  
 ![NAV_notification_template_new_record](media/nav_notification_template_new_record.png "NAV_notification_template_new_record")  

#### <a name="approval"></a>Aprobación  
 ![NAV_notification_template_approval_type](media/nav_notification_template_approval_type.png "NAV_notification_template_approval_type")  

#### <a name="overdue"></a>Vencidos  
 ![NAV_notification_overdue_type](media/nav_notification_overdue_type.png "NAV_notification_overdue_type")  

## <a name="see-also"></a>Consulte también  
 [Configurar notificaciones de flujo de trabajo](across-setting-up-workflow-notifications.md)   
 [Configurar el correo electrónico](madeira-how-setup-email.md)   
 [Procedimiento: Configurar usuarios de flujo de trabajo](across-how-to-set-up-workflow-users.md)   
 [Procedimiento: Configurar usuarios de aprobación](across-how-to-set-up-approval-users.md)   
 [Procedimiento: Crear flujos de trabajo](across-how-to-create-workflows.md)   
 [Uso de colas de proyectos para programar tareas](admin-job-queues-schedule-tasks.md)   
 [Flujo de trabajo](across-workflow.md)   

