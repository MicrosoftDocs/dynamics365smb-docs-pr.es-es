---
title: Configuración y uso de un flujo de trabajo de aprobación de compra
description: Puede automatizar el proceso de aprobar nuevos registros o registros modificados, como documentos, líneas de diario y fichas cliente, creando flujos de trabajo con pasos para las aprobaciones en cuestión. Antes de crear flujos de trabajo de aprobación, debe configurar un aprobador y un aprobador sustituto para cada usuario de aprobación. También puede establecer límites de cantidad de aprobadores para definir qué registros de venta y de compra pueden aprobar. Las solicitudes de aprobación y otras notificaciones se pueden enviar como mensajes de correo electrónico o como notas internas. Para cada configuración de usuario de aprobación, también puede configurar cuándo reciben notificaciones.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 05/26/2021
ms.author: edupont
ms.openlocfilehash: 964e1dae3dc754198777c703a15c1ef0b6fe82a7
ms.sourcegitcommit: 6bce51954f17b80491e180f25d67ff18b1618a88
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/27/2021
ms.locfileid: "6110984"
---
# <a name="walkthrough-setting-up-and-using-a-purchase-approval-workflow"></a>Tutorial: Configuración y uso de un flujo de trabajo de aprobación de compra

Puede automatizar el proceso de aprobar nuevos registros o registros modificados, como documentos, líneas de diario y fichas cliente, creando flujos de trabajo con pasos para las aprobaciones en cuestión. Antes de crear flujos de trabajo de aprobación, debe configurar un aprobador y un aprobador sustituto para cada usuario de aprobación. También puede establecer límites de cantidad de aprobadores para definir qué registros de venta y de compra pueden aprobar. Las solicitudes de aprobación y otras notificaciones se pueden enviar como mensajes de correo electrónico o como notas internas. Para cada configuración de usuario de aprobación, también puede configurar cuándo reciben notificaciones.

> [!NOTE]
> Además de la funcionalidad de flujo de trabajo en [!INCLUDE[prod_short](includes/prod_short.md)], puede usar Power Automate para definir flujos de trabajo para eventos en [!INCLUDE[prod_short](includes/prod_short.md)]. Tenga en cuenta que, aunque son dos sistemas de flujo de trabajo independientes, cualquier plantilla de flujo de trabajo que cree con Power Automate se agrega a la lista de modelos de flujo de trabajo en la sección [!INCLUDE[prod_short](includes/prod_short.md)]. Para obtener más información, vea [Usar Business Central en un flujo de trabajo automatizado](across-how-use-financials-data-source-flow.md).  

 Puede configurar y utilizar flujos de trabajo que vinculen tareas de procesos empresariales realizadas por distintos usuarios. Las tareas de sistema, como registros automáticos, se pueden incluir como pasos en los flujos de trabajo, antes o después de las tareas de usuario. Solicitar y conceder aprobaciones para crear registros nuevos son pasos habituales de un flujo de trabajo. Para obtener más información, consulte [Flujo de trabajo](across-workflow.md).  

## <a name="about-this-walkthrough"></a>Acerca de este tutorial

En este tutorial se ilustran las siguientes tareas:  

- Configurar usuarios de aprobación  
- Configurar notificaciones para usuarios de aprobación  
- Modificar y activar un flujo de trabajo de aprobación  
- Solicitar aprobación de un pedido de compra, como Alicia  
- Recibir una notificación a continuación aprobar la solicitud, como Pedro  

## <a name="story"></a>Historia

Pedro es superusuario en CRONUS. Crea dos usuarios de aprobación. Uno es Alicia, que representa un agente de compras. El otro es él mismo, que representa al aprobador de Alicia. Pedro se concede derechos de aprobación de compra ilimitados y especifica que recibirá las notificaciones por la nota interna en cuanto se produzca un evento relevante. Por último, Pedro crea el flujo de trabajo de aprobación necesario como copia de la plantilla existente de flujo de trabajo de aprobación de pedido de compra, deja todas las condiciones de evento y las opciones de respuesta existentes sin cambiar y, a continuación, activa el flujo de trabajo.  

Para probar el flujo de aprobación, Pedro primero inicia sesión en [!INCLUDE[prod_short](includes/prod_short.md)] como Alicia y, a continuación, solicita aprobación de un pedido de compra. Después inicia sesión como él mismo, ve la nota en su área de trabajo, sigue el vínculo a la solicitud de aprobación del pedido de compra y aprueba la solicitud.  

## <a name="users"></a>Usuarios

Para poder configurar los usuarios de aprobación y su método de notificación, debe asegurarse de que existen dos usuarios en [!INCLUDE[prod_short](includes/prod_short.md)]: un usuario representará a Alicia. El otro usuario, usted, representará a Sean. Para obtener más información, vea [Crear usuarios de acuerdo con las licencias](ui-how-users-permissions.md).

### <a name="setting-up-approval-users"></a>Configuración de usuarios de aprobación

Cuando inicie sesión como usted mismo, configure a Alicia como un usuario de aprobación cuyo aprobador sea usted mismo. Configure sus derechos de aprobación y especifique cómo y cuándo se le notificarán las solicitudes de aprobación.  

#### <a name="to-set-up-yourself-and-alicia-as-approval-users"></a>Para configurarse a usted y a Alicia como usuarios de aprobación

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Config. usuario aprobación** y luego elija el enlace relacionado.  
2. En la página **Config. usuario aprobación**, seleccione la acción **Nuevo**.  

    > [!NOTE]  
    >  Debe configurar un aprobador para poder configurar usuarios que requieren la aprobación del aprobador. Así, antes de configurar a Alicia, debe configurarse a sí mismo.  

3. Configure a los dos usuarios de aprobación rellenando los campos tal como se describe en la tabla siguiente.  

    |Id. de usuario|Id. aprobador|Aprobación compra ilimitada|  
    |-------------|-----------------|---------------------------------|  
    |USTED||Seleccionada|  
    |ALICIA|USTED||  

### <a name="setting-up-notifications"></a>Configuración de notificaciones

En este tutorial, el usuario recibe una notificación mediante una nota interna sobre las solicitudes para aprobar. La notificación de aprobación también puede realizarse por correo electrónico y puede agregar un paso de respuesta de flujo de trabajo que notifique al remitente cuando se aprueba o rechaza una solicitud. Para obtener más información, consulte [Especificar cómo y cuándo recibir notificaciones](across-how-to-specify-when-and-how-to-receive-notifications.md).

#### <a name="to-set-up-how-and-when-you-are-notified"></a>Para configurar cómo y cuándo recibirá notificaciones

1. En la página **Config. usuario aprobación**, seleccione la línea para usted y después seleccione la acción **Configuración de notificación**.  
2. En la página **Configuración de notificación**, en el campo **Tipo de notificación**, elija **Aprobación**.  
3. En el campo **Método de notificación**, elija **Nota**.  
4. En la página **Configuración de notificación**, seleccione la acción **Programación de notificación**.  
5. En la página **Programación de notificación**, del campo **Periodicidad**, seleccione **Inmediatamente**.  

## <a name="creating-the-approval-workflow"></a>Creación del flujo de aprobación

Cree el flujo de aprobación de pedido de compra copiando los pasos de la plantilla de flujo de trabajo de **aprobación de pedido de compra**. Deje los pasos de flujo de trabajo existentes sin cambiar y, a continuación, active el flujo de trabajo.  

> [!TIP]
> Opcionalmente, agregue un paso de respuesta de flujo de trabajo para notificar al remitente cuando su solicitud sea aprobada o rechazada. Para obtener más información, consulte [Especificar cómo y cuándo recibir notificaciones](across-how-to-specify-when-and-how-to-receive-notifications.md).

### <a name="to-create-and-enable-a-purchase-order-approval-workflow"></a>Para crear y activar un flujo de trabajo de aprobación de pedido de compra

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Flujos de trabajo** y luego elija el enlace relacionado.  
2. En la página **Flujos de trabajo**, seleccione **Acciones**, luego seleccione **Nuevo** y luego elija la acción **Nuevo flujo de trabajo de plantilla**.  
3. En la página **Plantillas de flujo de trabajo**, seleccione la plantilla de flujo de trabajo denominada **Flujo de trabajo de aprobación de pedido de compra**.  

    La página **Flujo de trabajo** se abre para un nuevo flujo de trabajo que contiene toda la información de la plantilla seleccionada. El valor del campo **Código** se amplía con *-01* para indicar que este es el primer flujo de trabajo creado a partir de la plantilla de flujo de trabajo denominada **Flujo de trabajo de aprobación de pedido de compra**.  
4. En el encabezado de la página **Flujo de trabajo**, seleccione la casilla **Habilitado**.  

## <a name="using-the-approval-workflow"></a>Uso del flujo de trabajo de aprobación

Utilice el nuevo flujo de trabajo de aprobación de pedido de compra iniciando sesión primero en [!INCLUDE[prod_short](includes/prod_short.md)] como Alicia para solicitar la aprobación de un pedido de compra. Después, inicie sesión como usted mismo, consulte la nota en el área de trabajo, siga el vínculo a la solicitud de aprobación y, a continuación, apruebe la solicitud.  

### <a name="to-request-approval-of-a-purchase-order-as-alicia"></a>Para solicitar aprobación de un pedido de compra como Alicia

1. Inicie sesión como Alicia.
2. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Pedidos de compra** y luego elija el enlace relacionado.  
3. Seleccione la línea para abrir el pedido de compra 106001.  
4. En la página **Pedido de compra**, elija **Acciones**, luego, **Solicitar aprobación** y, después, la acción **Enviar solicitud aprobación**.  

Observe que el valor del campo **Estado** ha cambiado **Pendiente de aprobación**.  

### <a name="to-approve-the-purchase-order-as-sean"></a>Para aprobar el pedido de compra como Pedro

1. Inicie sesión como Sean.
2. En el área de trabajo, en el área **Autoservicio**, elija la ventana **Solicitudes para aprobar**.
3. En la página **Solicitudes para aprobar**, seleccione la línea sobre el pedido de compra de Alicia y luego elija la acción **Aprobar**.  

El valor del campo **Estado** del pedido de compra de Alicia cambia **Lanzado**.  

Ya ha configurado y probado un flujo de trabajo de aprobación sencillo según los dos primeros pasos del flujo de trabajo de aprobación de pedido de compra. Puede ampliar fácilmente este flujo de trabajo para registrar automáticamente el pedido de compra de Alicia cuando Pedro lo apruebe. Para hacerlo, debe activar el flujo de trabajo de factura de compra, en el que la respuesta a una factura de compra lanzada es registrarla. Primero debe cambiar la condición del evento en el primer paso del flujo de trabajo (compra) **Factura** a **Pedido**.  

La versión genérica de [!INCLUDE[prod_short](includes/prod_short.md)] incluye varias plantillas de flujo de trabajo para ejemplos compatibles con el código de aplicación. La mayor parte de ellos son de los flujos de trabajo de aprobación.  

Las variaciones del flujo de trabajo se definen rellenando los campos de las líneas de flujo de trabajo en listas fijas de valores de evento y respuesta que representan ejemplos de flujo de trabajo que admite el código de aplicación. Para obtener más información, consulte [Crear flujos de trabajo](across-how-to-create-workflows.md).  

Si una situación de negocio requiere un evento de flujo de trabajo o respuesta no compatibles, un asociado de Microsoft tiene que implementarlos a través de código o puede configurar un flujo de trabajo mediante Power Automate. Para más información, ver [Utilizando [!INCLUDE[prod_short](includes/prod_short.md)] en un flujo de trabajo automatizado](across-how-use-financials-data-source-flow.md) o [Eventos en AL](/dynamics365/business-central/dev-itpro/developer/devenv-events-in-al) en la ayuda del desarrollador, respectivamente.

## <a name="see-also"></a>Consulte también

[Configurar usuarios de aprobación](across-how-to-set-up-approval-users.md)  
[Configurar notificaciones de flujo de trabajo](across-setting-up-workflow-notifications.md)  
[Crear flujos de trabajo](across-how-to-create-workflows.md)  
[Usar flujos de trabajo de aprobación del producto](across-how-use-approval-workflows.md)  
[Flujo de trabajo](across-workflow.md)  
[Usar Business Central en un flujo de trabajo automatizado](across-how-use-financials-data-source-flow.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]