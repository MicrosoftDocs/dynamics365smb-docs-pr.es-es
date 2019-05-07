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
ms.openlocfilehash: d55d8d5ab916cee6600deaf891702a625d76d7ee
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2019
ms.locfileid: "940341"
---
# <a name="view-the-status-of-a-synchronization"></a><span data-ttu-id="f0658-103">Ver el estado de una sincronización</span><span class="sxs-lookup"><span data-stu-id="f0658-103">View the Status of a Synchronization</span></span>
<span data-ttu-id="f0658-104">Puede ver el estado de los proyectos individuales de sincronización que se han ejecutado para la integración de [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="f0658-104">You can view the status of the individual synchronization jobs that have been run for [!INCLUDE[crm_md](includes/crm_md.md)] integration.</span></span> <span data-ttu-id="f0658-105">Esto incluye proyectos de sincronización que se han ejecutado desde la cola de proyectos y proyectos manuales de sincronización que se han realizado en registros desde [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="f0658-105">This includes synchronization jobs that have been run from the job queue and manual synchronization jobs that were performed on records from [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="f0658-106">Esto es útil al solucionar problemas de sincronización porque le concede acceso a los detalles sobre los errores específicos.</span><span class="sxs-lookup"><span data-stu-id="f0658-106">This is helpful when troubleshooting synchronization problems because it gives you access to details about specific errors.</span></span>

### <a name="to-view-all-synchronization-issues"></a><span data-ttu-id="f0658-107">Para ver todos los errores de sincronización</span><span class="sxs-lookup"><span data-stu-id="f0658-107">To view all synchronization issues</span></span>
1. <span data-ttu-id="f0658-108">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Errores de sincronización de datos emparejados** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="f0658-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Coupled Data Synchronization Errors**, and then choose the related link.</span></span>
2. <span data-ttu-id="f0658-109">En la página **Errores de sincronización de datos emparejados**, puede ver todos los problemas que se han producido en la sincronización de datos entre [!INCLUDE[crm_md](includes/crm_md.md)] y [!INCLUDE[d365fin](includes/d365fin_md.md)], filtrar y ordenar los registros de la página por tabla, mensaje de error y realizar acciones como **Reintentar** o **Eliminar emparejamiento** para resolver los problemas de uno en uno o de forma masiva.</span><span class="sxs-lookup"><span data-stu-id="f0658-109">On the **Coupled Data Synchronization Errors** page you can view of all issues that occurred in synchronization of data between [!INCLUDE[crm_md](includes/crm_md.md)] and [!INCLUDE[d365fin](includes/d365fin_md.md)], filter and sort records in the page by table, error message and take actions such as **Retry** or **Remove Coupling** to resolve issues one by one or in bulk.</span></span>

### <a name="to-view-synchronization-log-for-specific-manually-synchronized-record"></a><span data-ttu-id="f0658-110">Para ver el registro de sincronización de un registro específico (sincronizado manualmente)</span><span class="sxs-lookup"><span data-stu-id="f0658-110">To view synchronization log for specific (manually synchronized) record</span></span>
1. <span data-ttu-id="f0658-111">Abrir, por ejemplo, un cliente, un producto o cualquier otro registro que esté sincronizando datos entre [!INCLUDE[d365fin](includes/d365fin_md.md)] y Sales</span><span class="sxs-lookup"><span data-stu-id="f0658-111">Open, for example, customer, item or any other record that is synchronizing data between [!INCLUDE[d365fin](includes/d365fin_md.md)] and Sales</span></span>
2. <span data-ttu-id="f0658-112">Seleccione la acción **Registro de sincronización** para ver el registro de sincronización del registro seleccionado, por ejemplo, un cliente específico que haya sincronizado manualmente.</span><span class="sxs-lookup"><span data-stu-id="f0658-112">Choose **Synchronization Log** action to view the synchronization log for selected record, for example, specific customer you synchronized manually</span></span>

## <a name="see-also"></a><span data-ttu-id="f0658-113">Consulte también</span><span class="sxs-lookup"><span data-stu-id="f0658-113">See Also</span></span>  
[<span data-ttu-id="f0658-114">Configuración de la integración de Dynamics 365 for Sales en Business Central</span><span class="sxs-lookup"><span data-stu-id="f0658-114">Setting Up Dynamics 365 for Sales Integration in Business Central</span></span>](admin-setting-up-integration-with-dynamics-sales.md)  
[<span data-ttu-id="f0658-115">Uso de Dynamics 365 for Sales desde Business Central</span><span class="sxs-lookup"><span data-stu-id="f0658-115">Using Dynamics 365 for Sales from Business Central</span></span>](marketing-integrate-dynamicscrm.md)
