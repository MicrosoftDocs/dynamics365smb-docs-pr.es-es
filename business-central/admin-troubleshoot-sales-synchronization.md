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
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: 1c2181ee381425a168a9b6b6ce321e595a01ed8e
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "4754997"
---
# <a name="troubleshooting-synchronization-errors"></a>Solución de problemas de errores de sincronización
[!INCLUDE[prod_short](includes/cc_data_platform_banner.md)]

Hay muchos factores involucrados en la integración de [!INCLUDE[prod_short](includes/prod_short.md)] con [!INCLUDE[prod_short](includes/cds_long_md.md)], y a veces las cosas salen mal. Este tema señala algunos de los errores típicos que se producen y ofrece algunos consejos para corregirlos.

A menudo se producen errores, ya sea por algo que un usuario ha hecho a los registros emparejados o por algo que no funciona en la configuración de la integración. En el caso de los errores relacionados con los registros emparejados, los usuarios pueden resolverlos por sí mismos. Estos errores se deben a acciones tales como eliminar datos en una aplicación empresarial, pero no en las dos, y después realizar la sincronización. Para obtener más información, consulte [Ver el estado de una sincronización](admin-how-to-view-synchronization-status.md).

## <a name="example"></a>Ejemplo:
Este vídeo muestra un ejemplo de cómo solucionar errores que ocurrieron al sincronizar con Sales. El proceso será el mismo para todas las integraciones. 

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2097304]

Los errores relacionados con la configuración de la integración suelen requerir la atención de un administrador. Puede ver estos errores en la página **Errores de sincronización de integración**. Algunos ejemplos de problemas típicos son:  
  
* Los permisos y los roles asignados a los usuarios no son correctos.  
* La cuenta de administrador se especificó como el usuario de integración.  
* La contraseña del usuario de integración está configurada para requerir un cambio cuando el usuario inicia sesión.  
* Los tipos de cambio de las divisas no se especifican en una u otra aplicación.  
  
Debe resolver manualmente los errores, pero hay algunas maneras en las que la página le ayuda. Por ejemplo:  

* Los campos **Origen** y **Destino** pueden contener vínculos a la fila donde se encontró el error. Haga clic en el enlace para investigar el error.  
* Las acciones **Eliminar movs. anteriores a 7 días** y **Eliminar todos los movs.** limpiarán la lista. Normalmente, estas acciones se utilizan después de haber resuelto la causa de un error que afecta a muchos registros. Sin embargo, preste atención. Estas acciones pueden eliminar errores que todavía son relevantes.

A veces, las marcas de tiempo en los registros pueden causar conflictos. La tabla "Registro de integración CDS" mantiene las marcas de tiempo "Fecha de última modificación de sincronización" y "Fecha de última modificación de sincronización de CDS" para la última integración realizada en ambas direcciones para una fila. Estas marcas de tiempo se comparan con las marcas de tiempo en Business Central y los registros de ventas. En Business Central, la marca de tiempo está en la tabla Registro de integración.

Puede filtrar los registros que se van a sincronizar comparando las marcas de tiempo de la fila en los campos "Filtro de fecha modificación de sinc." y "Filtro de fecha modif. tabla integ. de sinc.".

El mensaje de error de conflicto "No se puede actualizar el registro del cliente porque tiene una fecha de modificación posterior al registro de la cuenta" o "No se puede actualizar el registro de la cuenta porque tiene una fecha de modificación posterior al registro del cliente" puede aparecer si una fila tiene una marca de tiempo que es más grande que IntegrationTableMapping."Filtro de fecha modificación de sinc." pero no es más reciente que la marca de tiempo en el registro de integración de ventas. Significa que la fila de origen se sincronizó manualmente, no por el movimiento de la cola de proyectos. 

El conflicto ocurre porque la fila de destino también se modificó: la marca de tiempo de la fila es más reciente que la marca de tiempo del registro de integración de ventas. La verificación de destino se realiza solo para tablas bidireccionales. 

Estos registros ahora se mueven a la página "Registros sinc. omitidos", que se abre desde la página Configuración de conexión de Microsoft Dynamics en Business Central. Allí puede especificar los cambios que desea conservar y luego sincronizar nuevamente los registros.

## <a name="remove-couplings-between-records"></a>Eliminar acoplamientos entre registros
Cuando algo sale mal en su integración y necesita desacoplar registros para dejar de sincronizarlos, puede hacerlo para uno o más registros a la vez. Puede desacoplar uno o más registros de las páginas de lista o la página **Errores de sincronización de datos acoplados** eligiendo una o más líneas y eligiendo **Eliminar acoplamiento**. También puede eliminar todos los acoplamientos para una o más asignaciones de tabla en la página **Asignaciones de tablas de integración**. 

## <a name="see-also"></a>Consulte también
[Integración con Microsoft Dataverse](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[Configuración de cuentas de usuario para la integración con Microsoft Dataverse](admin-setting-up-integration-with-dynamics-sales.md)  
[Configurar una conexión a Microsoft Dataverse](admin-how-to-set-up-a-dynamics-crm-connection.md)  
[Emparejar y sincronizar registros manualmente](admin-how-to-couple-and-synchronize-records-manually.md)  
[Ver el estado de una sincronización](admin-how-to-view-synchronization-status.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]