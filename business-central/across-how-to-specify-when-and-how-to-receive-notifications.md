---
title: Especificar cómo y cuándo recibir notificaciones de flujos de trabajo
description: Cuando configura usuarios en flujos de trabajo de aprobación, puede especificar cómo y cuándo recibe notificaciones cada usuario de aprobación.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/11/2021
ms.author: edupont
ms.openlocfilehash: 261e2908f7f7ed3a47a337b2c3f49d7c633f1cce
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2022
ms.locfileid: "8522357"
---
# <a name="specify-when-and-how-to-receive-workflow-notifications"></a>Especificar cómo y cuándo recibir notificaciones de flujos de trabajo
Cuando configura usuarios de aprobación en flujos de trabajo, en los que desea que alguien apruebe los cambios, como cuando se crean nuevos registros o cuando alguien solicita una aprobación, debe especificar cómo y cuándo se notificará al usuario de aprobación. Por ejemplo, puede especificar que un usuario de aprobación recibirá inmediatamente un correo electrónico cuando alguien cree un nuevo cliente. Como alternativa, puede programar las notificaciones para que se entreguen, por ejemplo, semanal o mensualmente.

Las personas pueden cambiar también su configuración de notificaciones eligiendo el botón **Cambiar configuración de notificaciones** en cualquier notificación.  

> [!NOTE]
> Las notificaciones se entregan de acuerdo con la configuración de notificaciones del receptor, no del remitente. Es una distinción importante porque significa que, cuando alguien solicita una aprobación como parte de un flujo de trabajo, su solicitud no se envía necesariamente de inmediato. En su lugar, se entregará de acuerdo con la programación de notificaciones especificada en la configuración de notificaciones del aprobador. 

Para poder configurar preferencias de notificación de un usuario de aprobación debe configurar el usuario como usuario de aprobación. Para obtener más información, [Configurar usuarios de aprobación](across-how-to-set-up-approval-users.md).  

Puede definir el diseño de las notificaciones por correo electrónico personalizando el informe 1320, Correo electrónico de notificación. Para obtener más información, vea [Crear y modificar diseños de informe personalizados](ui-how-create-custom-report-layout.md).  

> [!NOTE]
> Si desea utilizar el correo electrónico como método de notificación, debe configurarlo para el remitente y para el destinatario en[!INCLUDE [prod_short](includes/prod_short.md)]. Para obtener más información, consulte [Configurar correo electrónico](admin-how-setup-email.md).

## <a name="steps-in-workflows"></a>Pasos de flujos de trabajo 
Muchos pasos del flujo de trabajo de aprobación están relacionados con la notificación a los usuarios de un evento que se ha producido y en el que deben realizar una acción. Por ejemplo, en un paso del flujo de trabajo, el evento puede ser que el usuario 1 solicita la aprobación de un registro nuevo. La respuesta relacionada es que se envíe una notificación al usuario 2, el aprobador. En el siguiente paso del flujo de trabajo, el evento puede ser que el usuario 2 aprueba el registro. La respuesta relacionada es que se envíe una notificación al usuario 3 para iniciar un proceso con el registro aprobado. En el caso de los pasos del flujo de trabajo relacionados con la aprobación, cada notificación está vinculada a un movimiento de aprobación. Para obtener más información, consulte [Flujo de trabajo](across-workflow.md).  

## <a name="specify-when-and-how-users-receive-notifications"></a>Especificar cómo y cuándo los usuarios reciben notificaciones  

1.  Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Config. usuario aprobación** y luego elija el enlace relacionado.  
2.  Seleccione la línea del usuario para el que desea configurar las preferencias de notificación y, a continuación, elija la acción **Configuración de notificación**.  
3.  En la página **Configuración de notificación**, rellene los campos tal como se describe en la tabla siguiente.  

    > [!NOTE]
    > Si abre la página **Configuración de notificaciones** desde la página **Configuración usuarios de aprobación**, la configuración de notificaciones está vinculada al usuario de aprobación. El usuario de aprobación siempre recibirá notificaciones de flujo de trabajo de acuerdo con esa configuración de notificaciones. Si usa Dígame para abrir la página **Configuración de notificaciones**, la configuración de notificaciones se aplicará a todos los usuarios.  

    |Campo|Descripción|  
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
 [Usar flujos de trabajo](across-use-workflows.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]