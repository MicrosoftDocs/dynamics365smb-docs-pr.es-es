---
title: Configurar usuarios de flujo de trabajo
description: Para poder crear flujos de trabajo debe configurar los usuarios que participan en ellos en la página Config. usuario aprobación.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.search.keywords: 'reject, delegate, request'
ms.search.form: '1533,'
ms.date: 04/04/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Configurar una secuencia de usuarios de flujo de trabajo

Para poder crear flujos de trabajo de aprobación, debe configurar los usuarios que pueden enviar solicitudes y sus aprobadores. Por ejemplo, puede especificar quién recibe una notificación para actuar sobre un paso del flujo de trabajo. Los participantes en el flujo de trabajo de aprobación se configuran en la página **Config. usuario aprobación**. Obtenga más información en [Configurar usuarios de aprobación](across-how-to-set-up-approval-users.md).

En la página **Grupos de usuarios de flujo de trabajo** puede especificar dónde se involucra un participante en un flujo de trabajo de aprobación introduciendo un número en el **Nº secuencia** . Por ejemplo, puede especificar que los usuarios participen en un orden secuencial, como una cadena de aprobadores. También puede especificar una lista plana de aprobadores introduciendo el mismo número. En este último caso, solo uno de los aprobadores debe aprobar una solicitud.

[!INCLUDE [workflow-requestor-approver](includes/workflow-requestor-approver.md)]

## Para configurar un grupo de usuarios de flujo de trabajo

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Grupos de usuarios de flujo de trabajo** y luego elija el vínculo relacionado.  
2. Seleccione la acción **Nuevo**. Se abre la página **Grupo de usuarios de flujo de trabajo**.  
3. En el campo **Código**, introduzca un máximo de 20 caracteres para identificar el flujo de trabajo.  
4. En el campo **Descripción**, describa el flujo de trabajo.  
5. En la ficha desplegable **Miembros de grupo de usuarios de flujo de trabajo**, rellene los campos en la primera línea tal y como se describe en la tabla siguiente.  

   |Campo|Descripción|
   |-----|-----------|
   |**Nombre de usuario**|Especifique el usuario que forma parte de un flujo de trabajo.<br /><br /> El usuario debe existir en la página **Configuración usuarios**. Obtenga más información en [Asignar permisos a usuarios y grupos](ui-define-granular-permissions.md).|
   |**Nº secuencia**|Especifique el orden en el que participa el usuario de flujo de trabajo en flujos de trabajo relacionados con otros usuarios. Este campo puede especificar, por ejemplo, cuándo aprueba el usuario en relación con otros aprobadores configurando el **Grupo de usuarios de flujo de trabajo** en el campo **Tipo de aprobador** en la respuesta relacionada del flujo de trabajo.|

   > [!NOTE]
   > Normalmente, los números de secuencia son secuenciales para los usuarios de un grupo de usuarios de flujo de trabajo. Sin embargo, varios usuarios pueden tener el mismo número de secuencia. Cuando ese es el caso, solo uno de los usuarios debe aprobar una solicitud antes de que el flujo de trabajo pase al siguiente paso. Por ejemplo, si el usuario A y el usuario B son ambos el número dos en la secuencia, el flujo de trabajo pasa al paso tres cuando el usuario A o el usuario B aprueban la solicitud.
6. Repita el paso 5 para añadir más usuarios de flujo de trabajo al grupo de usuarios del flujo de trabajo.  

## Consulte también .

[Configurar usuarios de aprobación](across-how-to-set-up-approval-users.md)  
[Configurar flujos de trabajo de aprobación](across-set-up-workflows.md)  
[Usar flujos de trabajo de aprobación](across-use-workflows.md)  
[Tutorial: Configuración y uso de un flujo de trabajo de aprobación de compra](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Flujo de trabajo](across-workflow.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
