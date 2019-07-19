---
title: Solución de problemas de errores de sincronización | Documentos de Microsoft
description: Proporciona orientación para identificar y resolver los errores de sincronización.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/11/2019
ms.author: bholtorf
ms.openlocfilehash: bb6d0837f91240eb31abc7c02895cf2da420bf7d
ms.sourcegitcommit: 8fe694b7bbe7fc0456ed5a9e42291218d2251b05
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 07/04/2019
ms.locfileid: "1726795"
---
# <a name="troubleshooting-synchronization-errors"></a>Solución de problemas de errores de sincronización
Hay muchos factores involucrados en la integración de [!INCLUDE[d365fin](includes/d365fin_md.md)] con [!INCLUDE[crm_md](includes/crm_md.md)], y a veces las cosas salen mal. Este tema señala algunos de los errores típicos que se producen y ofrece algunos consejos para corregirlos.

A menudo se producen errores, ya sea por algo que un usuario ha hecho a los registros emparejados o por algo que no funciona en la configuración de la integración. En el caso de los errores relacionados con los registros emparejados, los usuarios pueden resolverlos por sí mismos. Estos errores se deben a acciones tales como eliminar un registro en una aplicación empresarial, pero no en las dos, y después realizar la sincronización. Para obtener más información, consulte [Ver el estado de una sincronización](admin-how-to-view-synchronization-status.md).

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2097304]

Los errores relacionados con la configuración de la integración suelen requerir la atención de un administrador. Puede ver estos errores en la página **Errores de sincronización de integración**. Algunos ejemplos de problemas típicos son:  
  
* Los permisos y los roles asignados a los usuarios no son correctos.  
* La cuenta de administrador se especificó como el usuario de integración.  
* La contraseña del usuario de integración está configurada para requerir un cambio cuando el usuario inicia sesión.  
* Los tipos de cambio de las divisas no se especifican en una u otra aplicación.  
  
Debe resolver manualmente los errores, pero hay algunas maneras en las que la página le ayuda. Por ejemplo:  

* Los campos **Origen** y **Destino** pueden contener vínculos al registro donde se encontró el error. Haga clic en el vínculo para abrir el registro e investigar el error.  
* Las acciones **Eliminar movs. anteriores a 7 días** y **Eliminar todos los movs.** limpiarán la lista. Normalmente, estas acciones se utilizan después de haber resuelto la causa de un error que afecta a muchos registros. Sin embargo, preste atención. Estas acciones pueden eliminar errores que todavía son relevantes.

## <a name="see-also"></a>Consulte también
[Integración con [!INCLUDE[crm_md](includes/crm_md.md)]](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[Configuración de cuentas de usuario para la integración con [!INCLUDE[crm_md](includes/crm_md.md)]](admin-setting-up-integration-with-dynamics-sales.md)  
[Configurar una conexión a [!INCLUDE[crm_md](includes/crm_md.md)]](admin-how-to-set-up-a-dynamics-crm-connection.md)  
[Emparejar y sincronizar registros manualmente](admin-how-to-couple-and-synchronize-records-manually.md)  
[Ver el estado de una sincronización](admin-how-to-view-synchronization-status.md)  