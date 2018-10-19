---
title: "Especificar cómo y cuándo recibir notificaciones | Documentos de Microsoft"
description: "Al configurar usuarios en los flujos de trabajo de aprobación, especifique en las ventanas Configuración de notificación y Programación de notificación cómo y cuándo cada usuario recibe las notificaciones sobre los pasos de flujo de aprobación. Los usuarios individuales pueden cambiar también su configuración de notificación eligiendo el botón Cambiar configuración de notificación en cualquier notificación."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 714ebd289407293f2a9fb8f05cad68330c79ad9a
ms.contentlocale: es-es
ms.lasthandoff: 09/28/2018

---
# <a name="specify-when-and-how-to-receive-notifications"></a>Especificar cómo y cuándo recibir notificaciones
Al configurar usuarios en los flujos de trabajo de aprobación, especifique en las ventanas **Configuración de notificación** y **Programación de notificación** cómo y cuándo cada usuario recibe las notificaciones sobre los pasos de flujo de aprobación. Los usuarios individuales pueden cambiar también su configuración de notificación eligiendo el botón **Cambiar configuración de notificación** en cualquier notificación.  

 Para poder configurar preferencias de notificación de un usuario de aprobación debe configurar el usuario como usuario de aprobación. Para obtener más información, [Configurar usuarios de aprobación](across-how-to-set-up-approval-users.md).  

 Se define el diseño y el contenido y de las notificaciones configurando plantillas de notificación. Para obtener más información, vea [Administrar las plantillas de notificación](across-how-to-manage-notification-templates.md).  

 Muchos pasos del flujo de trabajo de aprobación están relacionados con la notificación a los usuarios de un evento que se ha producido y en el que deben realizar una acción. Por ejemplo, en un paso del flujo de trabajo, el evento puede ser que el usuario 1 solicita la aprobación de un registro nuevo. La respuesta relacionada es que se envíe una notificación al usuario 2, el aprobador. En el siguiente paso del flujo de trabajo, el evento puede ser que el usuario 2 aprueba el registro. La respuesta relacionada es que se envíe una notificación al usuario 3 para iniciar un proceso con el registro aprobado. En el caso de los pasos del flujo de trabajo relacionados con la aprobación, cada notificación está vinculada a un movimiento de aprobación. Para obtener más información, consulte [Flujo de trabajo](across-workflow.md).  

## <a name="specify-when-and-how-users-receive-notifications"></a>Especificar cómo y cuándo los usuarios reciben notificaciones  

1.  Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Config. usuario aprobación** y luego elija el enlace relacionado.  
2.  Seleccione la línea del usuario para el que desea configurar las preferencias de notificación y, a continuación, elija la acción **Configuración de notificación**.  
3.  En la ventana **Configuración de notificación**, rellene los campos tal como se describe en la tabla siguiente.  

    |Campo|Description|  
    |---------------------------------|---------------------------------------|  
    |**Tipo de notificación**|Especifique el tipo de evento del que trata la notificación.<br /><br /> Seleccione una de las siguientes opciones:<br /><br /> -   **Nuevo registro** especifica que la notificación trata de un registro nuevo, como un documento, en el que el usuario debe realizar alguna acción.<br />-   **Aprobación** especifica que la notificación trata de una solicitud de aprobación o más.<br />-   **Vencidos** especifica que la notificación recuerda a los usuarios que se han retrasado para actuar en un evento.|  
    |**Código plantilla notificación**|Especifique el código de la plantilla de notificación que se utiliza para crear las notificaciones para el usuario.|  
    |**Notificaciones no agregadas**|Especifique si el usuario recibe una notificación para cada evento o notificaciones agregadas.<br /><br /> Si la casilla **Notificaciones no agregadas** no está seleccionada, el usuario recibe las notificaciones que agregan información sobre los eventos que se produzcan dentro del mismo modelo de periodicidad en la programación de la notificación.|  

     Ya ha especificado cómo recibe el usuario las notificaciones. Proceda a especificar cuándo recibe el usuario las notificaciones.  

4.  Elija la acción **Programación de notificación**.  
5.  En la ventana **Programación de notificación**, rellene los campos tal como se describe en la tabla siguiente.  

    |Campo|Description|  
    |---------------------------------|---------------------------------------|  
    |**Periodicidad**|Especifique el modelo de periodicidad en el que el usuario recibe las notificaciones.|  
    |**Hora**|Especifique a qué hora del día recibe notificaciones el usuario cuando el valor del campo **Periodicidad** no es **Inmediatamente**.|  
    |**Frecuencia diaria**|Especifique en qué tipo de días recibe el usuario las notificaciones cuando el valor del campo **Periodicidad** es **Diario**.<br /><br /> Seleccione **Día laborable** para recibir notificaciones cada día laborable de la semana. Seleccione **Diario** para recibir notificaciones cada día de la semana, incluso los fines de semana.|  
    |**Lunes** a **Domingo**|Especifique en qué tipo de días recibe el usuario las notificaciones cuando el valor del campo **Periodicidad** es **Semanal**.|  
    |**Fecha de mes**|Especifique si el usuario recibe notificaciones al principio del mes, al final o en una fecha específica.|  
    |**Fecha de notificación mensual**|Especifique la fecha del mes en las que el usuario recibe las notificaciones cuando el valor del campo **Fecha de mes** es **Personalizada**.|  

## <a name="change-when-and-how-you-receive-notifications"></a>Cambiar cómo y cuándo recibe notificaciones  
1.  En una de las notificaciones que ha recibido, en correo electrónico o nota, seleccione el botón **Cambiar configuración de notificación**.  
2.  En la ventana **Configuración de notificación**, cambie sus preferencias de notificación tal como se describe en el procedimiento anterior.  

## <a name="see-also"></a>Consulte también  
 [Configurar usuarios de aprobación](across-how-to-set-up-approval-users.md)   
 [Administrar las plantillas de notificación](across-how-to-manage-notification-templates.md)   
 [Configurar notificaciones de flujo de trabajo](across-setting-up-workflow-notifications.md)   
 [Configuración de flujos de trabajo](across-set-up-workflows.md)   
 [Uso de flujos de trabajo](across-use-workflows.md)

