---
title: Configurar usuarios de flujo de trabajo | Documentos de Microsoft
description: "Para poder crear flujos de trabajo, debe configurar los usuarios que participan en flujos de trabajo. Esto es necesario para especificar, por ejemplo, quién debe recibir una notificación para actuar sobre un paso del flujo de trabajo."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reject, delegate, request
ms.date: 08/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 929cce642a6adccc493c1ce9947ac60662b261d5
ms.contentlocale: es-es
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-workflow-users"></a>Procedimiento: Configurar usuarios de flujo de trabajo
Para poder crear flujos de trabajo, debe configurar los usuarios que participan en flujos de trabajo. Esto es necesario para especificar, por ejemplo, quién debe recibir una notificación para actuar sobre un paso del flujo de trabajo.  

En la ventana **Grupo de usuarios de flujo de trabajo**, se configuran usuarios en grupos de usuarios de flujo de trabajo y se especifica el número de usuarios en una secuencia del proceso, como una cadena de aprobadores.  

Los usuarios del flujo de trabajo que funcionan como usuarios de aprobación, tanto solicitantes de aprobación como aprobadores, también deben configurarse como usuarios de flujo de trabajo en la ventana **Config. usuario aprobación**. Para obtener más información, vea [Procedimiento: Configurar usuarios de aprobación](across-how-to-set-up-approval-users.md).  

> [!NOTE]  
>  Para definir que una solicitud de aprobación no está aprobada hasta que varios aprobadores en un cadena de aprobación la hayan aprobado, configure aprobadores en jerarquía. Para el tipo de aprobador **Aprobador**, configura los aprobadores en la ventana **Config. usuario aprobación**. Para el tipo de aprobador, **Grupo de usuarios del grupo de trabajo**, configura los aprobadores en la ventana **Grupos de usuarios de flujo de trabajo** y define la jerarquía asignando números incrementales a cada aprobador en el campo **Nº secuencia** . Para obtener más información, consulte [Procedimiento: Configurar usuarios de aprobación](across-how-to-set-up-approval-users.md) y este tema.  
>   
>  Para definir que una solicitud de aprobación no está aprobada hasta que varios aprobadores iguales la hayan aprobado, sin importar la jerarquía, configure un grupo de usuarios de flujo de trabajo lineal. Para el tipo de aprobador, **Grupo de usuarios del grupo de trabajo**, configura los aprobadores en la ventana **Grupos de usuarios de flujo de trabajo** y asigna el mismo número a cada aprobador en el campo **Nº secuencia** . Para obtener más información, consulte este tema.  

### <a name="to-set-up-a-workflow-user"></a>Para configurar usuarios de flujo de trabajo  

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Grupos de usuarios de flujo de trabajo** y, a continuación, seleccione el vínculo relacionado.  
2. Seleccione la acción **Nuevo**. Se abe la ventana **Grupo de usuarios de flujo de trabajo**.  
3. En el campo **Código**, introduzca un máximo de 20 caracteres para identificar el flujo de trabajo.  
4. En el campo **Descripción**, describa el flujo de trabajo.  
5. En la ficha desplegable **Miembros de grupo de usuarios de flujo de trabajo**, rellene los campos en la primera línea tal y como se describe en la tabla siguiente.  

    |Campo|Description|  
    |---------------------------------|---------------------------------------|  
    |**Nombre usuario**|Especifique el usuario que formará parte de los flujos de trabajo.<br /><br /> El usuario debe existir en la ventana de **Configuración usuarios**. Para obtener más información, vea [Administrar usuarios y permisos](ui-how-users-permissions.md).|  
    |**Nº secuencia**|Especifique el orden en el que participa el usuario de flujo de trabajo en flujos de trabajo relacionados con otros usuarios. Este campo se puede usar, por ejemplo, para especificar cuándo aprueba el usuario en relación con otros aprobadores cuando se utiliza la opción **Grupo de usuarios de flujo de trabajo** en el campo **Tipo de aprobador** en la respuesta relacionada del flujo de trabajo. **SUGERENCIA**: Para definir que una solicitud de aprobación no está aprobada hasta que varios aprobadores iguales la hayan aprobado, independientemente de la jerarquía, configure un grupo de usuarios de flujo de trabajo plano asignando el mismo número de secuencia a los aprobadores correspondientes.|  
6. Repita el paso 5 para añadir más usuarios de flujo de trabajo al grupo de usuarios.  
7. Repita los pasos del 2 al 6 para añadir más grupos de usuarios de flujo de trabajo.  

## <a name="see-also"></a>Consulte también  
[Procedimiento: Configurar usuarios de aprobación](across-how-to-set-up-approval-users.md)   
[Configuración de flujos de trabajo](across-set-up-workflows.md)   
[Uso de flujos de trabajo](across-use-workflows.md)   
[Tutorial: Configuración y uso de un flujo de trabajo de aprobación de compra](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)   
[Flujo de trabajo](across-workflow.md)   

