---
title: Ver el estado de una sincronización | Documentos de Microsoft
description: Obtenga información sobre cómo ver el estado de un proyecto de sincronización individual.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: 11e29674c2d12031fdf4e7f66e767be4fcc74795
ms.sourcegitcommit: 04581558f6c5488c705a7ac392cf297be10b5f4f
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/06/2019
ms.locfileid: "1620889"
---
# <a name="view-the-status-of-a-synchronization"></a>Ver el estado de una sincronización
Puede ver el estado de los proyectos individuales de sincronización que se han ejecutado para la integración de [!INCLUDE[crm_md](includes/crm_md.md)]. Esto incluye proyectos de sincronización que se han ejecutado desde la cola de proyectos y proyectos manuales de sincronización que se han realizado en registros desde [!INCLUDE[d365fin](includes/d365fin_md.md)]. Esto es útil al solucionar problemas de sincronización porque le concede acceso a los detalles sobre los errores específicos.

### <a name="to-view-synchronization-issues-for-coupled-records"></a>Para ver los problemas de sincronización de los registros emparejados
1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Errores de sincronización de datos emparejados** y luego elija el enlace relacionado.
2. La página **Errores de sincronización de datos emparejados** muestra los problemas que se produjeron al sincronizar registros emparejados. Puede filtrar y ordenar los registros y realizar acciones como **Restaurar** o **Eliminar registros** para resolver los problemas uno por uno.

### <a name="to-view-synchronization-log-for-specific-manually-synchronized-record"></a>Para ver el registro de sincronización de un registro específico (sincronizado manualmente)
1. Abrir, por ejemplo, un cliente, un producto o cualquier otro registro que esté sincronizando datos entre [!INCLUDE[d365fin](includes/d365fin_md.md)] y Sales.
2. Seleccione la acción **Registro de sincronización** para ver el registro de sincronización de un registro seleccionado. Por ejemplo, un cliente específico que ha sincronizado manualmente.

## <a name="see-also"></a>Consulte también  
[Configuración de la integración de Dynamics 365 for Sales en Business Central](admin-setting-up-integration-with-dynamics-sales.md)  
[Uso de Dynamics 365 for Sales desde Business Central](marketing-integrate-dynamicscrm.md)
