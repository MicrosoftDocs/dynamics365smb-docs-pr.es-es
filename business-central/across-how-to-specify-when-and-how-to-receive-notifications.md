---
title: Especificar cómo y cuándo recibir notificaciones | Documentos de Microsoft
description: Al configurar usuarios en los flujos de trabajo de aprobación, especifique en las páginas Configuración de notificación y Programación de notificación cómo y cuándo cada usuario recibe las notificaciones sobre los pasos de flujo de aprobación. Los usuarios individuales pueden cambiar también su configuración de notificación eligiendo el botón Cambiar configuración de notificación en cualquier notificación.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 7ae55ba1c1aa0d2f10d1529dbf82b47022d3d9d5
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2020
ms.locfileid: "3916298"
---
# <a name="specify-when-and-how-to-receive-notifications"></a>Especificar cómo y cuándo recibir notificaciones
Al configurar usuarios en los flujos de trabajo de aprobación, especifique en las páginas **Configuración de notificación** y **Programación de notificación** cómo y cuándo cada usuario recibe las notificaciones sobre los pasos de flujo de aprobación. Los usuarios individuales pueden cambiar también su configuración de notificación eligiendo el botón **Cambiar configuración de notificación** en cualquier notificación.  

> [!NOTE]
> Las notificaciones se entregan de acuerdo con la configuración de notificaciones del receptor, no del remitente. Es una distinción importante porque significa que, cuando alguien solicita una aprobación como parte de un flujo de trabajo, su solicitud no se envía necesariamente de inmediato. En cambio, se entregará de acuerdo con la configuración de notificaciones de los aprobadores. 

 Para poder configurar preferencias de notificación de un usuario de aprobación debe configurar el usuario como usuario de aprobación. Para obtener más información, [Configurar usuarios de aprobación](across-how-to-set-up-approval-users.md).  

 Puede definir el diseño de las notificaciones por correo electrónico personalizando el informe 1320, Correo electrónico de notificación. Para obtener más información, vea [Crear y modificar diseños de informe personalizados](ui-how-create-custom-report-layout.md).  

 Muchos pasos del flujo de trabajo de aprobación están relacionados con la notificación a los usuarios de un evento que se ha producido y en el que deben realizar una acción. Por ejemplo, en un paso del flujo de trabajo, el evento puede ser que el usuario 1 solicita la aprobación de un registro nuevo. La respuesta relacionada es que se envíe una notificación al usuario 2, el aprobador. En el siguiente paso del flujo de trabajo, el evento puede ser que el usuario 2 aprueba el registro. La respuesta relacionada es que se envíe una notificación al usuario 3 para iniciar un proceso con el registro aprobado. En el caso de los pasos del flujo de trabajo relacionados con la aprobación, cada notificación está vinculada a un movimiento de aprobación. Para obtener más información, consulte [Flujo de trabajo](across-workflow.md).  

## <a name="specify-when-and-how-users-receive-notifications"></a>Especificar cómo y cuándo los usuarios reciben notificaciones  

1.  Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Config. usuario aprobación** y luego elija el enlace relacionado.  
2.  Seleccione la línea del usuario para el que desea configurar las preferencias de notificación y, a continuación, elija la acción **Configuración de notificación**.  
3.  En la página **Configuración de notificación**, rellene los campos tal como se describe en la tabla siguiente.  

    |Campo|Description|  
    |---------------------------------|---------------------------------------|  
    |**Tipo de notificación**|Especifique el tipo de evento del que trata la notificación.<br /><br /> Seleccione una de las siguientes opciones:<br /><br /> -   **Nuevo registro** especifica que la notificación trata de un registro nuevo, como un documento, en el que el usuario debe realizar alguna acción.<br />-   **Aprobación** especifica que la notificación trata de una solicitud de aprobación o más.<br />-   **Vencidos** especifica que la notificación recuerda a los usuarios que se han retrasado para actuar en un evento.|  
    |**Método de notificación**|Especifique si la notificación es un correo electrónico o una nota interna.|

    Puede definir el diseño de las notificaciones por correo electrónico personalizando el informe 1320, Correo electrónico de notificación. Para obtener más información, vea [Crear y modificar diseños de informe personalizados](ui-how-create-custom-report-layout.md).

    Ya ha especificado cómo recibe el usuario las notificaciones. Proceda a especificar cuándo recibe el usuario las notificaciones.  

4.  Elija la acción **Programación de notificación**.  
5.  En la página **Programación de notificación**, rellene los campos tal como se describe en la tabla siguiente.  

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
2.  En la página **Configuración de notificación**, cambie sus preferencias de notificación tal como se describe en el procedimiento anterior.  

## <a name="see-also"></a>Consulte también  
 [Configurar usuarios de aprobación](across-how-to-set-up-approval-users.md)   
 [Crear y modificar diseños de informe personalizados](ui-how-create-custom-report-layout.md)   
 [Configurar notificaciones de flujo de trabajo](across-setting-up-workflow-notifications.md)   
 [Configuración de flujos de trabajo](across-set-up-workflows.md)   
 [Uso de flujos de trabajo](across-use-workflows.md)
