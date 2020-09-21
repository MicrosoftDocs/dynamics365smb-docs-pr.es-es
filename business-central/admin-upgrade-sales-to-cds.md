---
title: Actualización de una integración con Dynamics 365 Sales | Microsoft Docs
description: Obtenga información sobre cómo preparar Dynamics 365 Business Central para integrarse con Dynamics 365 Sales.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, integrating
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: 57bb8d6ee48b608074a669109bdd99abf8c452c2
ms.sourcegitcommit: 351eb465e6dfb3d01c0f3ea406db340f393f47fc
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/01/2020
ms.locfileid: "3742840"
---
# <a name="upgrading-an-integration-with-dynamics-365-sales"></a><span data-ttu-id="e3b6f-103">Actualización de una integración con Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="e3b6f-103">Upgrading an Integration with Dynamics 365 Sales</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="e3b6f-104">se integra con [!INCLUDE[d365fin](includes/cds_long_md.md)], lo que facilita la conexión y sincronización de datos con otras aplicaciones de Dynamics 365, como [!INCLUDE[crm_md](includes/crm_md.md)], o incluso aplicaciones que crea usted mismo.</span><span class="sxs-lookup"><span data-stu-id="e3b6f-104">integrates with [!INCLUDE[d365fin](includes/cds_long_md.md)], which makes it easy to connect and synchronize data with other Dynamics 365 applications, such as [!INCLUDE[crm_md](includes/crm_md.md)], or even apps that you build yourself.</span></span> <span data-ttu-id="e3b6f-105">Si está integrando por primera vez, le recomendamos que lo haga a través de [!INCLUDE[d365fin](includes/cds_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="e3b6f-105">If you are integrating for the first time, we recommend that you do so through [!INCLUDE[d365fin](includes/cds_long_md.md)].</span></span> <span data-ttu-id="e3b6f-106">Para obtener más información, vea [Integración con Common Data Service](admin-common-data-service.md).</span><span class="sxs-lookup"><span data-stu-id="e3b6f-106">For more information, see [Integration with Common Data Service](admin-common-data-service.md).</span></span>

<span data-ttu-id="e3b6f-107">Si ya ha integrado [!INCLUDE[crm_md](includes/crm_md.md)] con [!INCLUDE[d365fin](includes/d365fin_md.md)], puede continuar sincronizando datos utilizando su configuración.</span><span class="sxs-lookup"><span data-stu-id="e3b6f-107">If you have already integrated [!INCLUDE[crm_md](includes/crm_md.md)] with [!INCLUDE[d365fin](includes/d365fin_md.md)], you can continue to synchronize data using your setup.</span></span> <span data-ttu-id="e3b6f-108">Sin embargo, si actualiza [!INCLUDE[d365fin](includes/d365fin_md.md)] o desactiva la integración de [!INCLUDE[crm_md](includes/crm_md.md)], para activarla de nuevo debe conectarse a través de [!INCLUDE[d365fin](includes/cds_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="e3b6f-108">However, if you upgrade [!INCLUDE[d365fin](includes/d365fin_md.md)], or turn off your [!INCLUDE[crm_md](includes/crm_md.md)] integration, to turn it on again you must connect through [!INCLUDE[d365fin](includes/cds_long_md.md)].</span></span> 

> [!NOTE]
> <span data-ttu-id="e3b6f-109">La reconexión a través de [!INCLUDE[d365fin](includes/cds_long_md.md)] aplicará la configuración de sincronización predeterminada y sobrescribirá cualquier configuración que tenga.</span><span class="sxs-lookup"><span data-stu-id="e3b6f-109">Reconnecting through [!INCLUDE[d365fin](includes/cds_long_md.md)] will apply default synchronization settings, and will overwrite any configurations you have.</span></span> <span data-ttu-id="e3b6f-110">Por ejemplo, se aplicarán las asignaciones de tabla predeterminadas.</span><span class="sxs-lookup"><span data-stu-id="e3b6f-110">For example, the default table mappings will be applied.</span></span>

## <a name="to-upgrade-your-connection-to-use-common-data-service"></a><span data-ttu-id="e3b6f-111">Para actualizar su conexión para usar Common Data Service</span><span class="sxs-lookup"><span data-stu-id="e3b6f-111">To upgrade your connection to use Common Data Service</span></span>
1. <span data-ttu-id="e3b6f-112">Abra la página **Configuración de conexión de Microsoft Dynamics 365** y elija **Habilitar** para desactivar la conexión existente con [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="e3b6f-112">Open the **Microsoft Dynamics 365 Connection Setup** page, choose the **Enable** toggle to turn off your existing connection to [!INCLUDE[crm_md](includes/crm_md.md)].</span></span>
2. <span data-ttu-id="e3b6f-113">Abra la página **Configuración de conexión de Common Data Service** y elija **Habilitar** para activar la conexión.</span><span class="sxs-lookup"><span data-stu-id="e3b6f-113">Open the **Common Data Service Connection Setup** page, and choose the **Enable** toggle to turn on the connection.</span></span>
  
   <span data-ttu-id="e3b6f-114">Después de habilitar la conexión CDS, la solución de integración base de CDS de Business Central se implementa en Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="e3b6f-114">After you enable the CDS connection, the Business Central CDS Base Integration Solution is deployed to Common Data Service.</span></span>
3. <span data-ttu-id="e3b6f-115">Desinstalar la solución de integración de Microsoft Dynamics 365 Business Central desde Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="e3b6f-115">Uninstall the Microsoft Dynamics 365 Business Central Integration solution from your Dynamics 365 Sales.</span></span> <span data-ttu-id="e3b6f-116">Para más información, ver [Desinstale o elimine un tema de solución](/powerapps/developer/common-data-service/uninstall-delete-solution).</span><span class="sxs-lookup"><span data-stu-id="e3b6f-116">For more information, see [Uninstall or delete a solution topic](/powerapps/developer/common-data-service/uninstall-delete-solution).</span></span> 

4. <span data-ttu-id="e3b6f-117">En la página **Configuración de conexión de Microsoft Dynamics 365**, elija **Habilitar** para conectarse a [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="e3b6f-117">On the **Microsoft Dynamics 365 Connection Setup** page, turn on the **Enable** toggle to connect to [!INCLUDE[crm_md](includes/crm_md.md)].</span></span>
  
   <span data-ttu-id="e3b6f-118">Después de habilitar la conexión a Sales, la solución de integración de Business Central se implementa en Sales.</span><span class="sxs-lookup"><span data-stu-id="e3b6f-118">After you enable the Sales connection, the Business Central Integration Solution is deployed to Sales.</span></span> <span data-ttu-id="e3b6f-119">Esto permite la integración con entidades que son específicas de [!INCLUDE[crm_md](includes/crm_md.md)], como pedidos de ventas, presupuestos y facturas.</span><span class="sxs-lookup"><span data-stu-id="e3b6f-119">This enables integration with entities that are specific to [!INCLUDE[crm_md](includes/crm_md.md)], such as sales orders, quotes, and invoices.</span></span>
5. <span data-ttu-id="e3b6f-120">En la página **Configuración de conexión de Sales**, elija **Usar configuración de sincronización predeterminada** para inicializar las asignaciones de tablas de integración para [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="e3b6f-120">On the **Sales Connection Setup** page, choose **Use Default Synchronization Setup** to initialize the integration table mappings for [!INCLUDE[crm_md](includes/crm_md.md)].</span></span>

## <a name="see-also"></a><span data-ttu-id="e3b6f-121">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e3b6f-121">See Also</span></span>
[<span data-ttu-id="e3b6f-122">Integración con Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="e3b6f-122">Integrating with Dynamics 365 Sales</span></span>](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[<span data-ttu-id="e3b6f-123">Integración con Common Data Service</span><span class="sxs-lookup"><span data-stu-id="e3b6f-123">Integrating with Common Data Service</span></span>](admin-common-data-service.md)
