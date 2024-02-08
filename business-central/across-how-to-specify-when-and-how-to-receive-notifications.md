---
title: Especificar cómo y cuándo recibir notificaciones de flujos de trabajo
description: 'Cuando configura usuarios en flujos de trabajo de aprobación, puede especificar cómo y cuándo recibe notificaciones cada usuario de aprobación.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.search.form: '663, 1500, 1512, 1513,'
ms.date: 09/09/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Especificar cómo y cuándo recibir notificaciones de flujos de trabajo

Cuando configura usuarios de aprobación en flujos de trabajo, en los que desea que alguien apruebe los cambios, como cuando se crean nuevos registros o cuando alguien solicita una aprobación, debe especificar cómo y cuándo notificar al usuario de aprobación. Por ejemplo, puede especificar que un usuario de aprobación recibirá inmediatamente un correo electrónico cuando alguien cree un nuevo cliente. También puede programar las notificaciones para que se mantengan y se entreguen juntas, por ejemplo, de forma semanal o mensual.

Las personas pueden cambiar también su configuración de notificaciones eligiendo **Cambiar configuración de notificaciones** en cualquier notificación.  

> [!NOTE]
> Las notificaciones se entregan de acuerdo con la configuración de notificaciones del receptor, no del remitente. Es una distinción importante porque significa que, cuando alguien solicita una aprobación como parte de un flujo de trabajo, su solicitud no se envía necesariamente de inmediato. En su lugar, se entregará de acuerdo con la programación de notificaciones especificada en la configuración de notificaciones del aprobador.

Para poder configurar preferencias de notificación de un usuario de aprobación debe configurar el usuario como usuario de aprobación. Obtenga más información en [Configurar usuarios de aprobación](across-how-to-set-up-approval-users.md).  

> [!NOTE]
> Si desea utilizar el correo electrónico como método de notificación, debe configurarlo para el remitente y para el destinatario en [!INCLUDE [prod_short](includes/prod_short.md)]. Obtenga más información en [Configurar correo electrónico](admin-how-setup-email.md).

## Pasos de flujos de trabajo

Muchos pasos del flujo de trabajo de aprobación están relacionados con la notificación a los usuarios de un evento que se ha producido y en el que deben realizar una acción. Por ejemplo, en un paso del flujo de trabajo, el evento puede ser que el usuario 1 solicita la aprobación de un registro nuevo. La respuesta relacionada es que se envíe una notificación al usuario 2, el aprobador. En el siguiente paso del flujo de trabajo, el evento puede ser que el usuario 2 aprueba el registro. La respuesta relacionada es que se envíe una notificación al usuario 3 para iniciar un proceso con el registro aprobado. En el caso de los pasos del flujo de trabajo relacionados con las aprobaciones, cada notificación está vinculada a una entrada de aprobación. Obtenga más información en [Flujo de trabajo](across-workflow.md).  

## Especificar cómo y cuándo los usuarios de aprobaciones reciben notificaciones  

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Config. usuario aprobación** y luego elija el vínculo relacionado.  
2. Seleccione la línea del usuario para el que desea configurar las preferencias de notificación y, a continuación, elija la acción **Configuración de notificación**.  
3. En la página **Configuración de notificaciones de flujo de trabajo**, rellene los campos tal como se describe en la tabla siguiente.  

   > [!NOTE]
   > Si abre la página **Configuración de notificaciones de flujo de trabajo** desde la página **Configuración usuarios de aprobación**, la configuración de notificaciones está vinculada al usuario de aprobación. El usuario de aprobación siempre recibirá notificaciones de flujo de trabajo de acuerdo con esa configuración de notificaciones. Si utiliza la función *Dígame* para abrir la página **Configuración de notificaciones de flujo de trabajo**, la configuración de notificaciones se aplica a todos los usuarios.

   |Campo|Descripción|
   |-----|-----------|
   |**Tipo de notificación**|Especifique el tipo de evento del que trata la notificación.<br /><br /> Seleccione una de las siguientes opciones:<br /><br /> -   **Nuevo registro** especifica que la notificación trata de un registro nuevo, como un documento, en el que el usuario debe realizar alguna acción.<br />-   **Aprobación** especifica que la notificación trata de una solicitud de aprobación o más.<br />-   **Vencidos** especifica que la notificación recuerda a los usuarios que se han retrasado para actuar en un evento.|
   |**Método de notificación**|Especifique si la notificación es un correo electrónico o una nota interna.|

   Puede definir el diseño de las notificaciones por correo electrónico personalizando el informe 1320, Correo electrónico de notificación. Obtenga más información en [Crear y modificar diseños de informe personalizados](ui-how-create-custom-report-layout.md).

   Ya ha especificado cómo recibe el usuario las notificaciones. Proceda a especificar cuándo recibe el usuario las notificaciones.  
4. Elija la acción **Programación de notificación**.  
5. En la página **Programación de notificación**, rellene los campos tal como se describe en la tabla siguiente.  

   |Campo|Descripción|
   |-----|-----------|
   |**Periodicidad**|Especifique el patrón periódico con el que se envían las notificaciones al usuario.|
   |**Hora**|Especifique a qué hora del día se envían notificaciones al usuario cuando el valor del campo **Periodicidad** tiene un valor diferente de **Inmediatamente**.|
   |**Frecuencia diaria**|Especifique en qué tipo de días recibe el usuario las notificaciones cuando el valor del campo **Periodicidad** es **Diario**.<br /><br /> Seleccione **Día laborable** para recibir notificaciones cada día de la semana laboral. Seleccione **Diario** para recibir notificaciones cada día de la semana, incluso los fines de semana.|
   |**Lunes** a **Domingo**|Especifique en qué tipo de días recibe el usuario las notificaciones cuando el valor del campo **Periodicidad** es **Semanal**.|
   |**Fecha de mes**|Especifique si el usuario recibe notificaciones al principio del mes, al final o en una fecha específica.|
   |**Fecha de notificación mensual**|Especifique la fecha del mes en las que el usuario recibe las notificaciones cuando el valor del campo **Fecha de mes** es **Personalizada**.|

## Cambiar cómo y cuándo recibe notificaciones

1. En una de las notificaciones que ha recibido, en correo electrónico o nota, elija **Cambiar configuración de notificación**.  
2. En la página **Configuración de notificaciones de flujo de trabajo**, cambie sus preferencias de notificación tal como se describe en los pasos 3-5 anteriores.
   1. Confirme que se haya elegido la notificación correcta en el campo **Tipo de notificación**.
   2. Elija si desea recibir una notificación por correo electrónico o por nota en el campo **Método de notificación**.
   3. Seleccione **Programación de notificación** para cambiar la frecuencia y la periodicidad con las que se envían las notificaciones.

## Consulte también .

[Configurar usuarios de aprobación](across-how-to-set-up-approval-users.md)  
[Crear y modificar diseños de informe personalizados](ui-how-create-custom-report-layout.md)  
[Configurar notificaciones de flujo de trabajo de aprobación](across-setting-up-workflow-notifications.md)  
[Configurar flujos de trabajo de aprobación](across-set-up-workflows.md)  
[Usar flujos de trabajo de aprobación](across-use-workflows.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
