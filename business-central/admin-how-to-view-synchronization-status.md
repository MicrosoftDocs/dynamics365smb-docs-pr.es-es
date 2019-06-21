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
# <a name="view-the-status-of-a-synchronization"></a><span data-ttu-id="7a4b2-103">Ver el estado de una sincronización</span><span class="sxs-lookup"><span data-stu-id="7a4b2-103">View the Status of a Synchronization</span></span>
<span data-ttu-id="7a4b2-104">Puede ver el estado de los proyectos individuales de sincronización que se han ejecutado para la integración de [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="7a4b2-104">You can view the status of the individual synchronization jobs that have been run for [!INCLUDE[crm_md](includes/crm_md.md)] integration.</span></span> <span data-ttu-id="7a4b2-105">Esto incluye proyectos de sincronización que se han ejecutado desde la cola de proyectos y proyectos manuales de sincronización que se han realizado en registros desde [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="7a4b2-105">This includes synchronization jobs that have been run from the job queue and manual synchronization jobs that were performed on records from [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="7a4b2-106">Esto es útil al solucionar problemas de sincronización porque le concede acceso a los detalles sobre los errores específicos.</span><span class="sxs-lookup"><span data-stu-id="7a4b2-106">This is helpful when troubleshooting synchronization problems because it gives you access to details about specific errors.</span></span>

### <a name="to-view-synchronization-issues-for-coupled-records"></a><span data-ttu-id="7a4b2-107">Para ver los problemas de sincronización de los registros emparejados</span><span class="sxs-lookup"><span data-stu-id="7a4b2-107">To view synchronization issues for coupled records</span></span>
1. <span data-ttu-id="7a4b2-108">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Errores de sincronización de datos emparejados** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="7a4b2-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Coupled Data Synchronization Errors**, and then choose the related link.</span></span>
2. <span data-ttu-id="7a4b2-109">La página **Errores de sincronización de datos emparejados** muestra los problemas que se produjeron al sincronizar registros emparejados.</span><span class="sxs-lookup"><span data-stu-id="7a4b2-109">The **Coupled Data Synchronization Errors** page shows issues that occurred when you synchronized coupled records.</span></span> <span data-ttu-id="7a4b2-110">Puede filtrar y ordenar los registros y realizar acciones como **Restaurar** o **Eliminar registros** para resolver los problemas uno por uno.</span><span class="sxs-lookup"><span data-stu-id="7a4b2-110">You can filter and sort records and take actions such as **Restore** or **Delete Records** to resolve issues one by one.</span></span>

### <a name="to-view-synchronization-log-for-specific-manually-synchronized-record"></a><span data-ttu-id="7a4b2-111">Para ver el registro de sincronización de un registro específico (sincronizado manualmente)</span><span class="sxs-lookup"><span data-stu-id="7a4b2-111">To view synchronization log for specific (manually synchronized) record</span></span>
1. <span data-ttu-id="7a4b2-112">Abrir, por ejemplo, un cliente, un producto o cualquier otro registro que esté sincronizando datos entre [!INCLUDE[d365fin](includes/d365fin_md.md)] y Sales.</span><span class="sxs-lookup"><span data-stu-id="7a4b2-112">Open, for example, a customer, item or any other record that is synchronizing data between [!INCLUDE[d365fin](includes/d365fin_md.md)] and Sales.</span></span>
2. <span data-ttu-id="7a4b2-113">Seleccione la acción **Registro de sincronización** para ver el registro de sincronización de un registro seleccionado.</span><span class="sxs-lookup"><span data-stu-id="7a4b2-113">Choose the **Synchronization Log** action to view the synchronization log for a selected record.</span></span> <span data-ttu-id="7a4b2-114">Por ejemplo, un cliente específico que ha sincronizado manualmente.</span><span class="sxs-lookup"><span data-stu-id="7a4b2-114">For example, a specific customer you synchronized manually.</span></span>

## <a name="see-also"></a><span data-ttu-id="7a4b2-115">Consulte también</span><span class="sxs-lookup"><span data-stu-id="7a4b2-115">See Also</span></span>  
[<span data-ttu-id="7a4b2-116">Configuración de la integración de Dynamics 365 for Sales en Business Central</span><span class="sxs-lookup"><span data-stu-id="7a4b2-116">Setting Up Dynamics 365 for Sales Integration in Business Central</span></span>](admin-setting-up-integration-with-dynamics-sales.md)  
[<span data-ttu-id="7a4b2-117">Uso de Dynamics 365 for Sales desde Business Central</span><span class="sxs-lookup"><span data-stu-id="7a4b2-117">Using Dynamics 365 for Sales from Business Central</span></span>](marketing-integrate-dynamicscrm.md)
