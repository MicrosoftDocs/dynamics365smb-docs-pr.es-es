---
title: "Administrar la personalización como administrador en Business Central | Documentos de Microsoft"
description: Aprenda a personalizar la interfaz de usuario para que se adapte a su forma de trabajar.
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: caf7cf5afe370af0c4294c794c0ff9bc8ff4c31c
ms.openlocfilehash: 15d7e4aac7989f95f7becc8aa8ed96381a7dc2de
ms.contentlocale: es-es
ms.lasthandoff: 11/22/2018

---
# <a name="managing-personalization-as-an-administrator"></a>Administrar la personalización como administrador
<!--NAV in the Web client--> Los usuarios pueden personalizar el área de trabajo para que se adapte a sus preferencias. Como administrador, puede controlar y administrar la personalización desactivando la capacidad de los usuarios para personalizar las páginas y borrar las personalizaciones de página que los usuarios hayan realizado.

## <a name="disable-personalization-for-a-profile"></a>Deshabilitar la personalización de un perfil
Puede evitar que todos los usuarios que pertenecen a un perfil específico puedan personalizar sus páginas.
1.  Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Perfiles** y luego elija el enlace relacionado.
2.  Seleccione el perfil de la lista que desea modificar.
3. Seleccione la casilla **Deshabilitar personalización** y, a continuación, seleccione el botón **Aceptar**.

## <a name="clear-user-personalizations"></a>Borrar personalizaciones de usuarios

Al borrar la personalización de la página, la página vuelve a su diseño original antes de realizar cualquier personalización. Existen dos formas de borrar las personalizaciones que los usuarios han realizado en las páginas: usando la página **Eliminar personalización usuario** o la página **Tarjeta personalización usuario**.

### <a name="clear-user-personalizations-by-using-the-delete-user-personalization-page"></a>Borrar las personalizaciones de los usuarios con la página Eliminar personalización de usuarios.

La página **Eliminar personalización de usuarios** le permite borrar la personalización por página y por usuario.

1.  Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Eliminar personalización usuario** y luego elija el enlace relacionado.

    La página enumera todas las páginas que se han personalizado y el usuario al que pertenece.

    >[!NOTE]
    > Una marca de verificación en las columnas **Personalización heredada** indica que la personalización se realizó en una versión anterior de [!INCLUDE[d365fin](includes/d365fin_md.md)] que manejaba la personalización de forma diferente a como lo hace ahora. Los usuarios que intentan personalizar estas páginas se bloquean a menos que elijan desbloquear la página. Para obtener más información, consulte [Por qué la página está bloqueada para la personalización](ui-personalization-locked.md).

2. Seleccione el movimiento que desea eliminar y, después, seleccione **Eliminar**.

    El usuario podrá ver los cambios la próxima vez que inicie sesión.

### <a name="clear-user-personalizations-by-using-the-user-personalization-card-page"></a>Borrar las personalizaciones de los usuarios con la página Tarjeta personalización de usuarios

La página **Tarjeta personalización de usuarios** le permite borrar la personalización en todas las páginas de un usuario específico. Esto requiere permiso de escritura para el **perfil** de tabla 2000000072.

1.  Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Personalización usuario** y luego elija el enlace relacionado.

    La página **Personalización usuario** muestra todos los usuarios que potencialmente hayan personalizado las páginas. Si no puede encontrar un usuario en la lista, significa que no tiene páginas personalizadas.

2. Seleccione el usuario de la lista y, a continuación, seleccione la acción **Editar**.

3.  En la pestaña **Acciones**, elija **Borrar páginas personalizadas**.

    El usuario podrá ver los cambios la próxima vez que inicie sesión.

## <a name="see-also"></a>Consulte también
[Personalización de su área de trabajo](ui-personalization-user.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Cambiar la configuración básica](ui-change-basic-settings.md)  
[Cambiar las funciones que se muestran](ui-experiences.md)  

