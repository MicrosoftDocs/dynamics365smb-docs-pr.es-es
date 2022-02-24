---
title: Por qué no puedo personalizar una página | Documentos de Microsoft
description: Explica por qué no puede personalizar una página y qué puede hacer para desbloquearla.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.date: 04/01/2019
ms.author: jswymer
ms.openlocfilehash: 1a3edaca2e76388d82ea8991c3196410dd9c7288
ms.sourcegitcommit: a88d1e9c0ab647cb8d9d81d32c0bdc82843f4145
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 07/31/2019
ms.locfileid: "1796771"
---
# <a name="why-a-page-is-locked-from-personalization"></a>Por qué la página está bloqueada para evitar la personalización

Hay dos condiciones que le impiden personalizar una página. La página está bloqueada (como se indica en ![Personalización bloqueada](media/personalization-lock-icon.png "Personalización bloqueada")) o está bloqueada (como se indica en ![Bloqueo de personalización](media/personalization-blocked-icon.png "Bloqueo de personalización")).

## <a name="locked-from-personalizing"></a>Bloqueado para evitar la personalización

Si hay un icono ![Bloqueo de personalización](media/personalization-lock-icon.png "Bloqueo de personalización") en el banner de **Personalización** cuando abre una página (como se muestra), significa que actualmente se le impide realizar más cambios de personalización en la página.

![Personalización bloqueada](media/personalization-locked.png "Personalización bloqueada")


<!-- This is because we changed the way personalization works behind the scenes since the last time that you personalized the page. Unfortunately, the old way and new of doing things do not work together.

The page currently includes the last personalization changes that you made. If you want to continue personalizing the page, then you can choose the lock icon and then **Unlock**. Just be aware that if you choose to unlock the page, the current personalization of the page will be cleared, and you will have to start from scratch.
-->

Puede haber dos razones para ello:

1. Ha personalizado la página antes, pero lo ha hecho con una versión anterior del producto. Hemos cambiado la manera en que la personalización funciona en segundo plano desde la última vez que personalizó la página. Desafortunadamente, la formas de hacer las cosas antigua y nueva no funcionan juntas.

2. Hasta ahora, ha utilizado únicamente el [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] para personalizar la página.

### <a name="unlocking-the-page"></a>Desbloqueo de la página

Si desea desbloquear una página y seguir personalizándola, seleccione ![Bloqueo de personalización](media/personalization-lock-icon.png "Bloqueo de personalización") y, a continuación, **Desbloquear**.  

Antes de desbloquear la página, tenga en cuenta lo siguiente:

- Se borrará la personalización actual de la página. La página volverá a su diseño original y tendrá que empezar desde cero.

- En [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)], la página permanecerá tal cual y no se verá afectada por los nuevos cambios de personalización realizados en el cliente de Business Central. En el futuro, la personalización en [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] y el cliente de Business Central serán completamente independientes entre sí.

## <a name="blocked-from-personalizing"></a>Bloqueado para evitar la personalización

Si hay un icono ![Personalización bloqueada](media/personalization-blocked-icon.png "Personalización bloqueada") en el banner Personalización, significa que se le impide hacer cualquier personalización de la página.

![Personalización bloqueada](media/personalization-blocked.png "Bloqueo de personalización")

La razón de esto es que el área de trabajo o rol que está actualmente asociado con su cuenta de usuario modifica esta página específicamente para su rol. Póngase en contacto con su administrador para obtener ayuda o, si tiene sentido, intente cambiar a un área de trabajo (desde [**Mi configuración**](https://businesscentral.dynamics.com?page=9176 "Vaya directamente a la página de configuración del usuario en Business Central")) que incluya la personalización de rol para esta página.

## <a name="see-also"></a>Consulte también
[Personalización de su área de trabajo](ui-personalization-manage.md)  
[Administrar la personalización](ui-personalization-manage.md)  
[Cambiar la configuración básica](ui-change-basic-settings.md)  
[Cambiar las funciones que se muestran](ui-experiences.md)  
