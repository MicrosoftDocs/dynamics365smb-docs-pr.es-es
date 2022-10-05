---
title: Configurar usuarios de flujo de trabajo
description: Para poder crear flujos de trabajo debe configurar los usuarios que participan en ellos en la página Grupo de usuarios de flujo de trabajo.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reject, delegate, request
ms.search.form: 1533
ms.date: 09/09/2022
ms.author: edupont
ms.openlocfilehash: 4dbe4217720ddd0bfe976560331329537577cfeb
ms.sourcegitcommit: 9049f75c86dea374e5bfe297304caa32f579f6e4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/23/2022
ms.locfileid: "9585951"
---
# <a name="set-up-workflow-users"></a>Configurar usuarios de flujo de trabajo

Para poder crear flujos de trabajo de aprobación, debe configurar los usuarios que participan en flujos de trabajo. Esto es necesario para especificar, por ejemplo, quién debe recibir una notificación para actuar sobre un paso del flujo de trabajo.  

En la página **Grupos de usuarios de flujo de trabajo**, se pueden configurar usuarios en grupos de usuarios de flujo de trabajo y se especifica el número de usuarios en una secuencia del proceso, como una cadena de aprobadores. 

Los usuarios del flujo de trabajo que funcionan como usuarios de aprobación, tanto solicitantes de aprobación como aprobadores, también deben configurarse como usuarios de flujo de trabajo en la página **Config. usuario aprobación**. Obtenga más información en [Configurar usuarios de aprobación](across-how-to-set-up-approval-users.md).  

> [!NOTE]  
> Para definir una solicitud de aprobación como no aprobada hasta que varios usuarios la hayan aprobado, establezca los aprobadores en una jerarquía. Para el tipo de aprobador **Aprobador**, configure los aprobadores en la página **Config. usuario aprobación**. Para el tipo de aprobador **Grupo de usuarios del grupo de trabajo**, configure los aprobadores en la página **Grupos de usuarios de flujo de trabajo** y define la jerarquía asignando números incrementales a cada aprobador en el campo **Nº secuencia** . Obtenga más información a continuación y en [Configurar usuarios de aprobación](across-how-to-set-up-approval-users.md). 

## <a name="to-set-up-a-workflow-user"></a>Para configurar usuarios de flujo de trabajo

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Grupos de usuarios de flujo de trabajo** y luego elija el vínculo relacionado.  
2. Seleccione la acción **Nuevo**. Se abre la página **Grupo de usuarios de flujo de trabajo**.  
3. En el campo **Código**, introduzca un máximo de 20 caracteres para identificar el flujo de trabajo.  
4. En el campo **Descripción**, describa el flujo de trabajo.  
5. En la ficha desplegable **Miembros de grupo de usuarios de flujo de trabajo**, rellene los campos en la primera línea tal y como se describe en la tabla siguiente.  

   |Campo|Descripción|
   |-----|-----------|
   |**Nombre usuario**|Especifique el usuario que formará parte de los flujos de trabajo.<br /><br /> El usuario debe existir en la página **Configuración usuarios**. Obtenga más información en [Asignar permisos a usuarios y grupos](ui-define-granular-permissions.md).|
   |**Nº secuencia**|Especifique el orden en el que participa el usuario de flujo de trabajo en flujos de trabajo relacionados con otros usuarios. Este campo puede especificar, por ejemplo, cuándo aprueba el usuario en relación con otros aprobadores configurando el **Grupo de usuarios de flujo de trabajo** en el campo **Tipo de aprobador** en la respuesta relacionada del flujo de trabajo.| 

   > [!TIP]
   > Para definir que una solicitud de aprobación requiera que varios usuarios iguales la aprueben, independientemente de la jerarquía, configure un grupo de usuarios de flujo de trabajo plano asignando el mismo número de secuencia a todos los aprobadores correspondientes.

6. Repita el paso 5 para añadir más usuarios de flujo de trabajo al grupo de usuarios del flujo de trabajo.  
7. Repita los pasos del 2 al 6 para añadir más grupos de usuarios de flujo de trabajo.  

## <a name="see-related-microsoft-training"></a>Consultar la [formación de Microsoft](/training/modules/create-workflows/) relacionada

## <a name="see-also"></a>Consulte también .

[Configurar usuarios de aprobación](across-how-to-set-up-approval-users.md)  
[Configurar flujos de trabajo de aprobación](across-set-up-workflows.md)  
[Usar flujos de trabajo de aprobación](across-use-workflows.md)  
[Tutorial: Configuración y uso de un flujo de trabajo de aprobación de compra](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Flujo de trabajo](across-workflow.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
