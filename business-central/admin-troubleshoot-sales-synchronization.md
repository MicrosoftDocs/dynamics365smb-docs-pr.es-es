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
# <a name="troubleshooting-synchronization-errors"></a><span data-ttu-id="901db-103">Solución de problemas de errores de sincronización</span><span class="sxs-lookup"><span data-stu-id="901db-103">Troubleshooting Synchronization Errors</span></span>
<span data-ttu-id="901db-104">Hay muchos factores involucrados en la integración de [!INCLUDE[d365fin](includes/d365fin_md.md)] con [!INCLUDE[crm_md](includes/crm_md.md)], y a veces las cosas salen mal.</span><span class="sxs-lookup"><span data-stu-id="901db-104">There are lots of moving parts involved in integrating [!INCLUDE[d365fin](includes/d365fin_md.md)] with [!INCLUDE[crm_md](includes/crm_md.md)], and sometimes things go wrong.</span></span> <span data-ttu-id="901db-105">Este tema señala algunos de los errores típicos que se producen y ofrece algunos consejos para corregirlos.</span><span class="sxs-lookup"><span data-stu-id="901db-105">This topic points out some of the typical errors that occur and gives some pointers for how to fix them.</span></span>

<span data-ttu-id="901db-106">A menudo se producen errores, ya sea por algo que un usuario ha hecho a los registros emparejados o por algo que no funciona en la configuración de la integración.</span><span class="sxs-lookup"><span data-stu-id="901db-106">Errors often occur either because of something that a user has done to coupled records or something is wrong with how the integration is set up.</span></span> <span data-ttu-id="901db-107">En el caso de los errores relacionados con los registros emparejados, los usuarios pueden resolverlos por sí mismos.</span><span class="sxs-lookup"><span data-stu-id="901db-107">For errors related to coupled records, users can resolve those themselves.</span></span> <span data-ttu-id="901db-108">Estos errores se deben a acciones tales como eliminar un registro en una aplicación empresarial, pero no en las dos, y después realizar la sincronización.</span><span class="sxs-lookup"><span data-stu-id="901db-108">These errors are caused by actions such as deleting a record in one, but not both, business apps and then synchronizing.</span></span> <span data-ttu-id="901db-109">Para obtener más información, consulte [Ver el estado de una sincronización](admin-how-to-view-synchronization-status.md).</span><span class="sxs-lookup"><span data-stu-id="901db-109">For more information, see [View the Status of a Synchronization](admin-how-to-view-synchronization-status.md).</span></span>

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2097304]

<span data-ttu-id="901db-110">Los errores relacionados con la configuración de la integración suelen requerir la atención de un administrador.</span><span class="sxs-lookup"><span data-stu-id="901db-110">Errors that are related to how the integration is set up typically require an administrator's attention.</span></span> <span data-ttu-id="901db-111">Puede ver estos errores en la página **Errores de sincronización de integración**.</span><span class="sxs-lookup"><span data-stu-id="901db-111">You can view these errors on the **Integration Synchronization Errors** page.</span></span> <span data-ttu-id="901db-112">Algunos ejemplos de problemas típicos son:</span><span class="sxs-lookup"><span data-stu-id="901db-112">Examples of some typical issues include:</span></span>  
  
* <span data-ttu-id="901db-113">Los permisos y los roles asignados a los usuarios no son correctos.</span><span class="sxs-lookup"><span data-stu-id="901db-113">The permissions and roles assigned to users are not correct.</span></span>  
* <span data-ttu-id="901db-114">La cuenta de administrador se especificó como el usuario de integración.</span><span class="sxs-lookup"><span data-stu-id="901db-114">The administrator account was specified as the integration user.</span></span>  
* <span data-ttu-id="901db-115">La contraseña del usuario de integración está configurada para requerir un cambio cuando el usuario inicia sesión.</span><span class="sxs-lookup"><span data-stu-id="901db-115">The integration user’s password is set to require a change when the user signs in.</span></span>  
* <span data-ttu-id="901db-116">Los tipos de cambio de las divisas no se especifican en una u otra aplicación.</span><span class="sxs-lookup"><span data-stu-id="901db-116">The exchange rates for currencies are not specified in one or the other app.</span></span>  
  
<span data-ttu-id="901db-117">Debe resolver manualmente los errores, pero hay algunas maneras en las que la página le ayuda.</span><span class="sxs-lookup"><span data-stu-id="901db-117">You must manually resolve the errors, but there are a few ways in which the page helps you.</span></span> <span data-ttu-id="901db-118">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="901db-118">For example:</span></span>  

* <span data-ttu-id="901db-119">Los campos **Origen** y **Destino** pueden contener vínculos al registro donde se encontró el error.</span><span class="sxs-lookup"><span data-stu-id="901db-119">The **Source** and **Destination** fields may contain links to the record where the error was found.</span></span> <span data-ttu-id="901db-120">Haga clic en el vínculo para abrir el registro e investigar el error.</span><span class="sxs-lookup"><span data-stu-id="901db-120">Click the link to open the record and investigate the error.</span></span>  
* <span data-ttu-id="901db-121">Las acciones **Eliminar movs. anteriores a 7 días** y **Eliminar todos los movs.** limpiarán la lista.</span><span class="sxs-lookup"><span data-stu-id="901db-121">The **Delete Entries Older than 7 Days** and the **Delete All Entries** actions will clean up the list.</span></span> <span data-ttu-id="901db-122">Normalmente, estas acciones se utilizan después de haber resuelto la causa de un error que afecta a muchos registros.</span><span class="sxs-lookup"><span data-stu-id="901db-122">Typically, you use these actions after you have resolved the cause of an error that affects many records.</span></span> <span data-ttu-id="901db-123">Sin embargo, preste atención.</span><span class="sxs-lookup"><span data-stu-id="901db-123">Use caution, however.</span></span> <span data-ttu-id="901db-124">Estas acciones pueden eliminar errores que todavía son relevantes.</span><span class="sxs-lookup"><span data-stu-id="901db-124">These actions might delete errors that are still relevant.</span></span>

## <a name="see-also"></a><span data-ttu-id="901db-125">Consulte también</span><span class="sxs-lookup"><span data-stu-id="901db-125">See Also</span></span>
<span data-ttu-id="901db-126">[Integración con [!INCLUDE[crm_md](includes/crm_md.md)]](admin-prepare-dynamics-365-for-sales-for-integration.md)</span><span class="sxs-lookup"><span data-stu-id="901db-126">[Integrating with [!INCLUDE[crm_md](includes/crm_md.md)]](admin-prepare-dynamics-365-for-sales-for-integration.md)</span></span>  
<span data-ttu-id="901db-127">[Configuración de cuentas de usuario para la integración con [!INCLUDE[crm_md](includes/crm_md.md)]](admin-setting-up-integration-with-dynamics-sales.md)</span><span class="sxs-lookup"><span data-stu-id="901db-127">[Setting Up User Accounts for Integrating with [!INCLUDE[crm_md](includes/crm_md.md)]](admin-setting-up-integration-with-dynamics-sales.md)</span></span>  
<span data-ttu-id="901db-128">[Configurar una conexión a [!INCLUDE[crm_md](includes/crm_md.md)]](admin-how-to-set-up-a-dynamics-crm-connection.md)</span><span class="sxs-lookup"><span data-stu-id="901db-128">[Set Up a Connection to [!INCLUDE[crm_md](includes/crm_md.md)]](admin-how-to-set-up-a-dynamics-crm-connection.md)</span></span>  
[<span data-ttu-id="901db-129">Emparejar y sincronizar registros manualmente</span><span class="sxs-lookup"><span data-stu-id="901db-129">Couple and Synchronize Records Manually</span></span>](admin-how-to-couple-and-synchronize-records-manually.md)  
[<span data-ttu-id="901db-130">Ver el estado de una sincronización</span><span class="sxs-lookup"><span data-stu-id="901db-130">View the Status of a Synchronization</span></span>](admin-how-to-view-synchronization-status.md)  