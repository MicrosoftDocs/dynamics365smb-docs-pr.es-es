---
title: Configurar usuarios de aprobación | Documentos de Microsoft
description: Antes de que puedas crear flujos de trabajo que impliquen pasos de aprobación, tienes que configurar los usuarios del flujo de trabajo implicados en los procesos de aprobación. En la página Config. usuario aprobación, también se pueden establecer los límites del importe de tipos específicos de solicitudes y definir aprobadores sustitutos a los que delegar las solicitudes de aprobación cuando el aprobador original está ausente.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: ab35f8f37490852be98d6c3e8a2cf30b2202764a
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/03/2019
ms.locfileid: "2881101"
---
# <a name="set-up-approval-users"></a>Configurar usuarios de aprobación
Antes de que puedas crear flujos de trabajo que impliquen pasos de aprobación, tienes que configurar los usuarios del flujo de trabajo implicados en los procesos de aprobación. En la página **Config. usuario aprobación**, también se pueden establecer los límites del importe de tipos específicos de solicitudes y definir aprobadores sustitutos a los que delegar las solicitudes de aprobación cuando el aprobador original está ausente.  

> [!NOTE]  
>  Los usuarios de la aprobación, tanto los solicitantes de aprobaciones como los aprobadores, primero se tienen que establecer como usuarios del flujo de trabajo en la página **Grupo de usuarios de flujo de trabajo**. Para obtener más información, consulte [Configurar usuarios de flujos trabajo](across-how-to-set-up-workflow-users.md).  

 Una vez configurados los usuarios de aprobación, puede utilizar la configuración para crear las respuestas de flujo de trabajo de los flujos de trabajo de aprobación. Para obtener más información, consulte el paso 9 en [Crear flujos de trabajo](across-how-to-create-workflows.md).  

> [!NOTE]  
>  Para definir que una solicitud de aprobación no está aprobada hasta que varios aprobadores en un cadena de aprobación la hayan aprobado, configure aprobadores en jerarquía. Para el tipo de aprobador **Aprobador**, configura los aprobadores en la página **Config. usuario aprobación**. Para el tipo de aprobador, **Grupo de usuarios del grupo de trabajo**, configura los aprobadores en la página **Grupos de usuarios de flujo de trabajo** y define la jerarquía asignando números incrementales a cada aprobador en el campo **Nº secuencia** . Para obtener más información, consulte este tema y [Configurar usuarios de flujo de trabajo](across-how-to-set-up-workflow-users.md) y este tema.  
>   
>  Para definir que una solicitud de aprobación no está aprobada hasta que varios aprobadores iguales la hayan aprobado, sin importar la jerarquía, configure un grupo de usuarios de flujo de trabajo lineal. Para el tipo de aprobador, **Grupo de usuarios del grupo de trabajo**, configura los aprobadores en la página **Grupos de usuarios de flujo de trabajo** y asigna el mismo número a cada aprobador en el campo **Nº secuencia** . Para obtener más información, consulte [Configurar usuarios de flujos trabajo](across-how-to-set-up-workflow-users.md).  

## <a name="to-set-up-an-approval-user"></a>Para configurar a un usuario de aprobación  
1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Config. usuario aprobación** y luego elija el enlace relacionado.  
2. Cree una nueva línea en la página **Config. usuario aprobación** y después rellena los campos tal y como se describe en la tabla siguiente.  

    |Campo|Description|  
    |---------------------------------|---------------------------------------|  
    |**Id. usuario**|Seleccione el identificador del usuario que participa en el proceso de aprobación.|  
    |**Cód. vendedor/comprador**|Especifica el código del comercial o del comprador que se aplica al usuario en el campo **Cód. vendedor/comprador**.<br /><br /> Normalmente se rellena el campo **Cód. vendedor/comprador** si el comprador responsable del cliente o proveedor es también la persona que tiene que aprobar la solicitud de venta o de compra en cuestión.|  
    |**Id. aprobador**|En el campo **Id. del usuario**, selecciona el Id. del usuario que tiene que aprobar las solicitudes hechas por el usuario.|  
    |**Importe límite aprob. ventas**|Especifica el importe de ventas máximo en la divisa local que el usuario puede aprobar en el campo **Id. de usuario**.|  
    |**Aprobación venta ilimitada**|Especifica que el usuario del campo **Id. de usuario** puede aprobar todas las solicitudes de venta independientemente de su importe.<br /><br /> Si activas esta casilla, no podrás rellenar el campo **Importe límite aprob. ventas**.|  
    |**Importe límite aprob. compras**|Especifica el importe de compra máximo en la divisa local que el usuario puede aprobar en el campo **Id. de usuario**.|  
    |**Aprobación compra ilimitada**|Especifica que el usuario del campo **Id. de usuario** puede aprobar todas las solicitudes de compra independientemente de su importe.<br /><br /> Si activas esta casilla, no podrás rellenar el campo **Importe límite aprob. ventas**.|  
    |**Imp. lím. aprob. solic. compra**|Especifica el importe de compras máximo en la divisa local que el usuario puede aprobar para ofertas de compra en el campo **Id. de usuario**.<br /><br /> Para utilizar este campo tienes que seleccionar la opción **Cadena de aprobadores** del campo **Tipo de límite de aprobador** de la página **Respuesta de flujo de trabajo**.|  
    |**Aprob. solic. compra ilimitada**|Especifica que el usuario del campo **Id. de usuario** puede aprobar todas las ofertas de compra independientemente de su importe.<br /><br /> Si activas esta casilla, no podrás rellenar el campo **Importe límite aprob. solicitud**.|  
    |**Sustituir**|En el campo **Id. del usuario**, selecciona el Id. del usuario que tiene que aprobar las solicitudes hechas por el usuario si el usuario de **Id. aprobador** no está disponible. **Nota**: El sustituto puede ser usuario del campo **Substituir**, el aprobador directo o administrador de la aprobación, en ese orden de prioridad. Para obtener más información, vea [Usar flujos de trabajo de aprobación](across-how-use-approval-workflows.md).|  
    |**Correo electrónico**|Especifica la dirección de correo electrónico del usuario en el campo **Id. de usuario**.|  
    |**Administrador aprobación**|Especifique el usuario que tiene derechos para desbloquear flujos de trabajo de aprobación, por ejemplo, delegando las solicitudes de aprobación en nuevos aprobadores sustitutos y eliminando las solicitudes de aprobación vencidas.|

    > [!Note]
    > Solo una persona puede ser el administrador de aprobación.  

3. Para probar la configuración de usuario de aprobación, elija la opción **Prueba configuración usuario aprobación**.  
4. Repita los pasos 2 y 3 para cada usuario que desee configurar como usuario de aprobación.  

## <a name="see-also"></a>Consulte también  
[Configurar usuarios de flujo de trabajo](across-how-to-set-up-workflow-users.md)   
[Configurar notificaciones de flujo de trabajo](across-setting-up-workflow-notifications.md)   
[Crear flujos de trabajo](across-how-to-create-workflows.md)   
[Configuración de flujos de trabajo](across-set-up-workflows.md)   
[Tutorial: Configuración y uso de un flujo de trabajo de aprobación de compra](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)   
[Flujo de trabajo](across-workflow.md)   
