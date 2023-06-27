---
title: Configurar usuarios de aprobación
description: 'Antes de poder crear flujos de trabajo que impliquen pasos de aprobación, debe configurar los usuarios del flujo de trabajo implicados en los procesos de aprobación.'
author: brentholtorf
ms.topic: how-to
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '663,'
ms.date: 05/31/2023
ms.author: bholtorf
---
# <a name="set-up-approval-users"></a><a name="set-up-approval-users"></a>Configurar usuarios de aprobación

Antes de poder crear flujos de trabajo que impliquen pasos de aprobación, debe configurar los usuarios que intervienen en los procesos de aprobación en la página **Config. usuario aprobación**. También puede establecer límites de importe para distintos tipos de solicitudes, definir aprobadores sustitutos y configurar notificaciones.  

Una vez configurados los usuarios de aprobación, puede crear las respuestas de flujo de trabajo de los flujos de trabajo de aprobación. Obtenga más información en [Crear flujos de trabajo de aprobación](across-how-to-create-workflows.md).  

> [!TIP]
> Puede exigir que varios aprobadores reaccionen ante una solicitud de aprobación creando un grupo de aprobadores en la página **Grupo de usuarios de flujo de trabajo** . Obtenga más información en [Configurar grupos de usuarios de flujo de trabajo](across-how-to-set-up-workflow-users.md).  

## <a name="to-set-up-an-approval-user"></a><a name="to-set-up-an-approval-user"></a>Para configurar a un usuario de aprobación

[!INCLUDE [workflow-requestor-approver](includes/workflow-requestor-approver.md)]

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Config. usuario aprobación** y luego elija el vínculo relacionado.  
2. Cree una nueva línea en la página **Config. usuario aprobación** y después rellena los campos tal y como se describe en la tabla siguiente.  

   |Campo|Descripción|
   |-----|-----------|
   |**Id. usuario**|Seleccione el identificador de la persona que participa en el proceso de aprobación.|
   |**Cód. vendedor/comprador**|Especifica el código del comercial o del comprador que se aplica al usuario.<br /><br /> Normalmente se rellena el campo **Cód. vendedor/comprador** si el comprador responsable del cliente o proveedor es también la persona que tiene que aprobar una solicitud de venta o de compra.|
   |**Id. aprobador**|Seleccione el Id. de usuario de la persona que debe aprobar las solicitudes realizadas por la persona que ha especificado en el campo **Id. de usuario**.|
   |**Importe límite aprob. ventas**|Especifique el importe máximo de ventas en divisa local (DL) que la persona seleccionada en el campo **ID. de usuario** puede aprobar.|
   |**Aprobación venta ilimitada**|Especifica que el la persona identificada en el campo **Id. de usuario** puede aprobar todas las solicitudes de venta independientemente del importe.<br /><br /> Si activa esta casilla, no podrá rellenar el campo **Importe límite aprob. ventas**.|
   |**Importe límite aprob. compras**|Especifique el importe máximo de compra en DL que la persona identificada en el campo **Id. de usuario** puede aprobar.|
   |**Aprobación compra ilimitada**|Especifica que el la persona identificada en el campo **Id. de usuario** puede aprobar todas las solicitudes de compra independientemente del importe.<br /><br /> Si activa esta casilla, no podrá rellenar el campo **Importe límite aprob. compras**.|
   |**Imp. lím. aprob. solic. compra**|Especifica el importe de compras máximo en la divisa local que la persona identificada puede aprobar para ofertas de compra en el campo **Id. de usuario**.<br /><br /> Para utilizar este campo tienes que seleccionar la opción **Cadena de aprobadores** del campo **Tipo de límite de aprobador** de la página **Respuesta de flujo de trabajo**.|
   |**Aprob. solic. compra ilimitada**|Especifica que el la persona identificada en el campo **Id. de usuario** puede aprobar todos los pedidos independientemente del importe.<br /><br /> Si activa esta casilla, no puede rellenar el campo **Importe límite aprob. solicitud**.|
   |**Sustituir**|En el campo **Id. del usuario**, selecciona la persona que aprobará las solicitudes hechas por la persona identificada si el usuario de **Id. aprobador** no está disponible. <br /><br />**Nota**: El sustituto puede ser usuario del campo **Substituir**, el aprobador directo o administrador de la aprobación, en ese orden de prioridad. Obtenga más información en [Usar flujos de trabajo de aprobación](across-how-use-approval-workflows.md).|
   |**Correo electrónico**|Especifica la dirección de correo electrónico de la persona en el campo **Id. de usuario**.|
   |**Administrador aprobación**|Especifique el usuario que tiene permiso para desbloquear el flujo de trabajo de aprobación, por ejemplo, delegando las solicitudes de aprobación en nuevos aprobadores sustitutos o eliminando las solicitudes de aprobación vencidas.<br /><br />**Nota** Solo una persona puede ser el administrador de aprobación.|

3. Para probar la configuración de usuario de aprobación, elija la opción **Prueba configuración usuario aprobación**.  
4. Repita los pasos 2 y 3 para cada persona que desee configurar como usuario de aprobación.  

El siguiente paso es especificar cómo desea que [!INCLUDE [prod_short](includes/prod_short.md)] notifique a las personas que una solicitud está pendiente de su atención. Obtenga más información en [Configurar notificaciones de flujo de trabajo de aprobación](across-setting-up-workflow-notifications.md).

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Consultar la [formación de Microsoft](/training/modules/create-workflows/) relacionada

## <a name="see-also"></a><a name="see-also"></a>Consulte también .

[Configurar usuarios de flujo de trabajo](across-how-to-set-up-workflow-users.md)  
[Configurar notificaciones de flujo de trabajo](across-setting-up-workflow-notifications.md)  
[Crear flujos de trabajo de aprobación](across-how-to-create-workflows.md)  
[Configurar flujos de trabajo de aprobación](across-set-up-workflows.md)  
[Tutorial: Configuración y uso de un flujo de trabajo de aprobación de compra](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Flujo de trabajo](across-workflow.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
