---
title: Administrar plantillas de notificación | Documentos de Microsoft
description: Las notificaciones se envían a los usuarios del flujo de trabajo para notificarles los pasos que deben realizar o informarles acerca del estado de los pasos del flujo de trabajo. Configure quién y cuándo recibe la notificación mediante la configuración de usuarios de aprobación, la programación de notificaciones de los usuarios y respuestas correspondientes del flujo de trabajo para definir al destinatario de las notificaciones.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: across-how-to-specify-when-and-how-to-receive-notifications
ms.openlocfilehash: 562664ad0fd443c3363d103572022e6d819ed357
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2019
ms.locfileid: "914283"
---
# <a name="manage-notification-templates"></a>Administrar las plantillas de notificación
Las notificaciones se envían a los usuarios del flujo de trabajo para notificarles los pasos que deben realizar o informarles acerca del estado de los pasos del flujo de trabajo. Configure quién y cuándo recibe la notificación mediante la configuración de usuarios de aprobación, la programación de notificaciones de los usuarios y respuestas correspondientes del flujo de trabajo para definir al destinatario de las notificaciones. Para obtener más información, consulte [Configurar notificaciones de flujo de trabajo](across-setting-up-workflow-notifications.md).  

 Las notificaciones se basan en las plantillas que definen el contenido y el diseño de la notificación. Puede exportar el contenido de una plantilla de notificación, editarla e importarla en la misma plantilla de notificación o en otra nueva. Esto se describe en los procedimientos siguientes:  

 La versión genérica de [!INCLUDE[d365fin](includes/d365fin_md.md)] contiene tres plantillas de notificación: una para notificar las solicitudes de aprobación, otra para notificar los nuevos registros y otra para notificar las solicitudes de aprobación vencidas. Las tres plantillas de notificación predefinidas admiten **Correo electrónico** y **Nota** como método de notificación. Para ver el contenido de las tres plantillas de notificación, vea la sección “Contenido de las plantillas de notificación” en este tema.

## <a name="to-create-a-new-notification-template"></a>Para crear una plantilla de notificación nueva  
1.  Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Plantillas de notificación** y luego elija el enlace relacionado.  
2.  En la página **Plantillas de notificación**, elija la acción **Nuevo**.  
3.  Rellene los campos tal como se describe en la tabla siguiente.  

    |Campo|Description|  
    |---------------------------------|---------------------------------------|  
    |**Código**|Identifique la plantilla de notificación.|  
    |**Descripción**|Describa la plantilla de notificación.|  
    |**Método de notificación**|Especifique si la notificación se envía como un correo electrónico o como una nota.|  
    |**Escriba**|Especifique el proceso empresarial para el que se usará la notificación.<br /><br /> Seleccione uno de los siguientes tipos:<br /><br /> -   **Aprobación** especifica que la plantilla se utiliza para notificar a los usuarios en los flujos de trabajo de aprobación.<br />-   **Registro nuevo** especifica que la plantilla notificará a los aprobadores cuando un nuevo registro (por ejemplo, una ficha cliente) necesita su aprobación.<br />-   **Vencidos** especifica que la plantilla se utiliza para notificar a los usuarios las solicitudes de aprobación vencidas.|  
    |**Predet.**|Especifique si la plantilla de notificación se usará de forma predeterminada.|  

## <a name="to-modify-a-notification-template"></a>Para modificar una plantilla de notificación  
1.  Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Plantillas de notificación** y luego elija el enlace relacionado.  
2.  En la página **Plantillas de notificación**, seleccione la plantilla de notificación que desea modificar.  
3.  Seleccione la acción **Exportar contenido de la plantilla**.  
4.  En la página **Exportar archivo**, seleccione el botón **Guardar** y, a continuación, asigne un nombre al archivo HTML y guárdelo en una ubicación adecuada.  
5.  Haga clic con el botón secundario en el archivo, seleccione **Abrir con** y, a continuación, elija el programa correspondiente.  

    > [!NOTE]  
    >  El contenido de las plantillas de notificación del tipo Correo electrónico están en formato HTML. El contenido de las plantillas de notificación del tipo Nota están en formato TXT.  
6.  Edite el contenido de la plantilla de notificación agregando, cambiando o quitando las variables de parámetro para definir el contenido que desee y, a continuación, guárdela. Para obtener más información, vea la sección “Contenido de las plantillas de notificación”.  

    Continúe con la importación del contenido modificado en la misma plantilla de notificación o en una nueva.  
7.  Para modificar la plantilla de notificación que ha exportado, en la página **Plantillas de notificación**, elija la plantilla seleccionada en el paso 2.  

    Además, para importar el contenido modificado de la plantilla en una nueva plantilla de notificación, siga el procedimiento “Para crear una plantilla de notificación nueva” y seleccione la nueva plantilla de notificación.  
8.  Seleccione la acción **Importar contenido de la plantilla**.  
9. Si está modificando una plantilla de notificación existente, elija el botón **Sí** en el mensaje acerca de la sobrescritura de la plantilla existente.  
10. En la página **Seleccionar un archivo para importar**, elija el archivo HTML que ha modificado en el paso 6 y, a continuación, seleccione el botón **Abrir**.  

La plantilla de notificación existente o nueva en la página **Plantillas de notificación** ahora se actualiza con el contenido modificado.  

### <a name="content-of-the-notification-templates"></a>Contenido de las plantillas de notificación  
Los tres tipos de plantilla de notificación, **Registro nuevo**, **Aprobación** y **Vencidos**, tienen contenido diferente.  

Los valores de parámetro se insertan automáticamente en las notificaciones según el tipo de plantilla de notificación.  

#### <a name="new-record"></a>Registro nuevo  
 ![NAV&#95;notification&#95;template&#95;new&#95;record&#95;type](media/nav_notification_template_new_record.png "NAV_notification_template_new_record")  

#### <a name="approval"></a>Aprobación  
 ![NAV&#95;notification&#95;template&#95;approval&#95;type](media/nav_notification_template_approval_type.png "NAV_notification_template_approval_type")  

#### <a name="overdue"></a>Vencidos  
 ![NAV&#95;notification&#95;overdue&#95;type](media/nav_notification_overdue_type.png "NAV_notification_overdue_type")  

## <a name="see-also"></a>Consulte también  
 [Configurar notificaciones de flujo de trabajo](across-setting-up-workflow-notifications.md)   
 [Configurar correo electrónico](admin-how-setup-email.md)   
 [Configurar usuarios de flujo de trabajo](across-how-to-set-up-workflow-users.md)   
 [Configurar usuarios de aprobación](across-how-to-set-up-approval-users.md)   
 [Crear flujos de trabajo](across-how-to-create-workflows.md)   
 [Uso de colas de proyectos para programar tareas](admin-job-queues-schedule-tasks.md)   
 [Flujo de trabajo](across-workflow.md)   
